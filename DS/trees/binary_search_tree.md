# Binary search tree (strong ordered)

a binary search tree (BST), also called an ordered or sorted binary tree, is a rooted binary tree data structure with the key of each internal node being greater than all the keys in the respective node's left subtree and less than the ones in its right subtree.
The time complexity of operations on the binary search tree is linear with respect to the height of the tree, or `O(H)`.

 ![image](https://github.com/sepgh/mini-dsa/assets/13250403/399ec9ac-2cc1-4db5-b28b-70e528469a4d)

 It's really good for adding and removing values compared to linked list which requires `O(N)`. But we have to assure the tree is always preserved within the rules.


## Insertion

For insertion we should be careful that we may hit a NULL right, and thats where we shhould insert new node.

## Delete

Deletion gets more complex. If a node doesn't have a child we can simply remove it.

If there is only one child (for the node we want to remove), then we can take the current node parent's pointer (pointer that belongs to the parent of the current node) and point it to the child.

If a node has both childs, we need to either A) find the largest node at the smaller side of current node, or B) find the smallest node at the larger side of current node, and replace that with current node (parent of current node points to that, previous parent would no longer point to it) and remove current node.

Normally there is no difference between choosing A or B, but if we keep the height of the tree at each node then we can make better decision on which side to choose based on the smaller height.

 
## Source:

search implemented: https://frontendmasters.com/courses/algorithms/implement-depth-first-search/
