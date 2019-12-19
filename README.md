# Guide to Systems Programming
## What is systems programming?
> [Systems Programming](https://en.wikipedia.org/wiki/Systems_programming), or system programming, is the activity of programming computer system software. The primary distinguishing characteristic of systems programming when compared to application programming is that application programming aims to produce software which provides services to the user directly (e.g. word processor), whereas systems programming aims to produce software and software platforms which provide services to other software, are performance constrained, or both (e.g. operating systems, computational science applications, game engines, industrial automation, and software as a service applications).
>
> Systems programming requires a great degree of hardware awareness. Its goal is to achieve efficient use of available resources, either because the software itself is performance critical or because even small efficiency improvements directly transform into significant monetary savings for the service provider (cloud based word processors).

**tl;dr**: Programming where the execution environment is resource constrained (latency, throughput, memory, disk, bandwidth, etc.) and relied upon for correctness and security by other systems or developers. Typically, knowledge of the hardware and use of systems programming languages (C, C++, Rust, etc.) is necessary to achieve acceptable levels of performance and security. 

## How can I contribute to this guide?
Is something unclear? Want to expand on something or make a change? This guide is open source! Make an issue or a PR and we can all refine this together. 

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
The following bits correspond to my experiences in courses at University of Michigan, with course numbers provided for reference, but they can all be learned at other universities or independently. 
1. (281) You should have a strong foundation in data structures and algorithms, their implementations, and how choices about implementation and usage can affect scalability and performance in various resources (especially time and space if just starting out). Should be comfortable with efficient usage and implementation tradeoffs of strings, arrays/vectors, linked lists, balanced binary search trees (B-trees, AVL, etc.), hash tables (probing and chaining), binary heaps, sorting algorithms, binary search, and similar. 

2. (370) You should be familiar with the basic Von Neumann architecture, and the modern model of compilation, assembling, and linking. You should be able to recognize the typical memory layout of a process in memory on Linux (stack, heap, text segment, data segment, etc.). You should be able to reason about the lifecycle of an instruction as it executes on a processor, pipelined execution, memory hierarchies (registers, caching, virtual memory, and disk access/paging, and the order of magnitude slowdown as you move down the hierarchy), and branch prediction, and have basic familiarity with a subset of ARM or another ISA, and be able to explain why there are different ISAs and processors for different use cases, and what the idea of endianness entails for portable programs. It would also be good to be familiar with some basic compiler optimizations and dependencies between instructions as they execute on a processor. You should now have some intuition about how all these hardware details might affect the runtime of a program (which may be wrong upon measurement, but is at least a good place to start). 

3. (281 + 370 + on your own) You should develop a strong understanding of the semantics of C, C++ and/or Rust, or some other similar language capable of running on bare metal. All three are very different and have different levels of complexity, but all get at the same idea: that the abstract machine and semantics of a programming language do not always map directly to hardware semantics, and this can lead to bugs and security issues around undefined behaviour, and has subtle implications for programs. You should also get a sense that sometimes the model/language/tooling allows for platform-specific behaviour, and that this can be necessary to gain back some hardware access and performance in some cases. (Personally I recommend learning the C memory model and semantics first because of its relative simplicity compared to C++ and Rust, followed by the Rust ownership/referencing model for its strictness and general applicability to correct C and C++ programs.) You should be able to recognize common memory safety issues like dangling pointers/references, double-frees, and out of bounds accesses/segmentation faults and know how to diagnose them in a program. Sanitizers, tools like `valgrind`, and compilers (especially Rust's) are all great at finding these issues in programs and can help get a sense of how to spot them and prevent them. 

4. (281) You should be able to profile short programs using tools like `perf` and `valgrind` to discern where runtime and memory resources are being consumed, and learn to trust tools over intuition when dealing with performance and resource usage. 

5. (388) You should develop a strong security-concious mindset, and a healthy sense of skepticism around the security of software (and hardware) in general. You should know that all complex systems have vulnerabilities, and that an attacker must be assumed to have full knowledge of an implementation (only keys are secure). In high risk environments, software systems often can't trust each other, themselves, or even the hardware they are running on, so there are tradeoffs to be made around what mitigations are worth implementing and what is not part of a threat model. You should be comfortable with application security issues like buffer overflows, mitigations like ASLR, stack canaries, write xor execute and other memory protections, and counter-attack techniques like NOP-sledding, return to libc, and ROP. You should know the layout of a stack frame and how a buffer overread or overwrite might leak information or allow arbitrary control of execution. You should also be comfortable with network security issues and with how an attacker can compromise systems and move through a network. Finally, you should be aware of recent hardware security issues like Spectre/Meltdown, Rowhammer, timing attacks, and information leakage over airgaps through things like heat, fan noise, coil whine, etc. 

6. (398) You should get a sense of what it's like to work in a team over an extended period on a single growing project, and how to communicate effectively and work under self-imposed and team-imposed deadlines. You should develop a good sense of how to deal with large systems design issues, shared state, and scalability. You should learn that multithreading and correct sychronization are very difficult, and that properly synchronizing data can have impacts on performance due to contention. You should take away a healthy skepticism of the correctness of programs, and a preference for systems that minimize shared state, and especially shared mutable state, to reduce bugs and contention, and increase scalability. This is doubly true with systems that interact over the network, where latency and inconsistency create even more opportunities for bugs and poor performance due to excessive communication. Ideally, a system should keep processing tasks as isolated as possible for maximum parallelism, scalability, distributability, and correctness (see map-reduce and related ideas). You should also realize by now that a large-scale system should have a solid design before implementation begins, and that systems of any scale will have unintended behavior and ballooning complexity without attention to design from the start.

7. To be written: (multithreading and synchronization, virtual memory, data locality, memory allocation, context switching, task scheduling and preemption, interrupts, file systems, networking, avoidance of shared mutable state, the advantages of thinking like a functional programmer, etc.)

## What are some good articles, books and talks to learn more?
### Operating Systems
- [LiveOverflow "How Do Linux Kernel Drivers Work?"](https://youtu.be/juGNPLdjLH4)
- [OSDev wiki](https://wiki.osdev.org/Main_Page)
- [Philipp Oppermann "Writing an OS in Rust"](https://os.phil-opp.com)
- [Bryan Cantrill "Is It Time to Rewrite the Operating System in Rust?"](https://youtu.be/HgtRAbE1nBM)

### Security
- [LiveOverflow "Binary Exploitation / Memory Corruption](https://www.youtube.com/playlist?list=PLhixgUqwRTjxglIswKp9mpkfPNfHkzyeN)
- [Chandler Carruth “Spectre: Secrets, Side-Channels, Sandboxes, and Security”](https://youtu.be/_f7O3IfIR2k)
- [Chandler Carruth “Garbage In, Garbage Out: Arguing about Undefined Behavior..."](https://youtu.be/yG1OZ69H_-o)

### Data Oriented Design
- [Stoyan Nikolov “OOP Is Dead, Long Live Data-oriented Design”](https://youtu.be/yy8jQgmhbAU)
- [Mike Acton "Data-Oriented Design and C++"](https://youtu.be/rX0ItVEVjHc)
- [Mike Acton "Building a Data-Oriented Future"](https://youtu.be/u8B3j8rqYMw)
- [Richard Fabian "Data-Oriented Design"](http://www.dataorienteddesign.com/dodbook/)
- [Dawid Ciężarkiewicz "The faster you unlearn OOP, the better for you and your software"](https://dpc.pw/the-faster-you-unlearn-oop-the-better-for-you-and-your-software)

### Data Structures & Algorithms
- [E-Maxx "Competitive Programming Algorithms"](https://cp-algorithms.com)
- [Matt Kulukundis “Designing a Fast, Efficient, Cache-friendly Hash Table, Step by Step”](https://youtu.be/ncHmEUmJZf4)
- [Malte Skarupke "You Can Do Better than std::unordered_map"](https://youtu.be/M2fKMP47slQ)
- [Malte Skarupke "I wrote the fastest hashtable"](https://probablydance.com/2017/02/26/i-wrote-the-fastest-hashtable/)
- [Malte Skarupke "A new fast hash table in response to Google’s new fast hash table"](https://probablydance.com/2018/05/28/a-new-fast-hash-table-in-response-to-googles-new-fast-hash-table/)
- [Malte Skarupke "Fibonacci Hashing: The Optimization that the World Forgot"](https://probablydance.com/2018/06/16/fibonacci-hashing-the-optimization-that-the-world-forgot-or-a-better-alternative-to-integer-modulo/)

### Performance
- [Daniel Lemire's blog](https://lemire.me/blog/)
- [Game Programming Patterns "Data Locality"](https://gameprogrammingpatterns.com/data-locality.html)
- [Andrei Alexandrescu “Speed Is Found In The Minds of People"](https://youtu.be/FJJTYQYB1JQ)
- [Jason Turner “Practical Performance Practices"](https://youtu.be/uzF4u9KgUWI)
- [Chandler Carruth “High Performance Code 201: Hybrid Data Structures"](https://youtu.be/vElZc6zSIXM)
- [Chandler Carruth "Efficiency with Algorithms, Performance with Data Structures"](https://youtu.be/fHNmRkzxHWs)
- [Chandler Carruth “There Are No Zero-cost Abstractions”](https://youtu.be/rHIkrotSwcc)
- [Chandler Carruth “Going Nowhere Faster”](https://youtu.be/2EWejmkKlxs)
- [Chandler Carruth "Tuning C++: Benchmarks, and CPUs, and Compilers! Oh My!"](https://youtu.be/nXaxk27zwlk)
- [Andrei Alexandrescu "Optimization Tips - Mo' Hustle Mo' Problems"](https://youtu.be/Qq_WaiwzOtI)
- [Timur Doumler “Want fast C++? Know your hardware!"](https://youtu.be/BP6NxVxDQIs)
- [Joshua Liebow-Feeser "Move fast and don't break things: High-performance networking in Rust"](https://youtu.be/UfMOOxOGCmA)
- [Alan Talbot “Moving Faster: Everyday efficiency in modern C++”](https://youtu.be/EovBkh9wDnM)

### Compilers
- [Matt Godbolt “The Bits Between the Bits: How We Get to main()”](https://youtu.be/dOfucXtyEsU)
- [Matt Godbolt “What Has My Compiler Done for Me Lately? Unbolting the Compiler's Lid”](https://youtu.be/bSkpMdDe4g4)
