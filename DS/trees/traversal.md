# Tree traversal  (Depth First)

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

## Why "Depth First"?
 
 If we do an in order traversal we are going to go left allthe way until we can no longer go left.In other words we're gonna go as deep as possible in this tree on the left handside and then visit a node.Then we're gonna go right once and then go as left as deep as possible andthen come back and visit that node. And so if you think about we always go depth first, right that's what that means, that's why it's called the DFS or depth first search or depth first traversal.

 That's all you're doing which means **we can technically do any of these traversals without using recursion**. We just simply have to a**dd the children to a stack** and we do the same thing.

## Running time

The running time is the "whole tree". So its `O(N)`.


## sources

https://frontendmasters.com/courses/algorithms/tree-traversals
https://frontendmasters.com/courses/algorithms/implement-tree-traversal/
