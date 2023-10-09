# Path finding (problem)

Assuming we have a 2D array like below

```
[
  ["#","#","#","#","#","E","#"],
  ["#","#"," "," "," "," ","#"],
  ["#"," "," ","#","#","#","#"],
  ["#","S","#","#","#","#","#"],
]
```

Let's say any item with value `#` is a wall, we would like to find list of points which show path from `S` to `E`, knowing where `S` is.


# Base case

1. If we hit a wall we are in wrong direcion (we return)
2. If we are off the map then we return
3. If we are at "E" then we got to the goal
4. If we have seen a tile before then we return  (using `seen` arr)

# Recursive case

We call this recursion **walk** (act of walking in each direction)

- Push current point to `path`
- Push current point to `seen`
- **walk** all 4 directions [up, right, bottom, left] **-> we use loop here <-** and since we are calling walk then we are recursing.
- We try the base case for each direction. If base case return true then we reached the goal and we return.
- Remove current point from `path` if we are out of the loop because that path didnt get to somewhere.


More info:

- https://frontendmasters.com/courses/algorithms/path-finding-base-case/
- https://frontendmasters.com/courses/algorithms/path-finding-recursive-case/

# Time complexity (?)

Not sure, `O(k^2)`?
