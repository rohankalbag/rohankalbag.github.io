---
layout: post
title: Formal Verification and Test Generation for Ripple Carry Adder Implementation
---

[Click to access source files](https://github.com/rohankalbag/ee709-iitb)


*This project conducts the formal verification of a given Ripple Carry Adder (RCA) implementation. Binary Decision Diagrams (BDDs) were employed using `bddlib` to represent the provided RTL description of the adder circuit. Additionally, BDD operations, including Image and Pre-Image, were implemented natively in C++ to rigorously prove critical properties such as Goldberg's Conjecture, ensuring the correctness of the adder's design implementation. Furthermore, SAT solvers were used to construct the smallest spanning test-vector set for post-fabrication physical design testing, thereby enhancing the circuit's reliability and robustness.*
