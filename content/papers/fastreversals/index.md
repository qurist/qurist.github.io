---
title: Quantum routing with fast reversals 
date: 2021-08-31
url: /papers/fastreversals/
tags: ["quantum computation", "publication", "quantum architectures", "algorithms", "quantum routing"]
author: [<a href="/">Aniruddha Bapat</a>, Andrew M Childs, Alexey V Gorshkov, Samuel King, Eddie Schoute, Hrishee Shastri]
summary: We present methods for implementing arbitrary permutations of qubits under interaction constraints.  
editPost:
    URL: 10.22331/q-2021-08-31-533
citation: Bapat, A., Childs, A. M., Gorshkov, A. V., King, S., Schoute, E., & Shastri, H. (2021). "Quantum routing with fast reversals". *Quantum, 5, 533*.

---


---

##### Download

- [Paper](/papers/fastreversals/paper.pdf)

---

##### Abstract

We present methods for implementing arbitrary permutations of qubits 
under interaction constraints. Our protocols make use of previous methods for rapidly reversing the order of qubits along a path.
Given nearest-neighbor interactions on a path of length $n$,
we show that there exists a constant $\epsilon \approx 0.034$ such that the quantum routing time
is at most $(1-\epsilon)n$,
whereas any SWAP-based protocol needs at least time $n-1$.
This represents the first known quantum advantage over SWAP-based routing methods
and also gives improved quantum routing times for realistic architectures such as grids.
Furthermore, we show that our algorithm approaches a quantum routing time of $2n/3$ in expectation for uniformly random permutations,
whereas \swap{}-based protocols require time $n$ asymptotically.
Additionally, we consider sparse permutations that route $k \le n$ qubits
and give algorithms with quantum routing time at most $n/3 + O(k^2)$ on paths and at most 
$2r/3 + O(k^2)$ on general graphs with radius $r$.


---

##### Citation

Bapat, A., Childs, A. M., Gorshkov, A. V., King, S., Schoute, E., & Shastri, H. (2021). "Quantum routing with fast reversals". *Quantum, 5, 533*.

```BibTeX
@article{bapat2021quantum,
  title={Quantum routing with fast reversals},
  author={Bapat, Aniruddha and Childs, Andrew M and Gorshkov, Alexey V and King, Samuel and Schoute, Eddie and Shastri, Hrishee},
  journal={Quantum},
  volume={5},
  pages={533},
  year={2021},
  publisher={Verein zur F{\"o}rderung des Open Access Publizierens in den Quantenwissenschaften}
}
```

---

##### Related material

+ [Recorded talk](https://www.youtube.com/watch?v=e-1rk_QFiCg), presented by Eddie Schoute at PLanQC'21.
+ [Presentation slides](/papers/fastreversals/presentation.pdf)

---

##### See also
+ This paper is a follow-up to our earlier work on [reversing a spin chain](/papers/spinchainreversal).
+ [Patent](/papers/frpatent).