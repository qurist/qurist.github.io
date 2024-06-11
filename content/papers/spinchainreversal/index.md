---
title: Nearly optimal time-independent reversal of a spin chain
date: 2022-02-22
url: /papers/spinchainreversal/
tags: ["quantum computation", "publication", "quantum architectures", "quantum entanglement"]
author: [<a href="/">Aniruddha Bapat</a>, Eddie Schoute, Alexey V Gorshkov, Andrew M Childs]
summary: We propose a time-independent Hamiltonian protocol for the reversal of qubit ordering in a chain of $N$ spins.  
cover:
    image: "/papers/spinchainreversal/icon.png"
    alt: ""
    relative: true
    hidden: true
editPost:
    URL: 10.1103/PhysRevResearch.4.L012023
citation: Bapat, A., Schoute, E., Gorshkov, A. V., & Childs, A. M. (2022). "Nearly optimal time-independent reversal of a spin chain". *Physical Review Research, 4(1), L012023*.

---


---

##### Download

- [Paper](/papers/spinchainreversal/paper.pdf)

---

##### Abstract

We propose a time-independent Hamiltonian protocol for the reversal of qubit ordering in a chain of $N$ spins.
Our protocol has an easily implementable nearest-neighbor, transverse-field Ising model Hamiltonian with timeindependent,
nonuniform couplings. Under appropriate normalization, we implement this state reversal three
times faster than a naive approach using SWAP gates, in time comparable to a protocol of Raussendorf [[Phys.
Rev. A 72, 052301 (2005)](https://journals.aps.org/pra/abstract/10.1103/PhysRevA.72.052301)] that requires dynamical control. We also prove lower bounds on state reversal by
using results on the entanglement capacity of Hamiltonians and show that we are within a factor $1.502(1 + 1/N)$
of the shortest time possible. Our lower bound holds for all nearest-neighbor qubit protocols with arbitrary
finite ancilla spaces and local operations and classical communication. We give numerical evidence that the
fast reversal protocols are more robust to noise than a SWAP-based reversal. Finally, we extend our protocol to
an infinite family of nearest-neighbor, time-independent Hamiltonian protocols for state reversal. This includes
chains with nearly uniform coupling that may be especially feasible for experimental implementation.

---

##### Citation

Bapat, A., Schoute, E., Gorshkov, A. V., & Childs, A. M. (2022). "Nearly optimal time-independent reversal of a spin chain". *Physical Review Research, 4(1), L012023*.

```BibTeX
@article{bapat2022nearly,
  title={Nearly optimal time-independent reversal of a spin chain},
  author={Bapat, Aniruddha and Schoute, Eddie and Gorshkov, Alexey V and Childs, Andrew M},
  journal={Physical Review Research},
  volume={4},
  number={1},
  pages={L012023},
  year={2022},
  publisher={APS}
}
```

---

##### Related material

+ [Supplementary material](/papers/spinchainreversal/supplement.pdf)

##### See also

+ [Patent](/papers/scrpatent)
+ [Follow-up work](/papers/fastreversals). 