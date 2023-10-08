# Bubble sort

For each index of an array, we compare its value with value of next index, and if the current index value is larger than next index value we swap them.

Each time we do this the largest number in the array will be pushed to the end, so each time we do this we can compare it with one less index from end of the array.

```
# round 1
[5, 3, 6, 4]  # [0] 5 v 3
[3, 5, 6, 4]  # [1] 5 v 6
[3, 5, 6, 4]  # [2] 6 v 4
[3, 5, 4, 6]
# end of round 1, we no longer compare anything with 6

# round 2
[3, 5, 4, 6]  # [0] 3 v 5
[3, 5, 4, 6]  # [1] 5 v 4
[3, 5, 4, 6]
# end of round 2, we no longer compare anything with 6, 4

# round 3
[3, 5, 4, 6]  # [0] 3 v 5
# we are sorted
```

## Running time

We are running `N(N+1)/2` times which simply creates `O(N^2)` complexity.

## Links

### Source: The Last Algorithms Course You'll Need

- https://frontendmasters.com/courses/algorithms/bubble-sort/

