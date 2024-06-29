---
title: A quantum-inspired solver for the MaxCut problem
date: 2024-06-17
url: /projects/maxcut/
tags: ["quantum computation", "project", "optimization", "quantum-inspired optimization"]
draft: true
author: [<a href="/">Aniruddha Bapat</a>]
summary: In this project, I describe some quantum-inspired heuristic methods for finding approximate solutions to the MaxCut problem.  
# cover:
#     image: "/papers/analogalgorithms/icon.png"
#     alt: ""
#     relative: true
---


---

##### Code

- [Github]()

---

### Introduction

MaxCut is an NP-hard combinatorial optimization problem that has been used as a benchmark for quantum and quantum-inspired optimization methods. Perhaps two reasons for its popularity are that it is easy to state (as we will, shortly) and has a nice physical interpretation as the energy minimization of an Ising model, which is the quintessential toy model in condensed matter physics. 

Now, the problem: Given an weighted, undirected graph $G$ on $n$ nodes with edge weight $w_{ij}$ for the edge between nodes $i$ and $j$, we are asked to find the graph cut with the maximum weight. A cut is a bipartitioning of the nodes into a left and a right partition, and the weight of a cut is the sum of the weights $w_ij$ where $i$ and $j$ belong to different partitions. 

While there are many ways to formulate this problem mathematically, one useful way is to assign a variable (a "spin") $s_i\in\{-1,1 \}$ to each node $i$ and set $s_i$ to $-1$ if $i$ is in the left partition and $+1$ if $i$ is in the right partition. Then, there is a one-to-one mapping between cuts (of which there are 2^$n$) and "spin" configurations $s_1s_2\ldots s_n$ (of which there are also 2^n). For a given cut, an edge $w_{ij}$ contributes to the cut weight iff $s_i \neq s_j$, or when $s_is_j = -1$. From this, we can consruct the following succint expression for the cut weight in terms of the spin variables,
\begin{equation}
C = \sum_{ij} w_{ij}\left(\frac{1 - s_is_j}{4}\right) .
\end{equation}
The objective is the to maximize $C$ over all possible graph cuts (or equivalently, over all spin configurations). As alluded to before, this is equivalent to minimizing the function $-C$, which looks a lot like an Ising model on the spins $s_i$ with interaction strengths given by $w_{ij}$. This interpretation naturally gives us a way to represent this problem on a quantum computer by mapping each spin to a qubit, and encoding the weights as two-qubit gates (or interations if we're working with an analog device). This is why, rightfully, MaxCut the related quadratic unconstrained binary optimization (or QUBO) class of problems have been widely used as benchmarks in the quantum optimization community. 

In this post, my goal will be to demonstrate a particular class of "local" quantum-inspired solvers for MaxCut. The bulk of it will be based on my own [work](/papers/localtensor) with my PhD advisor Stephen Jordan, which in turn sprang from [this paper](https://arxiv.org/abs/1905.07047) by Matthew Hastings. Unlike its predecessor, our work was concerned less with proving performance bounds and more with the question, "Can we make this algorithm actually work in practice?". The same will be true in this post (less theory, more practice). Lastly, this post is "purely classical" and will not be touching upon the many quantum algorithms that have also been devised to tackle these problems. However, I strongly encourage the reader to take a trip down that rabbit hole!

---
### Benchmarking instances

I will use a fixed set of instances for "training" purposes. These are instances of random-weighted complete graphs I generated using the popular MaxCut instance generator known as rudy. My graphs are all on $n=20$ nodes and have edge weights lying uniformly in the range $[-1000,1000]$. Ultimately for each algorithm we produce in this post, I will test performance on standard benchmarking instances such as the Gset and other instances from the "BiqMac" collection available [here](https://biqmac.aau.at).

---
### Continuous relaxation and gradient ascent

As a first attempt, let's try to build a maximizer based on gradient ascent. In gradient ascent, we start from a random input value and iteratively find the maximum by incrementing the input by a value proportional to the gradient of the function at the input value. This can be thought of as "walking uphill" until you reach a local maximum. By repeating this process many times with random initializations, one can attempt to sample multiple local maxima and pick the best one. 

In our problem, the domain is a discrete set of spin configurations. One way to visualize this set is to picture a $n$-dimensional hypercube with side length 2 that extends from $-1$ to $1$ in each dimension. The corners of such a hypercube are precisely those points with coordinates given by $n$-dimensional vectors with entries lying in ${-1,1}$. Thus, the problem domain can be mapped one-to-one with the corners of this hypercube. 

Gradient ascent doesn't quite work as stated since the domain is discrete, but we could modify it suitably. For instance, in each step one could greedily flip the spin that improves the objective by the largest margin. Or we could pick a random "improving" spin flip. In fact, we could also allow flips that worsen the value of the objective, with a probability that depends on the quality of the flip. When the probabilities take the particular Boltzmann form $p \propto e^{-\beta \Delta C}$, where $\Delta C$ is the decrease in the objective due to the flip, the algorithm is known as simulated annealing. These are all interesting options but I will not pursue them further in this post.

Instead, let's tranform the problem into a continuous one by allowing each spin variable to take real values between $-1$ and $1$. This is known as a relaxation of the domain. In the hypercube picture, we're letting our input be any point inside the hypercube instead of just its corners. Now, we can run gradient ascent (with boundary constraints) to find locally optimal, relaxed spin configurations inside the hypercube. However, since only discrete configurations (i.e. the corners) are valid canditate solutions, we need a procedure to "round" the continuous optima. A very natural mapping is to simply return the sign of each coordinate. That is, given a relaxed configuration $v_1v_2\ldots v_n$, we return $s_1s_2\ldots s_n$ where $s_i = sgn(v_i) = v_i / |v_i|$. Unless we need to, we won't alter this rounding scheme. And, I will adopt the convention of denoting continuous spins by $v_i$ and discrete or rounded spins by $s_i$ everywhere from now on.

Returning the the gradient ascent in continuous space, let's first express the gradient analytically. 
\begin{equation}
\partial C/\partial{v_i} = -\frac{1}{2} \sum_{j} W_{ij} v_j \equiv -\frac{1}{2}(A\cdot \vec{v})_i,
\end{equation}
where $W$ is the weighted adjacency matrix that encodes the edge weights, $W\_{ij}=W\_{ji}=w\_{ij}$. So, we can write the full gradient succinctly as $\nabla_v C = -\frac{1}{2} W\cdot\vec v$. The gradient update is then $\vec v \rightarrow \vec v - \alpha\frac{1}{2} W\cdot\vec v$, where $\alpha$ is commonly referred to as the learning rate, which is a free hyperparameter in the algorithm. In the first go, we can set the learning rate to be a constant. A well-motivated choice for $\alpha$ is based on the Newton's method, in which the learning rate is set to one divided by the second derivative of the function. In our case, the matrix of second derivatives (the Hessian) is equal to $-\frac{1}{2} W$. Therefore, a sensible scalar value for $\alpha$ is simply $2/\lVert W\rVert$ where $\lVert W\rVert$ is an appropriate matrix norm. We'll use the $1$-norm, $\lVert W \rVert_1 = \max_j \sum_i |W\_{ij}|$, which in our case has the natural interpretation of being the maximum possible value of $W\cdot\vec v$ when $v_i \in [-1,1]$.

---
### Experiment 1: Measuring solution quality after a fixed number of gradient updates


---
### Experiment 2: Measuring time-to-solution


---

##### See also

+ [Original paper](/papers/localtensor)
