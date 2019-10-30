# Guide to Systems Programming @ Umich
## What is systems programming?
> [Systems Programming](https://en.wikipedia.org/wiki/Systems_programming), or system programming, is the activity of programming computer system software. The primary distinguishing characteristic of systems programming when compared to application programming is that application programming aims to produce software which provides services to the user directly (e.g. word processor), whereas systems programming aims to produce software and software platforms which provide services to other software, are performance constrained, or both (e.g. operating systems, computational science applications, game engines, industrial automation, and software as a service applications).
>
> Systems programming requires a great degree of hardware awareness. Its goal is to achieve efficient use of available resources, either because the software itself is performance critical or because even small efficiency improvements directly transform into significant monetary savings for the service provider (cloud based word processors).

**tl;dr**: Programming where the execution environment is resource constrained (latency, throughput, memory, disk, bandwidth, etc.) and relied upon for correctness and security by other systems or developers. Typically, knowledge of the hardware and use of systems programming languages (C, C++, Rust, etc.) is necessary to achieve acceptable levels of performance and security. 

## What are some areas of software that fit into systems programming?
Definitions may vary depending on who you ask. The following are considered to be systems programming areas of development, some more so than others:
- Operating systems
- Kernels
- Firmware
- Embedded
- Device drivers
- Hypervisors
- Network stacks
- Simulations and games
- Servers
- Foundational libraries
  - Esp. threading, data structures, networking, linear algebra, etc. where high performance is expected and hardware available may influence choices. 
- Programming languages and runtimes
- Databases
- Many more!

## What should I know to get into systems programming?
1. (281) You should have a strong foundation in data structures and algorithms, their implementations, and how choices about implementation and usage can affect scalability and performance in various resources (especially time and space if just starting out). Should be comfortable with efficient usage and implementation tradeoffs of strings, arrays/vectors, linked lists, balanced binary search trees, hash tables, binary heaps, sorting algorithms, binary search, and similar. 

2. (370) You should be familiar with the basic Von Neumann architecture, and the modern model of compilation, assembling, and linking. You should be able to recognize the typical memory layout of a process in memory on Linux (stack, heap, text segment, data segment, etc.). You should be able to reason about the lifecycle of an instruction as it executes on a processor, pipelined execution, memory hierarchies (registers, caching, virtual memory, and disk access/paging, and the order of magnitude slowdown as you move down the hierarchy), and branch prediction, and have basic familiarity with a subset of ARM or another ISA, and be able to explain why there are different ISAs and processors for different use cases, and what the idea of endianness entails for portable programs. It would also be good to be familiar with some basic compiler optimizations and dependencies between instructions as they execute on a processor. You should now have some intuition about how all these hardware details might affect the runtime of a program (which may be wrong upon measurement, but is at least a good place to start). 

3. (281 + 370 + on your own) You should develop a strong understanding of the semantics of C, C++ and/or Rust, or some other similar language capable of running on bare metal. All three are very different and have different levels of complexity, but all get at the same idea: that the abstract machine and semantics of a programming language do not always map directly to hardware semantics, and this can lead to bugs and security issues around undefined behaviour, and has subtle implications for programs. You should also get a sense that sometimes the model/language/tooling allows for platform-specific behaviour, and that this can be necessary to gain back some hardware access and performance in some cases. (Personally I recommend learning the C memory model and semantics first because of its relative simplicity compared to C++ and Rust, followed by the Rust ownership/referencing model for its strictness and general applicability to correct C and C++ programs.) You should be able to recognize common memory safety issues like dangling pointers/references, double-frees, and out of bounds accesses/segmentation faults and know how to diagnose them in a program. Sanitizers, tools like `valgrind`, and compilers (especially Rust's) are all great at finding these issues in programs and can help get a sense of how to spot them and prevent them. 

4. (281) You should be able to profile short programs using tools like `perf` and `valgrind` to discern where runtime and memory resources are being consumed, and learn to trust tools over intuition when dealing with performance and resource usage. 
