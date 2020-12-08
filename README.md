# What is systems programming?
Broadly, developing software that is:
1. Relied upon for correctness and security by other software.
2. Constrained by physical resources of its execution environments.

# What are some resources to learn about systems programming?
## Data Structures & Algorithms
Keywords: asymptotic complexity, array, queue, hash table, search tree, linked list, heap, sorting, binary search, backtracking, graph search, divide and conquer, memoization, string matching
- [E-Maxx "Competitive Programming Algorithms"](https://cp-algorithms.com)

## Programming Languages
- [Robert C. Seacord "Effective C: An Introduction to Professional C Programming"](https://nostarch.com/Effective_C)
- [Cliff L. Biffle "Prefer Rust to C/C++ for new code."](http://cliffle.com/blog/prefer-rust/)
- [Cliff L. Biffle "Learn Rust the Dangerous Way"](http://cliffle.com/p/dangerust/)
- [Ginger Bill "The Fatal Flaw of Ownership Semantics"](http://www.gingerbill.org/article/2020/06/21/the-ownership-semantics-flaw/)

## Computer Architecture
Keywords: von Neumann architecture, instruction set architecture, memory hierarchy, endianness, pipelining, branch prediction, out-of-order execution, cache coherence, trap
- [Bryan Cantrill "The Soul of a New Machine: Rethinking the Computer"](https://youtu.be/vvZA9n3e5pc)

## Compilers
- [Matt Godbolt "The Bits Between the Bits: How We Get to main()"](https://youtu.be/dOfucXtyEsU)
- [Matt Godbolt "What Has My Compiler Done for Me Lately? Unbolting the Compiler's Lid"](https://youtu.be/bSkpMdDe4g4)
- [JF Bastien "No Sane Compiler Would Optimize Atomics"](https://www.youtube.com/watch?v=IB57wIf9W1k)
- [Bob Steagall "The Structure of a Program"](https://youtu.be/3KoXeegncrs)

## Abstract Machine
Keywords: undefined behavior, implementation-defined behavior, Rust ownership/lifetimes, memory safety, strict aliasing, C/C++ volatile
- [Bob Steagall "The Abstract Machine"](https://youtu.be/ZAji7PkXaKY)
- [Patrice Roy "Which Machine Am I Coding To?"](https://youtu.be/KoqY50HSuQg)
- [Niall Douglas "Elsewhere Memory (C++20 Abstract Machine) + Virtual Memory"](https://youtu.be/Djw6aY0VhwI)
- [Chandler Carruth "Garbage In, Garbage Out: Arguing about Undefined Behavior..."](https://youtu.be/yG1OZ69H_-o)
- [Ralf Jung ""What The Hardware Does" is not What Your Program Does: Uninitialized Memory"](https://www.ralfj.de/blog/2019/07/14/uninit.html)
- [Ulrich Drepper "What Every Programmer Should Know About Memory"](https://people.freebsd.org/~lstewart/articles/cpumemory.pdf)
- [Herb Sutter "atomic Weapons: The C++ Memory Model and Modern Hardware"](https://herbsutter.com/2013/02/11/atomic-weapons-the-c-memory-model-and-modern-hardware/)
- [Hans Boehm "Using weakly ordered C++ atomics correctly"](https://www.youtube.com/watch?v=M15UKpNlpeM)
- [Paul E. McKenney "C++ Atomics: The Sad Story of memory_order_consume: A Happy Ending At Last?"](https://www.youtube.com/watch?v=ZrNQKpOypqU)

## Security/Cryptography
Keywords: threat model, principle of least priviledge, Kerckhoffs's principle, confidentiality, data integrity, authentication, non-repudiation, computational hardness, vulnerabilities, buffer overflow, side-channel attack
- [Chandler Carruth "Spectre: Secrets, Side-Channels, Sandboxes, and Security"](https://youtu.be/_f7O3IfIR2k)
- [Ryan Eberhardt "Designing a New Rust Class at Stanford: Safety in Systems Programming"](https://reberhardt.com/blog/2020/10/05/designing-a-new-class-at-stanford-safety-in-systems-programming.html)
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

## Concurrency & Asynchrony
Keywords: multithreading, race condition, synchronization, deadlock, starvation, linearizability, memory ordering, shared mutable state, fiber, coroutine, async/await
- [Arthur O'Dwyer "Concurrency"](https://youtu.be/F6Ipn7gCOsY)
- [Filip Pizlo "Locking in WebKit"](https://webkit.org/blog/6161/locking-in-webkit/)
- [Jon Gjengset "A Cool Concurrency Primitive in Rust"](https://youtu.be/eLNAMEoKAAc)

## Functional Programming
Keywords: referential transparency, algebraic datatypes, lambda expression, recursion, higher order function, persistent data structure, lazy evaluation, category theory
- [Borislav Stanimirov "No Touchy! A Case Study of Software Architecture with Immutable Objects"](https://youtu.be/ZSrIZW2Hzhk)
- [Alexis King "Parse, don't validate"](https://lexi-lambda.github.io/blog/2019/11/05/parse-don-t-validate/)
- [Alexis King "No, dynamic type systems are not inherently more open"](https://lexi-lambda.github.io/blog/2020/01/19/no-dynamic-type-systems-are-not-inherently-more-open/)

## Distributed Systems
Keywords: CAP theorem, consensus, clock synchronization, logical clock, redundancy, fault tolerance, ACID, eventual consistency, MapReduce
- [Tim Berglund "Distributed Systems in One Lesson"](https://youtu.be/Y6Ev8GIlbxc)
- [Cory Benfield "Building Protocol Libraries The Right Way"](https://youtu.be/7cC3_jGwl_U)

## Operating Systems
Keywords: scheduling, preemption, context switch, address space, virtual memory, file system, device driver, IPC, virtualization, networking
- [MIT CSAIL "xv6: a simple, Unix-like teaching operating system"](https://pdos.csail.mit.edu/6.828/2014/xv6.html)
- [OSDev wiki](https://wiki.osdev.org/Main_Page)
- [Philipp Oppermann "Writing an OS in Rust"](https://os.phil-opp.com)
- [Bryan Cantrill "Is It Time to Rewrite the Operating System in Rust?"](https://youtu.be/HgtRAbE1nBM)
- [Geoffrey Lee and Charles Gray "L4/Darwin: Evolving UNIX"](https://ts.data61.csiro.au/publications/papers/Lee_Gray_06.pdf)
