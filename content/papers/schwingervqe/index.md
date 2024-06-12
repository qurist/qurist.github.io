---
title: Quench dynamics of the Schwinger model via variational quantum algorithms
date: 2023-08-02
url: /papers/schwingervqe/
tags: ["quantum computation", "publication", "variational quantum algorithms", "high-energy physics"]
author: [Lento Nagano, <a href="/">Aniruddha Bapat</a>, Christian Bauer]
summary: We investigate the real-time dynamics of the $(1+1)$-dimensional $U(1)$ gauge theory known as the Schwinger model via variational quantum algorithms.  
# cover:
#     image: "/papers/schwingervqe/icon.png"
#     alt: "A braid group element"
#     relative: true
editPost:
    URL: 10.1103/PhysRevD.108.034501
citation: Nagano, L., Bapat, A., & Bauer, C. W. (2023). "Quench dynamics of the Schwinger model via variational quantum algorithms". *Physical Review D, 108(3), 034501*.
---


---

##### Download

- [Paper](/papers/schwingervqe/paper.pdf)

---

##### Abstract

We investigate the real-time dynamics of the $(1 + 1)$-dimensional $U(1)$ gauge theory known as the Schwinger model via variational quantum algorithms. Specifically, we simulate quench dynamics in the presence of an external electric field. First, we use a variational quantum eigensolver to obtain the ground state of the system in the absence of an external field. With this as the initial state, we perform real-time evolution under an external field via a fixed-depth, parameterized circuit whose parameters are updated using McLachlan’s variational principle. We use the same ansatz for initial-state preparation and time evolution, by which we are able to reduce the overall circuit depth. We test our method with a classical simulator and confirm that the results agree well with exact diagonalization.

---

##### Citation

Nagano, L., Bapat, A., & Bauer, C. W. (2023). "Quench dynamics of the Schwinger model via variational quantum algorithms". *Physical Review D, 108(3), 034501*.

```BibTeX
@article{nagano2023quench,
  title={Quench dynamics of the Schwinger model via variational quantum algorithms},
  author={Nagano, Lento and Bapat, Aniruddha and Bauer, Christian W},
  journal={Physical Review D},
  volume={108},
  number={3},
  pages={034501},
  year={2023},
  publisher={APS}
}
```

---

<!-- ##### Related material

+ [Presentation slides](/papers/schwingervqe/presentation.pdf) -->