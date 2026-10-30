---
layout: post
title: "Levels of Implementation Difficulty"
---

Computer architecture lets you do many things! Caching, branch prediction, and more. Yet some are much, much more annoying (and consequently can result in longer delays) than others. A simple ranking my yours truly from best to worst:

1. Doing math using registers

- Nothing but ALU number crunching :)

2. Reading from memory

- Load store unit

3. Writing to memory

- Cache invalidation

4. Writing to shared memory

- Mutexes

5. Writing to shared memory on a multiprocessor

- Cache coherence

