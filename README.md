# technical-links
A collection of technical links I want to be easily find again

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

Intel Core i7 (Nehalem): Architecture By AMD?
http://www.tomshardware.com/reviews/Intel-i7-nehalem-cpu,2041-11.html

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

Incremental Correctness Validation
-----------------------------------
RefDiff
https://github.com/aserg-ufmg/RefDiff/blob/master/README.md
(tool for reconstructing NFC changes from diffs)

Continuous Verification: A new method to secure programs
https://medium.com/sourceclear/continuous-verification-a-new-method-to-secure-programs-5aadcb11cd5b
