---
title: Bang-bang control as a design principle for classical and quantum optimization algorithms 
date: 2018-12-6
url: /papers/bangbang/
tags: ["quantum computation", "publication", "optimal control"]
author: [<a href="/">Aniruddha Bapat</a>, Stephen Jordan]
summary: We study the performance of several variational quantum optimization algorithms on two toy constraint satisfaction problem instances, and argue that the type of control strategy can be crucial to success.
cover:
    image: "/papers/bangbang/icon.png"
    alt: "The ramp-with-spike problem instance"
    relative: true
editPost:
    URL: 10.4230/LIPIcs.TQC.2014.161
citation: Bapat, A., & Jordan, S. (2019). "Bang-bang control as a design principle for classical and quantum optimization algorithms". *Quantum Information & Computation, 19(5-6), 424-446*.

---


---

##### Download

- [Paper](/papers/bangbang/paper.pdf)

---

##### Abstract

Physically motivated classical heuristic optimization algorithms such as simulated annealing (SA) treat the objective function as an energy landscape, and allow walkers to escape local minima. It has been argued that quantum properties such as tunneling may give quantum algorithms advantage in finding ground states of vast, rugged cost landscapes. Indeed, the Quantum Adiabatic Algorithm (QAO) and the recent Quantum Approximate Optimization Algorithm (QAOA) have shown promising results on various problem instances that are considered classically hard. Here, building on previous observations, we argue that the type of control strategy used by the optimization algorithm may be crucial to its success. Along with SA, QAO, and QAOA, we define a new, bang-bang version of simulated annealing, BBSA, and study the performance of these algorithms on two well-studied problem instances from the literature. Both classically and quantumly, the successful control strategy is found to be bang-bang, exponentially outperforming the quasistatic analogues on the same instances. Lastly, we construct O(1)-depth QAOA protocols for a class of symmetric cost functions, and provide an accompanying physical picture.

---

##### Citation

Bapat, A., & Jordan, S. (2019). "Bang-bang control as a design principle for classical and quantum optimization algorithms". *Quantum Information & Computation, 19(5-6), 424-446*.

```BibTeX
  @article{bapat2019bang,
  title={Bang-bang control as a design principle for classical and quantum optimization algorithms},
  author={Bapat, Aniruddha and Jordan, Stephen},
  journal={Quantum Information \& Computation},
  volume={19},
  number={5-6},
  pages={424--446},
  year={2019},
  publisher={Rinton Press, Incorporated Paramus, NJ}
}
```

---

##### Related material

+ [Talk slides](/papers/bangbang/presentation.pdf)