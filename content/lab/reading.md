+++
title = "Reading List"
+++

The following is an opinionated list of important papers that cut across programming languages, architecture, and compilers research.
The papers might not always be the best place to learn the modern incarnation of ideas that they describe but are worth reading and understanding once you are able to grok the idea from other sources.
If you would like to add a paper, please [open a pull request][flame-www].


## Specialization Era
These readings provide a good overview of what motivates the need for specialized accelerators.
Most papers that design and describe accelerators will take arguments presented in these papers as implicit axioms: for example, when a paper trades-off generality for efficiency, the argument is justified because they getting both is no longer possible.

* **Computing's Energy Problem.**
A classic Mark Horowitz paper that describes the fundamental energy limitations of general purpose processors: most of the energy (time, area, etc.) of a general-purpose processor is spent on *deciding* what computation to perform instead of performing it.

* **Understanding Sources of Inefficiency in General-Purpose Chips.**
A follow-on to the previous paper that systematically studies the impact of architectural optimizations to a general-purpose processors.

* **Designing and Modeling of Specialized Architectures (§1-2).**
The first two chapters of Sophia Shao's dissertation provide a pretty great introduction to the history of physical scaling laws and why their demise implies a need for specialized architectures.

## Programming Languages

* **An Axiomatic Basis for Computer Programs.** Tony Hoare's paper introducing Hoare triples which are used to verify and specify a program's post-conditions given some pre-conditions. Hoare triples have been instantiated with various different *program logics* to reason about different kinds of properties: functional correctness, concurrent behavior, termination, etc.

* **A Syntactic Approach to Type Soundness.** Wright and Felleisen's paper that defined the modern, syntactic approach to proving the soundness of type systems through the dual properties of progress and preservation ([this paper][logical-approach] mentions that the specific formulation is due to Harper.) This the currently *the* standard way of presenting the soundness of a type system although there is a movement towards different, semantic notions of type soundness that are becoming more popular.

## Compilers

* **A Catalogue of Optimizing Tranformations.** A Francis Allen paper that collated various compiler optimizations being developed in the compilers community in the 70s. Some of the names for optimizations are archaic but the optimizations are a staple in any modern optimizing compiler.

* **Superoptimization: A Look at the Smallest Program.** Alexia Massalin's paper defining the concept of *superoptimizer*: an optimizer that attempts to find an *optimal* sequence of instructions to perform some computation. The paper spurred a whole subarea of compilers research and is a direct ancestor of tools like STOKE.

## Distributed Systems

* **Time, Clocks, and the Ordering of Events in a Distributed System.** Leslie Lamport's short but beautiful paper defining the notion of causal ordering in distributed systems as a mechanism. The definition of *logical clocks* is used to eventually define classic concepts like *vector clocks* in future papers. Keep an eye out for the citation to Einstein's paper on generality relativity in this one!


[flame-www]: https://github.com/mit-flame/www
[logical-approach]: https://dl.acm.org/doi/10.1145/3676954#body-ref-fn1
