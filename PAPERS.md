# Paper List
This is a simple list of papers I've found interesting over time and want to be able to find again.  This used to be a pile on my desk, but I'd really like to reclaim that space.  :)

## Graal

* Gilles Duboscq, Thomas Würthinger, and Hanspeter Mössenböck. 2014. Speculation without regret: reducing deoptimization meta-data in the Graal compiler. In Proceedings of the 2014 International Conference on Principles and Practices of Programming on the Java platform: Virtual machines, Languages, and Tools (PPPJ '14). ACM, New York, NY, USA, 187-193. DOI: http://dx.doi.org/10.1145/2647508.2647521

* Thomas Würthinger, Christian Wimmer, Andreas Wöß, Lukas Stadler, Gilles Duboscq, Christian Humer, Gregor Richards, Doug Simon, and Mario Wolczko. 2013. One VM to rule them all. In Proceedings of the 2013 ACM international symposium on New ideas, new paradigms, and reflections on programming & software (Onward! 2013). ACM, New York, NY, USA, 187-204. DOI=http://dx.doi.org/10.1145/2509578.2509581

* Gilles Duboscq, Thomas Würthinger, Lukas Stadler, Christian Wimmer, Doug Simon, and Hanspeter Mössenböck. 2013. An intermediate representation for speculative optimizations in a dynamic compiler. In Proceedings of the 7th ACM workshop on Virtual machines and intermediate languages (VMIL '13). ACM, New York, NY, USA, 1-10. DOI: http://dx.doi.org/10.1145/2542142.2542143

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
