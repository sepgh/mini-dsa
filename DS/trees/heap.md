# Head (Priority Queue)

A heap is a tree-based data structure that satisfies the heap property: In a max heap, for any given node C, if P is a parent node of C, then the key (the value) of P is greater than or equal to the key of C. In a min heap, the key of P is less than or equal to the key of C. The node at the "top" of the heap (with no parents) is called the root node. 

A heap can quickly return greatest or minimum value. A heap is also always a complete binary tree. It's always filled from left to the right and there wont be any gaps.

## Insertion

We move to the final spot on the heap and add the node, and ask if the heap is ordered validly? If not we replace the node with it's parent and ask the same question till we reach to a point where the heap order is valid.

## Deleting the top node (like dequeue)

To delete top node, we take it out and replace it with last node of the tree. Then we "heapify" from top! We keep checking if children are smaller (in min heap) and if they are we swap them (with the smallest child) till we get the smallest node to the root.

## The real beauty

We can implement heap in arrays, or specifically "array lists" (dynamic size). 
Once the heap is stored in an the list (as traversing tree using [DFS (pre-order)](https://github.com/sepgh/mini-dsa/blob/main/DS/trees/traversal.md#pre-order)) it's easy to prepend and append or take the first node out of it.

What is remained is "finding children" or "parent" of a node. For a node `i` where `i` is index of the node in an array, the child at left can be found using `2i+1` and child at left can be found with `2i+2`.
Note that in most programming languages, `int` won't be holding floating points therefore the results of these formulas are already floored (2.5 will be 2). To get index of the parent node we can use `(i-1)/2` formula.

## Updating

Usually heaps aren't used to be updated, but in such cases we need a hashmap of index to value...


https://frontendmasters.com/courses/algorithms/heap/


