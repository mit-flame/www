+++
title = "Challenge Problems"
+++

If you're an undergraduate or M.Eng. student at MIT interested in joining the
lab, here are some challenge problems.
The goal for these exercises is to give you a flavor the kind of work we do in
the lab and see if there is a technical fit.
Given this, we recommend that *you avoid using an LLM* to solve these problems.
If you do not have experience with these domains but are excited to learn
about them and want to use an LLM in the learning process, we recommend using
[this AGENTS.md file][agents].


## Matrix Multiplier in Calyx

[Calyx][] is a compiler infrastructure for hardware generation; think of it as
"LLVM for hardware generation". It provides a both software-like control flow
operations and hardware-like structural operations to describe efficient
circuits.

For this challenge problem, you will implement matrix multiplication unit in
Calyx.

**Preliminary.** Learn about Calyx and implement a basic design in it.
- (Optional) Read the [Calyx paper][].
- [Setup Calyx and follow the tutorial](https://docs.calyxir.org).
- Implement a matrix multiplier in Calyx and test it for correctness by writing
  a test harness.
    - You can select whatever algorithm for this you'd like but we'd recommend
    starting with basic, triply-nested `while` loops.
    - You should write a JSON test file, in the same way the tutorial does, and
      make it work with your implementation.
    - If you run into problems, the documentation page on [debugging Calyx would
      be helpful][calyx-debug]!

> You are likely going to run into problems when doing this, especially when installing
things.
Please open an [issue in the Calyx repository][calyx-issue] or ask a question
the [Calyx Zulip server][calyx-zulip]!

**Stretch Goal.** If you are a UROP applying to the lab, you can consider these optional!
If you are an M.Eng. student, you should attempt do at least one challenge problem.
Doing more problems gives us a better understanding of your skills and would help us match you to a project in the lab!
- *Latency optimization.* The test harness reports a cycle count.
  Optimize the design to reduce the cycle count.
  Some options (although you are welcome to try something else!)
  - Use Calyx's [static abstraction][calyx-static].
  - Implement a [systolic array][sa] in Calyx
- *Frequency optimization.* The frequency of a hardware design determines how quickly the clock can tick. This information is *not provided* by the test harness.
  - Install and use [AMD's Vivado tool][vivado] (using the free HLPack version) to get frequency numbers for your Calyx design.
  - Implement one optimization that improves the baseline frequency of the design.
- Implement a pass using the Calyx infrastructure improves *some* performance metric: the number of resources a design uses, its latency, or its frequency.
  - The [pass tutorial][pass] provides and overview on how to implement new passes in Calyx.
- Anything else you think might be cool!

## Optimizing Mandelbrot

Optimize a CPU implementation of Mandelbrot set generation using SIMD
programming.
Use [lab 1][xcel-compute-1] from the [accelerated computing
course][xcel-compute] as your starting point and optimize the `mandelbrot.cpp`
file.

**Baseline.** As a baseline result, we are able to get about a 10x improvement
on an Apple M4 Air using just the ARM Neon SIMD instructions.
Attempt to get your optimized implementation in that range.

**Challenge.**
Use other parallelism techniques such as multi-threading to optimize your
design even more.
The base image in the starter code is too small to see results with these
techniques so we recommend bumping the image size and the number of iterations
for each point.


After finishing up an exercise, please reach out to
[Rachit](mailto:rnigam@mit.edu)!

[Calyx paper]: https://people.csail.mit.edu/rachit/files/pubs/calyx.pdf
[calyx-static]: https://people.csail.mit.edu/rachit/files/pubs/piezo.pdf
[vivado]: https://www.amd.com/en/products/software/adaptive-socs-and-fpgas/vivado.html
[sa]: https://www.eecs.harvard.edu/~htk/publication/1982-kung-why-systolic-architecture.pdf
[pass]: https://docs.calyxir.org/new-pass.html
[calyx-zulip]: https://calyx.zulipchat.com/
[Calyx]: https://calyxir.org
[calyx-issue]: https://github.com/calyxir/calyx/issues
[calyx-debug]: https://docs.calyxir.org/debug/index.html
[agents]: https://gist.github.com/1cg/a6c6f2276a1fe5ee172282580a44a7ac
[xcel-compute]: https://accelerated-computing.academy/fall25/
[xcel-compute-1]: https://accelerated-computing.academy/fall25/labs/lab1/
