# Binary Search

Binary search works only on **sorted arrays**. The idea is to take a starting point, high point and a middle point (to begin with, this would be `low = 0`, `high = array.length`, `mid = low + (high - low) / 2`.

Then we check if the item we are searching for is equal to the mid point, and it is then we found it.
If not, in case the number is less than the current mid point, we move the `high` to `mid`, and calculate mid again, and perform the check again.
And in case the number is larger than the current mid point, we move the `low` to `mid + 1` **(Note the +1 here)**, and calculate mid again, and perform the check again.

We perform this operation as long as `low` is lower than `high`. 

# Running time

It runs at `O(Log(n))` since we are reducing the size of the data to check as we check.

## Links

### Source: The Last Algorithms Course You'll Need

- https://frontendmasters.com/courses/algorithms/pseudo-code-binary-search/
