# ebpftalk
All things eBPF

In the begining ...

[The BSD Packet Filter:
A New Architecture for User-level Packet Capture - Winter USENIX 1993](https://www.tcpdump.org/papers/bpf-usenix93.pdf)
20x faster than state of the art.






```bash
man bpf
```

LLVM family languages -> eBPF bytecode -> machine code to run in Kernel

Static analysis to prove the code is safe.
No loops.
No bad pointer de-references.
Size restrictions.
Always halts.


kprobe (when_event_happens, run_this())
k_ret probe
uprobe - userspace probes

[eBPF Features by Kernel Version](https://github.com/iovisor/bcc/blob/master/docs/kernel-versions.md)

[eBPF at Facebook](https://www.youtube.com/watch?v=ZYBXZFKPS28)
Alexei Starovoitov - original author of eBPF kernel patch

[IOVISOR project](https://www.iovisor.org/)
eBPF, bcc (eBpf Compiler Collection), XDP (eXpress Data Path) bare metal packet processing

[Using eBPF for Lightweight Android Profiling](https://www.youtube.com/watch?v=Vjb3qHem8io)
Riham Selim from Facebook

[seccomp-bpf Docker settings](https://docs.docker.com/engine/security/seccomp/)
```bash
# Set secccomp to YOLO
docker run --rm -it --security-opt seccomp=unconfined debian:jessie \
    unshare --map-root-user --user sh -c whoami
```

[eBPF Superpowers - DockerCon 2019](https://www.youtube.com/watch?v=4SiWL5tULnQ)
Liz Rice of Aqua Security livecodes some eBPF programs, shows commoon errors given by the verifyer.

[Understanding eBPF in a Hurry](https://www.youtube.com/watch?v=BNTQ8CNv7A0)
Ray Jenkins of Segment (which just merged with Twillio)

[How io_uring and eBPF Will Revolutionize Programming in Linux](https://thenewstack.io/how-io_uring-and-ebpf-will-revolutionize-programming-in-linux/) - eBPF at ScyllaDB.

[eBPF Adventures: Fiddling with the Linux Kernel and Unix Domain Sockets](https://www.nccgroup.com/us/about-us/newsroom-and-events/blog/2019/march/ebpf-adventures-fiddling-with-the-linux-kernel-and-unix-domain-sockets/)

[The Top Reasons Why You Should Give eBPF a Chance](https://blog.container-solutions.com/the-top-reasons-why-you-should-give-ebpf-a-chance)

[BPF Performance Tools (book)](http://www.brendangregg.com/bpf-performance-tools-book.html) - and the [git repo](https://github.com/brendangregg/bpf-perf-tools-book).

[eBPF - Rethinking the Linux Kernel](https://www.infoq.com/presentations/facebook-google-bpf-linux-kernel/)

[Security Monitering with eBPF](http://www.brendangregg.com/Slides/BSidesSF2017_BPF_security_monitoring.pdf)

[Awesome eBPF](https://github.com/zoidbergwill/awesome-ebpf)

[Kernel tree eBPF samples](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/tree/samples/bpf)

[rBPF](https://github.com/qmonnet/rbpf) - user space eBPF in Rust - use BPF on Linux containers like AWS Lambda that don't support eBPF.

[Linux Tracing Workshop](https://github.com/goldshtn/linux-tracing-workshop)
Collection of examples to trace C, JVM, .Net, Node, whole Docker Containters, 

[ProfilingJVM	Applications in	Production](https://www.usenix.org/sites/default/files/conference/protected-files/srecon18americas_slides_goldshtein.pdf)


-----
Building bcc tools Under WSL2

[Microslft WSL2 Linux Releases](https://github.com/microsoft/WSL2-Linux-Kernel/releases)

[GCC10 breaks the WSL2 Linux Build](https://lkml.org/lkml/2020/1/29/494)
----
* Unix monads (need STDERR, environment variables, and command line args too..) (shell monad)[http://okmij.org/ftp/Computation/monadic-shell.html]

* [Nanosecond](https://www.youtube.com/watch?v=9eyFDBPk4Yw) - Grace Hopper explains latency to Admirals with a foot of wire.

* [Performance Matters](https://www.youtube.com/watch?v=koTf7u0v41o) - Using simple stats to slow threads and understand why code is slow.

* [Language Level IO Typing](http://learnyouahaskell.com/input-and-output)

* [IO Typing with Clang Anylizer] (https://llvm.org/devmtg/2012-11/Zaks-Rose-Checker24Hours.pdf)

* [Not Hotdog dead code elimination](https://github.com/tensorflow/tensorflow/pull/7832)

* My stripped version of sqlite.

* eBPF condoms

* [Whole Program LLVM](https://github.com/travitch/whole-program-llvm)

* eBPF -> lcov?

* towards crypto signed data lineage

* Bolt/propeller - link permuations and live function splitting for cache efficency - can we eBPF to re-link on the fly for iterative code (molecular dynamics, CFD, ..., rebuilds of a codebase) ?

* eBPF feedback to generate upstream AST matchers for static lints in the CI.

* eBPF expectation tests - could we have eBPF in the browser? Analoge to Neo - re-writing the IO?  Could eBPF be used to create a jHipster on steroids?

