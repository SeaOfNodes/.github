# Simple - A Sea-of-Nodes Compiler IR Tutorial

Each repo is a port of the Simple compiler from its original Java port, to various other languages.

## What's a Sea of Nodes IR?

The Sea of Nodes IR is a ... compiler IR (Intermediate Representation) pioneered by Cliff Click starting around 1990, appearing as an appendix in his thesis
It became the core IR in the HotSpot C2 JIT compiler, and is used today in nearly every JVM on the planet - and C2 runs literally *trillions* of times daily.
The IR inspired Google's V8 team (and thus is/has been in Chrome), the Graal compiler and other high profile compiler efforts.

Despite this Sea of Nodes is not (to my knowledge) taught in compiler classes!
This is my (and others!) effort to teach the compiler community the how's and why's of the Sea of Nodes.

# Current ports (Sept 2024):
* [The main Java repo](https://github.com/SeaOfNodes/Simple) - The most complete repo
* [Go repo](https://github.com/SeaOfNodes/Simple-Go)
* [Rust repo](https://github.com/SeaOfNodes/Simple-Rust)
* [Cpp repo](https://github.com/SeaOfNodes/Simple-Cpp)

### Reading material:

Cliff Click's Phd Thesis.  
The Main part discusses combining optimizations which is used in e.g. C2 at least.  
The appendix starting on page 119 has a long discussion on engineering choices in the Sea of Nodes and is probably more relavent here:
* [Cliff Click Phd Thesis](https://repository.rice.edu/server/api/core/bitstreams/c5ea1ab7-e6c6-41e7-8e06-3cd5b80aeccd/content)  OR
* (https://www.researchgate.net/profile/Cliff-Click/publication/2394127_Combining_Analyses_Combining_Optimizations/links/0a85e537233956f6dd000000/Combining-Analyses-Combining-Optimizations.pdf)

A lighter read: 
* [From Quads to Graphs: An Intermediate Representation's Journey](http://softlib.rice.edu/pub/CRPC-TRs/reports/CRPC-TR93366-S.pdf)  OR
* (https://www.researchgate.net/publication/2746343_From_Quads_to_Graphs_An_Intermediate_Representation's_Journey)

Also:  
* [A Simple Graph-Based Intermediate Representation](https://www.oracle.com/technetwork/java/javase/tech/c2-ir95-150110.pdf)

The core Global Code Motion algorithm to unwind from the Sea of Nodes:
* [Global Code Motion Global Value Numbering](https://dl.acm.org/doi/10.1145/207110.207154)  OR
* (https://courses.cs.washington.edu/courses/cse501/06wi/reading/click-pldi95.pdf)
