+++
template = "index.html"
+++

The goal of the FLAME lab is to design principled abstractions across the programming systems stack 
(languages, compilers, architectures) to enable the efficient design and use of specialized hardware.

> If you are interested in joining the lab, please review the [specific instructions][prospective] before contacting us.

## Directions

### Computer Architecture
A staggering number of new hardware accelerators have been developed to combat the end of scaling.
However, each accelerator is a unique snowflake with its own design principles, implementation methodology, and
software stack.
*Can we bring order to this heterogeneity by extracting flexible and composable ideas for architectural design?*

### Programming Languages
Riding on the wave of physical and architectural scaling, programming languages have focused on gluttonous
abstraction to enable large-scale design.
With the end of scaling, languages need to work in tandem with compilers and architectures to carefully expose
low-level control.
*Can we design new programming languages that enable low-level control without compromising on modular abstraction?*

### Compilers
The clear abstraction boundary between hardware and software provided by traditional processors is lost in the realm of
accelerators.
While this boundary has enabled the principled study and design of software compilers, its absence means that accelerator
compilation only has point solutions.
*How can we scalable and automated compilers for accelerator design and use?*




[rachit]: https://rachit.pl
[prospective]: @/lab/prospective.md
[filament]: https://filamentHDL.com
[calyx]: https://calyxir.org
[calyx-dialect]: https://circt.llvm.org/docs/Dialects/Calyx/
