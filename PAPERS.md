# Paper List
This is a simple list of papers I've found interesting over time and want to be able to find again.  This used to be a pile on my desk, but I'd really like to reclaim that space.  :)  

## Graal

* Gilles Duboscq, Thomas Würthinger, and Hanspeter Mössenböck. 2014. Speculation without regret: reducing deoptimization meta-data in the Graal compiler. In Proceedings of the 2014 International Conference on Principles and Practices of Programming on the Java platform: Virtual machines, Languages, and Tools (PPPJ '14). ACM, New York, NY, USA, 187-193. DOI: http://dx.doi.org/10.1145/2647508.2647521

* Thomas Würthinger, Christian Wimmer, Andreas Wöß, Lukas Stadler, Gilles Duboscq, Christian Humer, Gregor Richards, Doug Simon, and Mario Wolczko. 2013. One VM to rule them all. In Proceedings of the 2013 ACM international symposium on New ideas, new paradigms, and reflections on programming & software (Onward! 2013). ACM, New York, NY, USA, 187-204. DOI=http://dx.doi.org/10.1145/2509578.2509581

* Gilles Duboscq, Thomas Würthinger, Lukas Stadler, Christian Wimmer, Doug Simon, and Hanspeter Mössenböck. 2013. An intermediate representation for speculative optimizations in a dynamic compiler. In Proceedings of the 7th ACM workshop on Virtual machines and intermediate languages (VMIL '13). ACM, New York, NY, USA, 1-10. DOI: http://dx.doi.org/10.1145/2542142.2542143

* Aleksandar Prokopec, Gilles Duboscq, David Leopoldseder, and Thomas Würthinger. 2019. An optimization-driven incremental inline substitution algorithm for just-in-time compilers. In Proceedings of the 2019 IEEE/ACM International Symposium on Code Generation and Optimization (CGO 2019). IEEE Press, Piscataway, NJ, USA, 164-179. https://dl.acm.org/citation.cfm?id=3314893

## Escape Analysis (extreme forms) 

General problem with these techniques is that they work well for generally short lived objects, and not long lived ones.  A generational GC also does very well on short lived objects, so benefit is hard to achieve.  Mostly useful when viewed as a compiler optimization to reduce malloc traffic for unmanaged languages..

* Samuel Z. Guyer, Kathryn S. McKinley, and Daniel Frampton. 2006. Free-Me: a static analysis for automatic individual object reclamation. In Proceedings of the 27th ACM SIGPLAN Conference on Programming Language Design and Implementation (PLDI '06). ACM, New York, NY, USA, 364-375. DOI=http://dx.doi.org/10.1145/1133981.1134024

* Sigmund Cherem and Radu Rugina. 2006. Compile-time deallocation of individual objects. In Proceedings of the 5th international symposium on Memory management (ISMM '06). ACM, New York, NY, USA, 138-149. DOI=http://dx.doi.org/10.1145/1133956.1133975

## C4 Collector

Together, these two provide the best public description of the Azul C4 collector which is arguably the most advanced production collector to date.

* Cliff Click, Gil Tene, and Michael Wolf. 2005. The pauseless GC algorithm. In Proceedings of the 1st ACM/USENIX international conference on Virtual execution environments (VEE '05). ACM, New York, NY, USA, 46-56. DOI: https://doi.org/10.1145/1064979.1064988

* Gil Tene, Balaji Iyengar, and Michael Wolf. 2011. C4: the continuously concurrent compacting collector. In Proceedings of the international symposium on Memory management (ISMM '11). ACM, New York, NY, USA, 79-88. DOI=http://dx.doi.org/10.1145/1993478.1993491

## Assorted Others

* Balaji Iyengar, Gil Tene, Michael Wolf, and Edward Gehringer. 2012. The Collie: a wait-free compacting collector. In Proceedings of the 2012 international symposium on Memory Management (ISMM '12). ACM, New York, NY, USA, 85-96. DOI=http://dx.doi.org/10.1145/2258996.2259009

   An interesting thought experiment on how to leverage HTM in a collector design. 

* Naveen Neelakantam, Ravi Rajwar, Suresh Srinivas, Uma Srinivasan, and Craig Zilles. 2007. Hardware atomicity for reliable software speculation. In Proceedings of the 34th annual international symposium on Computer architecture (ISCA '07). ACM, New York, NY, USA, 174-185. DOI: https://doi.org/10.1145/1250662.1250684

   HTM with explicit aborts to implement speculative optimization in a JIT.  Performance results are hard to take at face value due to non-speculative baseline.  Unclear applicability for existing JIT compilers, but very interesting for new projects.

* C. A. R. Hoare. 1973. Hints on Programming Language Design.. Technical Report. Stanford University, Stanford, CA, USA.

   Both a classic and a fun read.

* Maged M. Michael. 2004. Hazard Pointers: Safe Memory Reclamation for Lock-Free Objects. IEEE Trans. Parallel Distrib. Syst. 15, 6 (June 2004), 491-504. DOI=http://dx.doi.org/10.1109/TPDS.2004.8

   Classic paper on a key technique for concurrent data structure design.  Also applicable to general memory management & garbage collectors.  Simple, elegant, and powerful.
   
* Iavor S. Diatchki, Mark P. Jones, and Rebekah Leslie. 2005. High-level views on low-level representations. In Proceedings of the tenth ACM SIGPLAN international conference on Functional programming (ICFP '05). ACM, New York, NY, USA, 168-179. DOI=http://dx.doi.org/10.1145/1086365.1086387 

* Jonathan Pincus and Brandon Baker. 2004. Beyond Stack Smashing: Recent Advances in Exploiting Buffer Overruns. IEEE Security and Privacy 2, 4 (July 2004), 20-27. DOI=http://dx.doi.org/10.1109/MSP.2004.36 

* Björn Hartmann, Daniel MacDougall, Joel Brandt, and Scott R. Klemmer. 2010. What would other programmers do: suggesting solutions to error messages. In Proceedings of the SIGCHI Conference on Human Factors in Computing Systems (CHI '10). ACM, New York, NY, USA, 1019-1028. DOI: https://doi.org/10.1145/1753326.1753478 

* Mendel Rosenblum and John K. Ousterhout. 1992. The design and implementation of a log-structured file system. ACM Trans. Comput. Syst. 10, 1 (February 1992), 26-52. DOI=http://dx.doi.org/10.1145/146941.146943 

*  Cristian Cadar, Daniel Dunbar, and Dawson Engler. 2008. KLEE: unassisted and automatic generation of high-coverage tests for complex systems programs. In Proceedings of the 8th USENIX conference on Operating systems design and implementation (OSDI'08). USENIX Association, Berkeley, CA, USA, 209-224. 

* Leo A. Meyerovich and Ariel S. Rabkin. 2012. Socio-PLT: principles for programming language adoption. In Proceedings of the ACM international symposium on New ideas, new paradigms, and reflections on programming and software (Onward! 2012). ACM, New York, NY, USA, 39-54. DOI=http://dx.doi.org/10.1145/2384592.2384597 

* Manuel Fähndrich, Michael Barnett, and Francesco Logozzo. 2010. Embedded contract languages. In Proceedings of the 2010 ACM Symposium on Applied Computing (SAC '10). ACM, New York, NY, USA, 2103-2110. DOI=http://dx.doi.org/10.1145/1774088.1774531 

* Lijuan Luo, Martin Wong, and Wen-mei Hwu. 2010. An effective GPU implementation of breadth-first search. In Proceedings of the 47th Design Automation Conference (DAC '10). ACM, New York, NY, USA, 52-55. DOI=http://dx.doi.org/10.1145/1837274.1837289 

*  Zachary Anderson, David Gay, Rob Ennals, and Eric Brewer. 2008. SharC: checking data sharing strategies for multithreaded c. In Proceedings of the 29th ACM SIGPLAN Conference on Programming Language Design and Implementation (PLDI '08). ACM, New York, NY, USA, 149-158. DOI=http://dx.doi.org/10.1145/1375581.1375600 

   Very different take on language design for concurrency.  In modern terms, I'd describe this as an attempt at a gradual hybrid type system for concurrency.  

*  Thomas Ball, Vladimir Levin, and Sriram K. Rajamani. 2011. A decade of software model checking with SLAM. Commun. ACM 54, 7 (July 2011), 68-76. DOI: https://doi.org/10.1145/1965724.1965743 

*  Andrew W. Appel. 1987. Garbage collection can be faster than stack allocation. Inf. Process. Lett. 25, 4 (June 1987), 275-279. DOI=10.1016/0020-0190(87)90175-X http://dx.doi.org/10.1016/0020-0190(87)90175-X 

   If you do anything involving allocator or GC design, read and understand the point made in this paper.  It's a really fundemental observation and argument in favor of GC.

*  Jacob Burnim and Koushik Sen. 2009. Asserting and checking determinism for multithreaded programs. In Proceedings of the the 7th joint meeting of the European software engineering conference and the ACM SIGSOFT symposium on The foundations of software engineering (ESEC/FSE '09). ACM, New York, NY, USA, 3-12. DOI=http://dx.doi.org/10.1145/1595696.1595700 

   Beyond the actual mechanisms in the paper, the pre-post concurrency reasoning in this paper is a really useful way of *thinking* a about concurrent data structure and algorithm design.  

*  Anil Madhavapeddy, Alex  Ho, Tim  Deegan, David J Scott, Ripduman S Sohan.  2007. Melange: creating a "functional" internet.

* Rafkind, Jon & Wick, Adam & Regehr, John & Flatt, Matthew. (2009). Precise Garbage Collection for C. International Symposium on Memory Management, ISMM.

* Jason Ansel, Yee Lok Wong, Cy Chan, Marek Olszewski, Alan Edelman, and Saman Amarasinghe. 2011. Language and compiler support for auto-tuning variable-accuracy algorithms. International Symposium on Code Generation and Optimization (CGO ’11)

* Barabash, Katherine & Petrank, Erez. (2010). Tracing Garbage Collection on Highly Parallel Platforms. ACM SIGPLAN Notices. 45.

* Ross Tate, Michael Stepp, Zachary Tatlock, and Sorin Lerner. 2009. Equality saturation: a new approach to optimization. Principles of programming languages (POPL ’09). 

* Tarun Prabhu, Shreyas Ramalingam, Matthew Might, and Mary Hall. 2011. EigenCFA: accelerating flow analysis with GPUs. SIGPLAN Not. 46, 1 (January 2011),

* Morandat, Floréal & Hill, Brandon & Osvald, Leo & Vitek, Jan. (2012). Evaluating the Design of the R Language. 

* Jeremy Condit, Matthew Harren, Zachary Anderson, David Gay, and George C. Necula. 2007. Dependent types for low-level programming. In Proceedings of the 16th European Symposium on Programming (ESOP’07)

* Ross J. Anderson. 1994. Why cryptosystems fail. Commun. ACM 37, 11 (Nov. 1994)

  If you do any form of systems work, and you haven't read this classic paper, stop what you're doing and go read it.  The story is told through a lense of security and crpto, but the leasons are much broader.
  
* utler W. Lampson and David D. Redell. 1980. Experience with processes and monitors in Mesa. Commun. ACM 23, 2 (Feb. 1980)

  Classic systems paper describing operation experience with monitors, notify, and condition variables patterns.  Still very relevant today as these remain common coordination idioms to this day.
  
* Jacob Burnim, Tayfun Elmas, George Necula, and Koushik Sen. 2011. NDSeq: runtime checking for nondeterministic sequential specifications of parallel correctness. In Proceedings of the 32nd ACM SIGPLAN Conference on Programming Language Design and Implementation (PLDI ’11)

  Basic idea is to explicitly represent the nondeterminism implicit in a parallel program into the serial semantics of the program, and then focus on proving equivelence thereof.  Figuring out whether a particular reordering is legal is one of the hardest parts of proving parallel correctness.  This paper uses a minor syntax extension to separate the proof burden into two (much) easier sub-parts.  To me, this seems like obviously the right approach, and I'm suprised this hasn't been much more widely adopted.
  
* Bird, Christian & Nagappan, Nachiappan & Devanbu, Premkumar & Gall, Harald & Murphy, Brendan. (2009). Does distributed development affect software quality?. Communications of the ACM. 52. 10.1145/1536616.1536639. 

  Found that distributed teams did not effect software quality.  Did observe a ~6% dropoff when moving to more than one building, but little beyond that.
  
* Jonathan Ragan-Kelley, Andrew Adams, Sylvain Paris, Marc Levoy, Saman Amarasinghe, and Frédo Durand. 2012. Decoupling algorithms from schedules for easy optimization of image processing pipelines. ACM Trans. Graph. 31, 4, Article 32 (July 2012), 

* Dinakar Dhurjati, Sumant Kowshik, Vikram Adve, and Chris Lattner. 2003. Memory safety without runtime checks or garbage collection. In Proceedings of the 2003 ACM SIGPLAN conference on Language, compiler, and tool for embedded systems (LCTES ’03)

   Main reason to read is a really nicely written summary of related work in the field, and good discussion of where region inference struggles.  The technique described isn't as memorable.  
   
* Dean, Jeffrey & Chambers, Craig. (1994). Towards Better Inlining Decisions Using Inlining Trials. ACM SIGPLAN Lisp Pointers. 10.1145/182409.182489. 

  Basic idea is to memoize inlining decisions by actually performing the inlining and scoring the result.  Claims minor performance wins, reduced compile times, and less sensativity to inlining thersholds.  Key detail is in the synthesis of the matching procedure which enables reuse of the original decision.  Reading it with a modern eye, there looks to be lots of room for generalizing the match procedure using program synthesis techniques.  
  
* Stephen M. Blackburn, Sergey I. Salishev, Mikhail Danilov, Oleg A. Mokhovikov, Anton A. Nashatyrev, Peter A. Novodvorsky, Vadim I. Bogdanov, Xiao Feng Li, Dennis Ushako. The Moxie JVM Experience.  TR-CS-08-01, Austrailian National University.  (Apparently also published in VEE'08, not sure it's the exact same version.)

  Fairly settled material in terms of "modern" VM design these days, but given it was written a decade ago, that's somewhat impressive.  Worth a read just for framing and related work description.
  
## Non Computer Science
---------------------

* Kumar, Deepak & Choi, Se Hoon & Washicosky, Kevin & Eimer, William & Tucker, Stephanie & Ghofrani, Jessica & Lefkowitz, Aaron & Mccoll, Gawain & Goldstein, Lee & Tanzi, Rudolph & Moir, Robert. (2016). Amyloid- peptide protects against microbial infection in mouse and worm models of Alzheimers disease. Science Translational Medicine. 8.

