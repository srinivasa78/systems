# What is systems programming?
Broadly, developing software that is:
1. Relied upon for correctness and security by other software.
2. Constrained by physical resources of its execution environments.

# What are some resources to learn about systems programming?
## General
- [Chris Leary, JF Bastien "TLB hit"](https://tlbh.it)
- [Oxide Computer Company "On The Metal"](https://oxide.computer/podcast/)

## Data Structures & Algorithms
Keywords: asymptotic complexity, array, queue, hash table, search tree, linked list, heap, sorting, binary search, backtracking, graph search, divide and conquer, memoization, string matching
- ["Open Data Structures"](https://opendatastructures.org)
- [Thomas Cormen, Charles Leiserson, Ronald Rivest, Clifford Stein "Introduction to Algorithms"](https://mitpress.mit.edu/books/introduction-algorithms-third-edition)
- [E-Maxx "Competitive Programming Algorithms"](https://cp-algorithms.com)

## Programming Languages
- [Robert Seacord "Effective C: An Introduction to Professional C Programming"](https://nostarch.com/Effective_C)
- [Cliff Biffle "Prefer Rust to C/C++ for new code."](http://cliffle.com/blog/prefer-rust/)
- [Cliff Biffle "Learn Rust the Dangerous Way"](http://cliffle.com/p/dangerust/)
- [Ginger Bill "The Fatal Flaw of Ownership Semantics"](http://www.gingerbill.org/article/2020/06/21/the-ownership-semantics-flaw/)
- [Alexis King "No, dynamic type systems are not inherently more open"](https://lexi-lambda.github.io/blog/2020/01/19/no-dynamic-type-systems-are-not-inherently-more-open/)
- [Amos (fasterthanlime) "Aiming for correctness with types"](https://fasterthanli.me/articles/aiming-for-correctness-with-types)
- [Jon Gjengset "Crust of Rust: Lifetime Annotations"](https://youtu.be/rAl-9HwD858)
- [Jon Gjengset "Crust of Rust: Subtyping and Variance"](https://youtu.be/iVYWDIW71jk)
- [Jon Gjengset "Crust of Rust: Smart Pointers and Interior Mutability"](https://youtu.be/8O0Nt9qY_vo)

## Computer Architecture
Keywords: von Neumann architecture, instruction set architecture, memory hierarchy, endianness, pipelining, branch prediction, out-of-order execution, cache coherence, trap
- [John Paul Shen, Mikko H. Lipasti "Modern Processor Design: Fundamentals of Superscalar Processors"](https://www.amazon.com/dp/B00HCLUL5O)
- [Vijay Nagarajan, Daniel Sorin, Mark Hill, David Wood "A Primer on Memory Consistency and Cache Coherence"](https://doi.org/10.2200/S00962ED2V01Y201910CAC049)
- [David A. Patterson, John L. Hennessy "Computer Organization and Design RISC-V Edition"](https://www.amazon.com/dp/0128122757)
- [David A. Patterson, John L. Hennessy "Computer Organization and Design ARM Edition"](https://www.amazon.com/dp/0128017333)
- [John L. Hennessy, David A. Patterson "Computer Architecture: A Quantitative Approach"](https://www.amazon.com/dp/0128119055)

## Compilers, Linkers, Loaders and Runtimes
- [Matt Godbolt "The Bits Between the Bits: How We Get to main()"](https://youtu.be/dOfucXtyEsU)
- [Matt Godbolt "What Has My Compiler Done for Me Lately? Unbolting the Compiler's Lid"](https://youtu.be/bSkpMdDe4g4)
- [JF Bastien "No Sane Compiler Would Optimize Atomics"](https://www.youtube.com/watch?v=IB57wIf9W1k)
- [JF Bastien "Just-in-Time Compilation"](https://youtu.be/tWvaSkgVPpA)
- [Bob Steagall "The Structure of a Program"](https://youtu.be/3KoXeegncrs)
- [Amos (fasterthanlime) "Making our own executable packer"](https://fasterthanli.me/series/making-our-own-executable-packer)
- [Miguel Young de la Sota "Everything You Never Wanted To Know About Linker Script"](https://mcyoung.xyz/2021/06/01/linker-script/)

## Abstract Machine
Keywords: undefined behavior, memory model, pointer provenance, implementation-defined behavior, Rust ownership/lifetimes, memory safety, strict aliasing, C/C++ volatile
- [Bob Steagall "The Abstract Machine"](https://youtu.be/ZAji7PkXaKY)
- [Patrice Roy "Which Machine Am I Coding To?"](https://youtu.be/KoqY50HSuQg)
- [Niall Douglas "Elsewhere Memory (C++20 Abstract Machine) + Virtual Memory"](https://youtu.be/Djw6aY0VhwI)
- [Chandler Carruth "Garbage In, Garbage Out: Arguing about Undefined Behavior..."](https://youtu.be/yG1OZ69H_-o)
- [Ralf Jung ""What The Hardware Does" is not What Your Program Does: Uninitialized Memory"](https://www.ralfj.de/blog/2019/07/14/uninit.html)
- [Ralf Jung "Pointers Are Complicated II, or: We need better language specs"](https://www.ralfj.de/blog/2020/12/14/provenance.html)
- [Ralf Jung "Two Kinds of Invariants: Safety and Validity"](https://www.ralfj.de/blog/2018/08/22/two-kinds-of-invariants.html)
- [Miguel Young de la Sota "The Taxonomy of Pointers"](https://mcyoung.xyz/2021/05/24/ptr-taxonomy/)
- [Ulrich Drepper "What Every Programmer Should Know About Memory"](https://people.freebsd.org/~lstewart/articles/cpumemory.pdf)
- [CopperSpice "C++ Memory Model"](https://youtu.be/KgzjxfYaScU)
- [Herb Sutter "atomic Weapons: The C++ Memory Model and Modern Hardware"](https://herbsutter.com/2013/02/11/atomic-weapons-the-c-memory-model-and-modern-hardware/)
- [Hans Boehm "Using weakly ordered C++ atomics correctly"](https://www.youtube.com/watch?v=M15UKpNlpeM)
- [Paul McKenney "C++ Atomics: The Sad Story of memory_order_consume: A Happy Ending At Last?"](https://www.youtube.com/watch?v=ZrNQKpOypqU)
- [Russ Cox "Memory Models"](https://research.swtch.com/mm)

## Security/Cryptography
Keywords: threat model, principle of least priviledge, Kerckhoffs's principle, confidentiality, data integrity, authentication, non-repudiation, computational hardness, vulnerabilities, buffer overflow, side-channel attack
- [Chandler Carruth "Spectre: Secrets, Side-Channels, Sandboxes, and Security"](https://youtu.be/_f7O3IfIR2k)
- [LiveOverflow "Binary Exploitation / Memory Corruption](https://www.youtube.com/playlist?list=PLhixgUqwRTjxglIswKp9mpkfPNfHkzyeN)
- [Arun Thomas "Building Secure Systems using RISC V and Rust"](https://youtu.be/i0TmZ2vuzbs)

## Performance
Keywords: cache locality, zero-copy, data oriented design, benchmarking, SIMD
- [Emery Berger "Performance Matters"](https://www.youtube.com/watch?v=koTf7u0v41o)
- [Daniel Lemire's blog](https://lemire.me/blog/)
- [Game Programming Patterns "Data Locality"](https://gameprogrammingpatterns.com/data-locality.html)
- [Andrei Alexandrescu "Speed Is Found In The Minds of People"](https://youtu.be/FJJTYQYB1JQ)
- [Jason Turner "Practical Performance Practices"](https://youtu.be/uzF4u9KgUWI)
- [Chandler Carruth "High Performance Code 201: Hybrid Data Structures"](https://youtu.be/vElZc6zSIXM)
- [Chandler Carruth "Efficiency with Algorithms, Performance with Data Structures"](https://youtu.be/fHNmRkzxHWs)
- [Chandler Carruth "There Are No Zero-cost Abstractions"](https://youtu.be/rHIkrotSwcc)
- [Chandler Carruth "Going Nowhere Faster"](https://youtu.be/2EWejmkKlxs)
- [Chandler Carruth "Tuning C++: Benchmarks, and CPUs, and Compilers! Oh My!"](https://youtu.be/nXaxk27zwlk)
- [Andrei Alexandrescu "Optimization Tips - Mo' Hustle Mo' Problems"](https://youtu.be/Qq_WaiwzOtI)
- [Timur Doumler "Want fast C++? Know your hardware!"](https://youtu.be/BP6NxVxDQIs)
- [Alan Talbot "Moving Faster: Everyday efficiency in modern C++"](https://youtu.be/EovBkh9wDnM)
- [Matt Kulukundis "Designing a Fast, Efficient, Cache-friendly Hash Table, Step by Step"](https://youtu.be/ncHmEUmJZf4)
- [Malte Skarupke "You Can Do Better than std::unordered_map"](https://youtu.be/M2fKMP47slQ)
- [Malte Skarupke "I wrote the fastest hashtable"](https://probablydance.com/2017/02/26/i-wrote-the-fastest-hashtable/)
- [Malte Skarupke "A new fast hash table in response to Google’s new fast hash table"](https://probablydance.com/2018/05/28/a-new-fast-hash-table-in-response-to-googles-new-fast-hash-table/)
- [Malte Skarupke "Fibonacci Hashing: The Optimization that the World Forgot"](https://probablydance.com/2018/06/16/fibonacci-hashing-the-optimization-that-the-world-forgot-or-a-better-alternative-to-integer-modulo/)
- [Joshua Liebow-Feeser "Move fast and don't break things: High-performance networking in Rust"](https://youtu.be/UfMOOxOGCmA)
- [Richard Fabian "Data-Oriented Design"](http://www.dataorienteddesign.com/dodbook/)
- [Dawid Ciężarkiewicz "The faster you unlearn OOP, the better for you and your software"](https://dpc.pw/the-faster-you-unlearn-oop-the-better-for-you-and-your-software)
- [Stoyan Nikolov "OOP Is Dead, Long Live Data-oriented Design"](https://youtu.be/yy8jQgmhbAU)
- [Mike Acton "Data-Oriented Design and C++"](https://youtu.be/rX0ItVEVjHc)
- [Mike Acton "Building a Data-Oriented Future"](https://youtu.be/u8B3j8rqYMw)
- [Marek Majkowski "Kernel Bypass"](https://blog.cloudflare.com/kernel-bypass/)
- [Nick Fitzgerald "Always Bump Downwards"](https://fitzgeraldnick.com/2019/11/01/always-bump-downwards.html)

## Scalability
- [Bryan Cantrill "The Soul of a New Machine: Rethinking the Computer"](https://youtu.be/vvZA9n3e5pc)

## Concurrency & Asynchrony
Keywords: multithreading, race condition, synchronization, deadlock, starvation, linearizability, memory ordering, shared mutable state, fiber, coroutine, async/await
- [Ulrich Drepper "Futexes Are Tricky"](https://akkadia.org/drepper/futex.pdf)
- [Filip Pizlo "Locking in WebKit"](https://webkit.org/blog/6161/locking-in-webkit/)
- [Jon Gjengset "A Cool Concurrency Primitive in Rust"](https://youtu.be/eLNAMEoKAAc)
- [Dale Weiler "Fibers, Oh My!"](https://graphitemaster.github.io/fibers/)
- [Samy Al Bahra "Concurrency Kit"](http://concurrencykit.org)
- [libuv Team "libuv"](https://libuv.org)
- [Austin Clements "Proposal: Non-cooperative goroutine preemption"](https://go.googlesource.com/proposal/+/master/design/24543-non-cooperative-preemption.md)
- [Aleksey Kladov "Spinlocks Considered Harmful"](https://matklad.github.io/2020/01/02/spinlocks-considered-harmful.html)
- [Alain Kägi, Doug Burger, and James R. Goodman "Efficient Synchronization: Let Them Eat QOLB"](https://dl.acm.org/doi/pdf/10.1145/384286.264166)

## Functional Programming
Keywords: referential transparency, algebraic datatypes, lambda expression, recursion, higher order function, persistent data structure, lazy evaluation, category theory
- [Bartosz Milewski "Category Theory for Programmers"](https://bartoszmilewski.com/2014/10/28/category-theory-for-programmers-the-preface/)
- [Borislav Stanimirov "No Touchy! A Case Study of Software Architecture with Immutable Objects"](https://youtu.be/ZSrIZW2Hzhk)
- [Alexis King "Parse, don't validate"](https://lexi-lambda.github.io/blog/2019/11/05/parse-don-t-validate/)

## Distributed Systems
Keywords: CAP theorem, consensus, clock synchronization, logical clock, redundancy, fault tolerance, ACID, eventual consistency, MapReduce
- [Tim Berglund "Distributed Systems in One Lesson"](https://youtu.be/Y6Ev8GIlbxc)
- [Cory Benfield "Building Protocol Libraries The Right Way"](https://youtu.be/7cC3_jGwl_U)
- [Jerome Saltzer, David Reeed, David Clark "End-to-End Arguments in System Design"](http://web.mit.edu/Saltzer/www/publications/endtoend/endtoend.pdf)

## Operating Systems
Keywords: scheduling, preemption, context switch, address space, virtual memory, file system, device driver, IPC, virtualization, networking
- [MIT CSAIL "xv6: a simple, Unix-like teaching operating system"](https://pdos.csail.mit.edu/6.828/2014/xv6.html)
- [UW-Madison "Operating Systems: Three Easy Pieces"](http://pages.cs.wisc.edu/~remzi/OSTEP/)
- [Marshall McKusick, George Neville-Neil, Robert Watson "Design and Implementation of the FreeBSD Operating System"](https://www.informit.com/store/design-and-implementation-of-the-freebsd-operating-9780321968975)
- [OSDev wiki](https://wiki.osdev.org/Main_Page)
- [Philipp Oppermann "Writing an OS in Rust"](https://os.phil-opp.com)
- [Bryan Cantrill "Is It Time to Rewrite the Operating System in Rust?"](https://youtu.be/HgtRAbE1nBM)
- [Geoffrey Lee, Charles Gray "L4/Darwin: Evolving UNIX"](https://ts.data61.csiro.au/publications/papers/Lee_Gray_06.pdf)
- [Alexander van der Grinten "Managarm: A Fully Asynchronous OS Based on Modern C++"](https://youtu.be/BzwpdOpNFpQ)
- [Daniel Bittman, Peter Alvaro, Pankaj Mehra, Darrell D. E. Long, Ethan L. Miller "Twizzler: a Data-Centric OS for Non-Volatile Memory"](https://www.usenix.org/conference/atc20/presentation/bittman)
- [Hubertus Franke, Rusty Russell, Matthew Kirkwood "Fuss, Futexes and Furwocks: Fast Userlevel Locking in Linux"](https://www.kernel.org/doc/ols/2002/ols2002-pages-479-495.pdf)
- [Kevin Boos, Namitha Liyanage, Ramla Ijaz, Lin Zhong "Theseus: an Experiment in Operating System Structure and State Management"](http://kevinaboos.web.rice.edu/docs/theseus_boos_osdi2020.pdf)
- [Vikram Narayanan, Tianjiao Huang, David Detweiler, Dan Appel, Zhaofeng Li, Gerd Zellweger, Anton Burtsev "RedLeaf: Isolation and Communication in a Safe Operating System"](https://mars-research.github.io/doc/redleaf-osdi20.pdf)
- [Pekka Enberg, Ashwin Rao, Sasu Tarkoma "I/O Is Faster Than the CPU – Let’s Partition Resources and Eliminate (Most) OS Abstractions"](http://penberg.org/parakernel-hotos19.pdf)
- [Irene Zhang, Jing Liu, Amanda Austin, Michael Lowell Roberts, Anirudh Badam "I’m Not Dead Yet! The Role of the Operating System in a Kernel-Bypass Era"](https://www.microsoft.com/en-us/research/publication/im-not-dead-yet-the-role-of-the-operating-system-in-a-kernel-bypass-era/)
- [Dawson R. Engler, M. Frans Kaashoek, James O’Toole Jr. "Exokernel: An Operating System Architecture for Application-Level Resource Management"](https://people.eecs.berkeley.edu/~kubitron/courses/cs262a-F18/handouts/papers/engler95exokernel.pdf)
- [Simon Peter, Jialin Li, Irene Zhang, Dan R. K. Ports, Doug Woos, Arvind Krishnamurthy, Thomas Anderson, Timothy Roscoe "Arrakis: The Operating System is the Control Plane"](https://www.usenix.org/system/files/conference/osdi14/osdi14-paper-peter_simon.pdf)
- [NICTA, UNSW, Open Kernel Labs, ANU "seL4: Formal Verification of an OS Kernel"](http://www.sigops.org/s/conferences/sosp/2009/papers/klein-sosp09.pdf)
- [Andrew Tanenbaum "MINIX 3: a Modular, Self-Healing POSIX-compatible Operating System"](https://youtu.be/bx3KuE7UjGA)
- [Andrew Baumann, Jonathan Appavoo, Orran Krieger "A fork() in the road"](https://www.microsoft.com/en-us/research/uploads/prod/2019/04/fork-hotos19.pdf)
- [Amit Levy, Bradford Campbell, Branden Ghena, Daniel B. Giffin, Pat Pannuto, Prabal Dutta, Philip Levis "Multiprogramming a 64 kB Computer Safely and Efficiently"](https://sing.stanford.edu/site/publications/levy17-tock.pdf)
- [Kevin Elphinstone, Gernot Heiser "From L3 to seL4 what have we learnt in 20 years of L4 microkernels?"](http://sigops.org/s/conferences/sosp/2013/papers/p133-elphinstone.pdf)

## Research
- [Lalith Suresh "Low-level advice for systems research"](https://lalith.in/2020/09/27/Low-Level-Advice-For-Systems-Research/)

## Teaching
- [Ryan Eberhardt "Designing a New Rust Class at Stanford: Safety in Systems Programming"](https://reberhardt.com/blog/2020/10/05/designing-a-new-class-at-stanford-safety-in-systems-programming.html)
