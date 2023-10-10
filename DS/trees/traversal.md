# Tree traversal

> A traversal is as simple as visiting a node, which means you're gonna do something with the value of the node. And then we're going to recurse!
> Recurse, of course, is that fun operation of calling a functionto do the same thing again, but on a new node.
> And so that means we're gonna need to have a good base case. We're gonna have a pre or a post and recurse step. And so there's 3 types of tree traversals.
> And it really just depends on where you do the visiting of a node.

## Pre order

The tree recursion of which we visit nodes (assume adding node to an array of visited nodes) and recurse to next ones

```
visitNode()
recurseLeft()
recurseRight()
```

## In order (makes more sense in Binary Tree)

The tree recursion of which we recurse all left nodes and after we recurse each one we add them as visited and move to right ones.

```
recurseLeft()
visitNode()
recurseRight()
```

Now we've kind of switched up the order in which revisiting notes andthis will actually make a difference in certain types of sorting withthe binary search tree, for example in-order traversal will actually print out in order to array.

## Post order

We visit a node but after finishing recursions.

```
recurseLeft()
recurseRight()
visitNode()
```

## Running time

The running time is the "whole tree". So its `O(N)`.


## sources

https://frontendmasters.com/courses/algorithms/tree-traversals
https://frontendmasters.com/courses/algorithms/implement-tree-traversal/
