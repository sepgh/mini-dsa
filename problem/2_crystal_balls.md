# Two crystal balls problems

> Given two crystal balls that will break if dropped from high enough distance, determine the exact spot in which it will break in the most optimized way.

**Better (or worse) explanation:** 
You have two crystal balls made identically. You have a building with N number of floors. You are allowed to drop your crystal balls at floors of this building.
In the most optimized way, find the **minimum** floor of which if you drop a crystal ball from, it will [start to] break (The [start to] should be obvious. If a ball breaks at Nth floor, it will break at N+1 too).

Or, imagine you have an array of booleans with length N. This array is special! All values are normally `false` till at one point they suddenly start to become `true` till end. 
Find the first index that the value is `true` with limitation that your algorithm ends when it check a value that is `true` twice.

## Solution

We should find best way to take steps to do a drop test. If we go linearly (loop from 0 to N) our time would be `O(N)`. 

We can't really make it work like [binary search](https://github.com/sepgh/mini-dsa/blob/main/search/binary.md) either. Imagine you go for a `mid`, and its `true`. Now you have to go back to last mid and move one by one to current mid. So again the runtime complexity would be `O(N)` (eventually).

Instead, we could take `√N` steps. If at one step we hit a `true` (one crystal ball breaks) we take `√N (+1)` steps back and go one by one (max `√N`) till we hit a breaking point.

## Running time

As explained above, its `O(√N)`.

![image](https://github.com/sepgh/mini-dsa/assets/13250403/44829f38-ec23-4bc6-aa01-ff9cfde048ad)


## Links

### Source: The Last Algorithms Course You'll Need

- https://frontendmasters.com/courses/algorithms/two-crystal-balls-problem/

