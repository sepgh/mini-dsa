# Breadth-First Search

Kinda an opposite of Depth-First search. It uses `Queue` instead of `Stack` (read more about [stack in Depth-First](https://github.com/sepgh/mini-dsa/blob/main/DS/trees/traversal.md#why-depth-first)).

In BFS you visit each level and then move on to the next level.

![image](https://github.com/sepgh/mini-dsa/assets/13250403/e54fa3d6-007d-4269-ae4e-43074ae193cf)

Assuming we have the tree above, here is how we traverse/search.

```
Step 1: Empty Queue:  {}
Step 2: Add 7  {7}
Step 3: Peek item and add the children (7). {7, 23, 8}
Step 4: Dequeue/Visit {23, 8}

Step 5: Peek item and add children (23). {23, 8, 5, 4}
Step 6: Dequeue/Visit {8, 5, 4}

Step 7: Peek item and add children (8). {8, 5, 4, 21, 15}
Step 8: Dequeue/Visit {5, 4, 21, 15}

Step 9: Peek item and add children (5). {5, 4, 21, 15}
Step 10: Dequeue/Visit {4, 21, 15}

Step 11: Peek item and add children (4). {4, 21, 15}
Step 12: Dequeue/Visit {21, 15}

Step 9: Peek item and add children (21). {21, 15}
Step 10: Dequeue/Visit {15}

Step 9: Peek item and add children (15). {15}
Step 10: Dequeue/Visit {}
```

## Running time

`O(N)` when used with Queue


## Sudo code

```
queue = {head}
while not queue.epmty:
  next = queue.dequeue()
  qeueue.enqueue(next.left)
  qeueue.enqueue(next.right)
```


## Source

https://frontendmasters.com/courses/algorithms/breadth-first-search/
https://frontendmasters.com/courses/algorithms/implement-breadth-first-search/
