---
layout: post
title: Compiler Infrastructure and Optimization Implementations in Java
---

[Click for more details about the project](https://github.com/rohankalbag/compiler-design)

*This repository presents implementations of various compiler optimizations and infrastructure for MiniJava, a Java subset, using JavaCC and JTB. The projects include a type checker, function inliner with Rapid Type Analysis, a register allocator utilizing Kempe's graph coloring heuristic, and a for-loop parallelization employing the GCD test. Each implementation is accompanied by a detailed problem specification. For the Type Checker project, a Java-like object-oriented language is type-checked using a provided grammar file, and detailed error reporting is implemented. The Function Inliner focuses on determining inlineability based on RTA and transforming method calls. Register Allocation involves spilling variables to memory using liveness analysis results. Loop Parallelization utilizes the GCD test to identify parallelizable for-loops in methods, marked with the `/* @Parallel */` decorator.*
