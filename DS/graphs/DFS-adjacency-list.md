# DFS on Adjacency List

The problem is to find a path from source to needle and return it if such path exists in a graph. It is very similar to ["Path Finding" problem](https://github.com/sepgh/mini-dsa/blob/main/recursion/path_finding.md).

We need to create and update a "seen" list so we don't visit a vertex twice. 

To build a path, we walk it like this:

- we start somewhere, 
- if we saw the node before we return false otherwise we add it to seen list
- push the current node to the path, and if we reached the needle we return the path
- otherwise we loop over edges of current node and do the same walking till we get a true from a recursive walk
- if no recursive child walking returned true we pop current node from path and return false


https://frontendmasters.com/courses/algorithms/implement-dfs-on-adjacency-list/
