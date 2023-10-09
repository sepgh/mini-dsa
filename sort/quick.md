# Quick Sort


![image](https://github.com/sepgh/mini-dsa/assets/13250403/55688377-adf7-404f-906a-d94849237294)

https://en.wikipedia.org/wiki/Quicksort

We should first understand "evide and Conque". It means to be able to split our input into chunks and being able to solve the same problem for those chunks. It becomes something that becomes smaller and smaller and easier to solve.
---

1. If the range has fewer than two elements, return immediately as there is nothing to do. Possibly for other very short lengths a special-purpose sorting method is applied and the remainder of these steps skipped.
2. Otherwise pick a value, called a pivot, that occurs in the range (the precise manner of choosing depends on the partition routine, and can involve randomness).
3. Partition the range: reorder its elements, while determining a point of division, so that all elements with values less than the pivot come before the division, while all elements with values greater than the pivot come after it; elements that are equal to the pivot can go either way. Since at least one instance of the pivot is present, most partition routines ensure that the value that ends up at the point of division is equal to the pivot, and is now in its final position (but termination of quicksort does not depend on this, as long as sub-ranges strictly smaller than the original are produced).
4. Recursively apply the quicksort to the sub-range up to the point of division and to the sub-range after it, possibly excluding from both ranges the element equal to the pivot at the point of division. (If the partition produces a possibly larger sub-range near the boundary where all elements are known to be equal to the pivot, these can be excluded as well.)


Implementation:  https://frontendmasters.com/courses/algorithms/implementing-quicksort/

## Running time:

Mathematical analysis of quicksort shows that, on average, the algorithm takes `O(n log(n))` comparisons to sort n items. In the worst case, it makes `O(n^2)` comparisons
