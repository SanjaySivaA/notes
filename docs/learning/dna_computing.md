---
title: "DNA Computing"
---


## Introduction

Uses DNA, biochemistry and molecular biology hardware instead of traditional silicon ones. Sub-field of DNA nanoscience(self assembly etc).

Problem - specifically talking about Adleman's experiment, the components required grows exponentially as the number of nodes in the graph grows.  

[Further reading](https://en.wikipedia.org/wiki/DNA_computing#:~:text=Therefore,complete)

Slow speed(response time is in minutes, hours or days) is compensated by high potential for parallelism. However for exponential space problems,
amount of DNA required is too large to be practical.

Also, it is more difficult to analyze the results compared to a digital computer. 


## Adleman's 1994 Paper

### Problem

The [paper](https://courses.cs.duke.edu/spring08/cps296.4/papers/Adleman94.pdf) explained how DNA moleecules were used to encode a graph 
to solve an instance of the directed Hamiltonian path problem. 

A directed graph $G$ with designated vertices $v_{in}$ and $v_{out}$ is said to have a Hamiltonian path if and only if $\exists$ a path that begins
at $v_{in}$, ends at $v_{out}$ and enters every other vertex exactly once.

Some combinations of start and end vertices may not have Hamiltonian path(s).

There are algorithms for determining whether an arbitrary directed graph with designated vertices has a hamiltonian path. But all of them have 
exponential worst case running time. The directed Hamiltonian path problem is also NP-complete.  

```py
    # A non-deterministic algorithm for solving directed Hamiltonian Path problem

    '''
        Step 1: Generate random paths through the graph
        Step 2: Only keep paths starting from v_in and ending at v_out
        Step 3: If graph has n vertices, keep paths that enter exactly n vertices
        Step 4: Only keep paths that enter all vertices in the graph exactly once
        Step 5: 'Yes' if paths remaining otherwise 'No'
    '''
```

### Implementation

To implement step 1 of the algorithm, each vertex $i$ in the graph was associated with a random 20-mer(a sequence of 20 nucleotides) of DNA denoted $O_i$.

### Results

### Errors

### Advantages

### Remarks