---
title: Advantages and limitations of quantum routing 
date: 2023-02-01
url: /papers/quantumrouting/
tags: ["quantum computation", "publication", "quantum routing", "algorithms", "quantum entanglement", "quantum architectures"]
author: [<a href="/">Aniruddha Bapat</a>, Andrew M Childs, Alexey V Gorshkov, Eddie Schoute]
summary: We lower bound the circuit depth or time required for quantum routing in terms of spectral properties of graphs representing the architecture interaction constraints, and give a generalized upper bound for all simple connected $n$-vertex graphs.  
# cover:
#     image: "/papers/quantumrouting/icon.png"
#     alt: ""
#     relative: true
editPost:
    URL: 10.1103/PRXQuantum.4.010313
citation: Bapat, A., Childs, A. M., Gorshkov, A. V., & Schoute, E. (2023). "Advantages and limitations of quantum routing". *PRX Quantum, 4(1), 010313*.

---


---

##### Download

- [Paper](/papers/quantumrouting/paper.pdf)

---

##### Abstract

The SWAP gate is a ubiquitous tool for moving information on quantum hardware, yet it can be considered a classical operation because it does not entangle product states. Genuinely quantum operations could outperform SWAP for the task of permuting qubits within an architecture, which we call routing. We consider quantum routing in two models: (i) allowing arbitrary two-qubit unitaries, or (ii) allowing Hamil- tonians with norm-bounded interactions. We lower bound the circuit depth or time of quantum routing in terms of spectral properties of graphs representing the architecture interaction constraints, and give a generalized upper bound for all simple connected $n$-vertex graphs. In particular, we give conditions for a superpolynomial classical-quantum routing separation, which exclude graphs with a small spectral gap and graphs of bounded degree. Finally, we provide examples of a quadratic separation between gate-based and Hamiltonian routing models with a constant number of local ancillas per qubit and of an  $\Omega(n)$ speedup if we also allow fast local interactions.

---

##### Citation

Bapat, A., Childs, A. M., Gorshkov, A. V., & Schoute, E. (2023). "Advantages and limitations of quantum routing". *PRX Quantum, 4(1), 010313*.

```BibTeX
@article{bapat2023advantages,
  title={Advantages and limitations of quantum routing},
  author={Bapat, Aniruddha and Childs, Andrew M and Gorshkov, Alexey V and Schoute, Eddie},
  journal={PRX Quantum},
  volume={4},
  number={1},
  pages={010313},
  year={2023},
  publisher={APS}
}
```

---

<!-- ##### Related material

+ [Presentation slides](/papers/quantumrouting/presentation.pdf) -->

##### See also

+ [Follow up work](/papers/teleportationrouting)