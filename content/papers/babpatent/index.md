---
title: Performing bang-anneal-bang quantum optimization
date: 2022-11-17
url: /papers/babpatent/
tags: ["quantum computation", "publication", "optimal control"]
author: [Lucas T Brady, Christopher L Baldwin, <a href="/">Aniruddha Bapat</a>, Yaroslav Kharkov, Alexey V Gorshkov]
summary: we carry out simulations of optimal control protocols for energy minimization on various transverse field Ising models, demonstrating that optimal protocols typically exhibit a bang-anneal-bang pattern.  
cover:
    image: "/papers/babpatent/icon.png"
    alt: ""
    relative: true
editPost:
    URL: <a href="https://patentscope.wipo.int/search/en/detail.jsf?docId=WO2022241146"> Link <\a>
citation: Brady, L. T., Baldwin, C. L., Bapat, A., Kharkov, Y., & Gorshkov, A. V. (2021). "Performing bang-anneal-bang quantum optimization". *US Patent No. WO2022241146A1*.

---


---

##### Download

- [Initial publication](/papers/babpatent/paper.pdf)

---

##### Abstract

A process for bang-anneal-bang quantum optimization includes: identifying base curve $v(t)$; setting a total runtime of the process; creating an initial guess for parameters in an ansatz; creating an initial guess for parameters in an ansatz; evolving a quantum state from a ground state of B following Hamiltonian $H(t) = u(t) B+(1-u(t)) C$ and, at termination of evolving the quantum state, measuring the resulting quantum state; updating the parameters for the ansatz based on the resulting quantum state; repetitively creating the ansatz for $u(t)$, evolving the quantum state from the ground state of $B$ following Hamiltonian $H(t)$, and, at termination of evolving the quantum state, determining the resulting quantum state until the classical outer loop converges to a selected convergence limit; and returning the final form of $u(t)$ to perform bang-anneal-bang quantum optimization.

---

##### Citation

Brady, L. T., Baldwin, C. L., Bapat, A., Kharkov, Y., & Gorshkov, A. V. (2021). "Performing bang-anneal-bang quantum optimization". *US Patent No. WO2022241146A1*.

```BibTeX
  @misc{brady2022performing,
  title={Performing bang-anneal-bang quantum optimization},
  author={Brady, Lucas Tyler and Gorshkov, Alexey Vyacheslavovich and Baldwin, Christopher Lee and \textbf{AB} and Kharkov, Yaroslav and Bienias, Przemyslaw Dariusz and Kocia, Lucas},
  year={2022},
  note={WO 2022/241146A1}
}
```

---

##### See also

+ [Paper: Bang-anneal-bang](/papers/bangannealbang/)
+ [Paper: Behavior of analog algorithms](/papers/analogalgorithms/)