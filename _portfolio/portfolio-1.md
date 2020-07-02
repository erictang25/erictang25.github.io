---
title: "Game of Life"
excerpt: "Acceleration of the Game of Life using CUDA<br/><img src='/images/Gospers_glider_gun.gif'>"
collection: portfolio
---

The Game of Life is a cellular automaton devised by British mathematician John Horton Conway in 1970. It is a zero-player game in which its evolution is determined by its initial state. The game of life is Turing complete and can simulate a universal constructor or any other Turing machine. We implemented the Game of Life both sequentially and in parallel to show the effectiveness of using GPU acceleration to speed up code with high parallel portions. First, we designed a naive sequential implementation where we store each cell in a byte array. Then, we implemented a sequential and parallel version optimized the memory efficiency by encoding eight cells in a byte. Finally, we created a parallel lookup table (LUT) implementation that encodes the next cell states in a precompiled array. We evaluated the four versions based on the average execution time to simulate one generation for increasing the grid size of threads and found that the parallel versions were able to achieve a speedup of over 3000. This shows the effectiveness of hardware acceleration for parallelism to achieve higher performance in an era where single-core performance is stagnating. 

[Game of Life Github](https://github.com/erictang25/game-of-life)
