# technical-links
A collection of technical links I want to be able to easily find again

Performance Tooling and Micro Architecture References
------------------------------------------------------
Agner's "Instruction tables: Lists of instruction latencies, throughputs and micro-operation breakdowns for Intel, AMD and VIA CPUs"
https://www.agner.org/optimize/instruction_tables.pdf

Agner's "The microarchitecture of Intel, AMD and VIA CPUs: An optimization guide for assembly programmers and compiler makers"
http://www.agner.org/optimize/microarchitecture.pdf

Intel MPX Explained (with latency numbers)
https://intel-mpx.github.io/

SSE: mind the gap!  
https://fgiesen.wordpress.com/2016/04/03/sse-mind-the-gap/  
Collection of useful encoding tricks for common idioms in SSE

Cores don’t like to share  
https://fgiesen.wordpress.com/2013/01/31/cores-dont-like-to-share/  
example of machine_check.memory_order issue

pmu-tools  
https://github.com/andikleen/pmu-tools
Really useful wrapper for perf with symbolic names for Intel hardware events

This is not the performance you were looking for: the tricks systems play on us
https://blogs.janestreet.com/this-is-not-the-performance-you-were-looking-for-the-tricks-systems-play-on-us/

Gathering Intel on Intel AVX-512 Transitions
https://travisdowns.github.io/blog/2020/01/17/avxfreq1.html
Exhaustive study of AVX-512 switching costs.  By far best resource I've found to date.

Intel Core i7 (Nehalem): Architecture By AMD?
http://www.tomshardware.com/reviews/Intel-i7-nehalem-cpu,2041-11.html

GCC's assembler syntax
https://www.felixcloutier.com/documents/gcc-asm.html#constraints

Intel Haswell
--------------

Intel’s high-performance, low-power secret: the Haswell SoC
http://arstechnica.com/gadgets/2013/05/a-look-at-haswell/

Intel's Haswell Architecture Analyzed: Building a New PC and a New Intel
http://www.anandtech.com/show/6355/intels-haswell-architecture/9

PMU: Intel(R) Microarchitecture Code Name Haswell  
http://www.hpc.ut.ee/dokumendid/ips_xe_2015/vtune_amplifier_xe/documentation/en/help/reference/haswell/index.htm#events/about_front_end_performance_tuning_events.html
Web version of Haswell performance counter documentation

Intel Skylake
--------------
The Intel Skylake Mobile and Desktop Launch, with Architecture Analysis
http://www.anandtech.com/show/9582/intel-skylake-mobile-desktop-launch-architecture-analysis/5

AMD Zen
-------

AMD’s Epyc is a major advance in security
https://semiaccurate.com/2017/06/22/amds-epyc-major-advance-security/

Engineering Process/Management Topics
------------------------------

Speeding Up Your Engineering Org, Part I: Beyond the Cost Center Mentality
http://blog.hut8labs.com/speeding-up-your-eng-org-part-i.html
(Strongly recommend reading.  Some thoughts by me: http://www.philipreames.com/Blog/2014/05/11/feature-latency/)

Applying the Universal Scalability Law to organisations
http://blog.acolyer.org/2015/04/29/applying-the-universal-scalability-law-to-organisations/

Getting beyond MVP
paper writeup via the morning paper
https://blog.acolyer.org/2016/11/01/getting-beyond-mvp/amp/

You Are Not Google
https://blog.bradfieldcs.com/you-are-not-google-84912cf44afb

Why vacation at tech companies should be mandatory: better code, happier people 
https://text.sourcegraph.com/why-vacation-at-tech-companies-should-be-mandatory-better-code-happier-people-d1b549681291#.87dxh09de

Speculative Optimization
-------------------------

Thin Guards: A Simple and Effective Technique for Reducing the Penalty of Dynamic Class Loading (2002) 
http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.22.2436

Fuzzing
--------
Project Triforce: Run AFL on Everything!
https://www.nccgroup.trust/us/about-us/newsroom-and-events/blog/2016/june/project-triforce-run-afl-on-everything/

OSS-Fuzz: Five months later, and rewarding projects
https://opensource.googleblog.com/2017/05/oss-fuzz-five-months-later-and.html

AFL: american fuzzy lop
http://lcamtuf.coredump.cx/afl/
(currently the easiest to use high value fuzzer out there)

libFuzzer – a library for coverage-guided fuzz testing
http://llvm.org/docs/LibFuzzer.html
(interesting, but little public information about effectiveness)

Design for Test
---------------------------
Burning in a Module with Random Unit Testing
https://blog.regehr.org/archives/737

Software Testing Using Function/Inverse Pairs
https://blog.regehr.org/archives/708

Static Analysis & Whole Program Verification
---------------
PVS-Studio Open Source Results
http://www.viva64.com/en/a/0084/

SPIN
http://spinroot.com/spin/whatispin.html

Incremental Correctness Validation
-----------------------------------
RefDiff
https://github.com/aserg-ufmg/RefDiff/blob/master/README.md
(tool for reconstructing NFC changes from diffs)

Continuous Verification: A new method to secure programs
https://medium.com/sourceclear/continuous-verification-a-new-method-to-secure-programs-5aadcb11cd5b

Assorted Compiler/Runtime Topics
---------------------------------
Leaning Technologies Blog: Announcing CheerpJ, a Java compiler for Web applications
http://blog.leaningtech.com/2017/06/announcing-cheerpj-java-compiler-for-webapps.html?m=1

CFI directives in assembly files
http://www.imperialviolet.org/2017/01/18/cfi.html

Interesting C++ Library Collections
------------------------------------

Introducing Abseil, a new common libraries project
http://opensource.googleblog.com/2017/09/introducing-abseil-new-common-libraries.html

Assorted Verification
---------------------

SAT/SMT By Example
https://yurichev.com/writings/SAT_SMT_by_example.pdf

Using TLA+ in the Real World to Understand a Glibc Bug
https://probablydance.com/2020/10/31/using-tla-in-the-real-world-to-understand-a-glibc-bug/
