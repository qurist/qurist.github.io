---
title: Approximate optimization of the MaxCut problem with a local spin algorithm 
date: 2021-05-12
url: /papers/localtensor/
tags: ["quantum computation", "publication", "quantum optimization"]
author: [<a href="/">Aniruddha Bapat</a>, Stephen Jordan]
summary: We study the dynamics and practical performance of a quantum-inspired "local tensor" algorithm for approximate optimization of MaxCut problem instances.
cover:
    image: "/papers/localtensor/icon.png"
    alt: ""
    relative: true
editPost:
    URL: 10.1103/PhysRevA.103.052413
citation: Bapat, A., & Jordan, S. P. (2021). "Approximate optimization of the MaxCut problem with a local spin algorithm". *Physical Review A, 103(5), 052413*.
---


---

##### Download

- [Paper](/papers/localtensor/paper.pdf)

---

##### Abstract

Local tensor methods are a class of optimization algorithms introduced in [Hastings, [arXiv:1905.07047v2](https://arxiv.org/abs/1905.07047)] as a classical analogue of the quantum approximate optimization algorithm. These algorithms treat the cost function as a Hamiltonian on spin degrees of freedom and simulate the relaxation of the system to a low-energy configuration using local update rules on the spins. Whereas the emphasis in Hastings' work was on theoretical worst-case analysis, we here investigate the underlying dynamics of the algorithm, and find that the local tensor method closely follows discretized, imaginary-time dynamics of the system under the problem Hamiltonian. Then, we study practical performance through benchmarking experiments on instances of the MaxCut problem. Through heuristic arguments we propose formulas for choosing the hyperparameters of the algorithm which are found to be in good agreement with the optimal choices determined from experiment. We observe that the local tensor method is closely related to gradient descent on a relaxation of MaxCut to continuous variables but consistently outperforms gradient descent in all instances tested. We find that time to solution achieved by the local tensor method is highly uncorrelated with that achieved by a widely used commercial optimization package; on some MaxCut instances the local tensor method beats the commercial solver in time to solution by up to two orders of magnitude and vice versa.

---

##### Citation

Bapat, A., & Jordan, S. P. (2021). "Approximate optimization of the MaxCut problem with a local spin algorithm". *Physical Review A, 103(5), 052413*.

```BibTeX
@article{bapat2021approximate,
  title={Approximate optimization of the MaxCut problem with a local spin algorithm},
  author={Bapat, Aniruddha and Jordan, Stephen P},
  journal={Physical Review A},
  volume={103},
  number={5},
  pages={052413},
  year={2021},
  publisher={APS}
}
```

---

##### Related material

+ [Presentation slides](/papers/localtensor/presentation.pptx)