---
title: Behavior of analog algorithms
date: 2021-07-02
url: /papers/analogalgorithms/
tags: ["quantum computation", "publication", "optimal control", "quantum optimization"]
author: [Lucas T. Brady, Lucas Kocia, Przemyslaw Bienias, <a href="/">Aniruddha Bapat</a>, Yaroslav Kharkov, Alexey V. Gorshkov]
summary: In this work, we explore connections between various "analog" quantum optimization algorithms such as QAOA and annealing, and the limits in which they become approximations of the optimal control strategy.  
cover:
    image: "/papers/analogalgorithms/icon.png"
    alt: ""
    relative: true
editPost:
    URL: https://arxiv.org/abs/2107.01218
citation: Brady, L. T., Kocia, L., Bienias, P., Bapat, A., Kharkov, Y., & Gorshkov, A. V. (2021). "Behavior of analog quantum algorithms". *arXiv preprint arXiv:2107.01218*.

---


---

##### Download

- [Paper](/papers/analogalgorithms/paper.pdf)

---

##### Abstract

Analog quantum algorithms are formulated in terms of Hamiltonians rather than unitary gates and include quantum adiabatic computing, quantum annealing, and the quantum approximate optimization algorithm (QAOA). These algorithms are promising candidates for near-term quantum applications, but they often require fine tuning via the annealing schedule or variational parameters. In this work, we explore connections between these analog algorithms, as well as limits in which they become approximations of the optimal procedure.Notably, we explore how the optimal procedure approaches a smooth adiabatic procedure but with a superposed oscillatory pattern that can be explained in terms of the interactions between the ground state and first excited state that effect the coherent error cancellation of diabatic transitions. Furthermore, we provide numeric and analytic evidence that QAOA emulates this optimal procedure with the length of each QAOA layer equal to the period of the oscillatory pattern. Additionally, the ratios of the QAOA bangs are determined by the smooth, non-oscillatory part of the optimal procedure. We provide arguments for these phenomena in terms of the product formula expansion of the optimal procedure. With these arguments, we conclude that different analog algorithms can emulate the optimal protocol under different limits and approximations. Finally, we present a new algorithm for better approximating the optimal protocol using the analytic and numeric insights from the rest of the paper. In practice, numerically, we find that this algorithm outperforms standard QAOA and naive quantum annealing procedures.

---

##### Citation

Brady, L. T., Kocia, L., Bienias, P., Bapat, A., Kharkov, Y., & Gorshkov, A. V. (2021). "Behavior of analog quantum algorithms". *arXiv preprint arXiv:2107.01218*.

```BibTeX
@article{brady2021behavior,
  title={Behavior of analog quantum algorithms},
  author={Brady, Lucas T and Kocia, Lucas and Bienias, Przemyslaw and Bapat, Aniruddha and Kharkov, Yaroslav and Gorshkov, Alexey V},
  journal={arXiv preprint arXiv:2107.01218},
  year={2021}
}
```

---

##### Awards

+ This paper won the [2021 Applied NISQ Computing Paper award](https://riacs.usra.edu/quantum/ANISQCAward).

---

##### See also

+ [Patent](/papers/babpatent/)
