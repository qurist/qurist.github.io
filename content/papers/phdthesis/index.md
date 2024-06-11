---
title: Design and Optimization in Near-Term Quantum Computation 
date: 2021-08-21
url: /papers/phdthesis/
tags: ["quantum computation", "thesis", "quantum optimization", "optimal control", "quantum architectures"]
author: [<a href="/">Aniruddha Bapat</a>]
summary: My PhD thesis
editPost:
    URL: <a href="https://www.proquest.com/docview/2585963518?pq-origsite=gscholar&fromopenview=true&sourcetype=Dissertations%20&%20Theses"> Link <\a>
citation: Bapat, A. A. (2021). "Design and Optimization in Near-Term Quantum Computation". *Doctoral dissertation, University of Maryland, College Park*.

---


---

##### Download

- [Thesis](/papers/phdthesis/paper.pdf)

---

##### Abstract

Quantum computers have come a long way since conception, and there is still a long way to go before the dream of universal, fault-tolerant computation is realized. In the near term, quantum computers will occupy a middle ground that is popularly known as the “Noisy, Intermediate-Scale Quantum” (or NISQ) regime. The NISQ era represents a transition in the nature of quantum devices from experimental to computational. There is significant interest in engineering NISQ devices and NISQ algorithms in a manner that will guide the development of quantum computation in this regime and into the era of fault-tolerant quantum computing.

In this thesis, we study two aspects of near-term quantum computation. The first of these is the design of device architectures, covered in Chapters 2, 3, and 4. We examine different qubit connectivities on the basis of their graph properties, and present numerical and analytical results on the speed at which large entangled states can be created on nearest-neighbor grids and graphs with modular structure. Next, we discuss the problem of permuting qubits among the nodes of the connectivity graph using only local operations, also known as routing. Using a fast quantum primitive to reverse the qubits in a chain, we construct a hybrid, quantum/classical routing algorithm on the chain. We show via rigorous bounds that this approach is faster than any SWAP-based algorithm for the same problem.

The second part, which spans the final three chapters, discusses variational algorithms, which are a class of algorithms particularly suited to near-term quantum computation. Two prototypical variational algorithms, quantum adiabatic optimization (QAO) and the quantum approximate optimization algorithm (QAOA), are studied for the difference in their control strategies. We show that on certain crafted problem instances, bang-bang control (QAOA) can be as much as exponentially faster than quasistatic control (QAO). Next, we demonstrate the performance of variational state preparation on an analog quantum simulator based on trapped ions. We show that using classical heuristics that exploit structure in the variational parameter landscape, one can find circuit parameters efficiently in system size as well as circuit depth. In the experiment, we approximate the ground state of a critical Ising model with long-ranged interactions on up to 40 spins. Finally, we study the performance of Local Tensor, a classical heuristic algorithm inspired by QAOA on benchmarking instances of the MaxCut problem, and suggest physically motivated choices for the algorithm hyperparameters that are found to perform well empirically. We also show that our implementation of Local Tensor mimics imaginary-time quantum evolution under the problem Hamiltonian.


---

##### Citation

Bapat, A. A. (2021). "Design and Optimization in Near-Term Quantum Computation". *Doctoral dissertation, University of Maryland, College Park*.

```BibTeX
  @phdthesis{bapat2021design,
  title={Design and Optimization in Near-Term Quantum Computation},
  author={Bapat, Aniruddha A},
  year={2021},
  school={University of Maryland, College Park}
}
```

---

##### Related material

+ [Thesis defense](/papers/phdthesis/presentation.pdf)