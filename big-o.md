# Big O notation

Big O is a way to categorize your algorithms time or memory requirements based on input. It is not meant to be an exact measurement. It will not tell you how many CPU cycles it takes, instead it is meant to generalize the growth of your algorithm.

Important concepts
- growth is with respect to the input
- Constants are dropped
  O(2N) -> O(N) and this makes sense. That is because Big O is meant to describe the upper bound of the algorithm (the growth of the algorithm). The constant eventually becomes irrelevant.
- There is practical vs theoretical differences. EX: Just because N is faster than N^2, doesn't mean practically its always faster for smaller input.


## Links:

### Source: The Last Algorithms Course You'll Need

- https://theprimeagen.github.io/fem-algos/lessons/algorithms-and-time-space-complexity/time-and-space-complexity
- https://frontendmasters.com/courses/algorithms/big-o-time-complexity/


