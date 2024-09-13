+++
template = "index.html"
+++

The Foundations of Languages and Machines Lab at MIT is led by [Rachit Nigam][rachit]. We build new programming languages, compilers, and tools to design fast hardware quickly and correctly.
We have a strong emphasis on building real tools, getting them used by industrial collaborators, and engaging with the process of building correct and high-performance hardware ourselves.

> **We are looking for new students to join our lab starting in Fall '25!** Please read the [specific instructions][prospective] before reaching out.

## Projects

### Rethinking Hardware Description Languages
Hardware description languages (HDLs) provide low-level control allowing precise specification of circuits.
This precision comes at both a productivity and correctness cost; circuits must be defined using low-level abstractions of gates, wires, and clock cycles and require tedious, complex, and expensive tools to be verified correct.
How can we design new HDLs that provide strong correctness guarantees at compile-time *without* compromising on the efficiency of the circuits?

### Automatic Hardware Generation
Automatic hardware generation promises rapid creation of hardware designs from high-level descriptions.
However, existing tools provide limited expressive power, have unpredictable programming models, and are plagued with bugs.
How can we design new, high-level programming models for hardware generation that can describe classic micro-architectural optimizations (like speculation, out-of-order processing, multi-threading), express a wide variety of computational problems, and generate high-performance and correct circuits?


### Large Scale Heterogeneous Systems
Field Programmable Gate Arrays (FPGAs) have seen wide adoption as plug-and-play accelerators for various domains: networking, machine learning, language runtimes.
How can we design large-scale FPGA-based systems that can utilize multi-node setups, integrate which existing distributing computing frameworks, and provide a straightforward end-user programming model?

[rachit]: https://rachit.pl
[prospective]: @/lab/prospective.md