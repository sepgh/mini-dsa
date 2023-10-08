# Linked List

A linked list is a linear data structure, in which the elements are not stored at contiguous memory locations. The elements in a linked list are linked using pointers as shown in the below image:

![image](https://github.com/sepgh/mini-dsa/assets/13250403/4b2c16ef-1f9b-45f0-9bf8-348f5b31028a)
Source: https://www.geeksforgeeks.org/data-structures/linked-list/

Interface:

![image](https://github.com/sepgh/mini-dsa/assets/13250403/7f1b42b8-154b-4acd-8c69-03ced7daddea)



## Time Complexity

Is not good at traversing, normally does it in `O(N)`. But its extremely fast `O(1)` at prepending/appending (size growth) without need of copying. Getting head and tail is also constant operation.
Getting, deleting and editing from middle is costly and are done with `O(N)`.


## Array vs Linked List

Traversing in arrays are done with `O(1)`. However their size is limited so if you want to write a new value outside the bound you need to copy the array into a larger array first which is `O(N)` operation. Arrays need to allocate memory when they are defined, while a linked list is more optimized in this regard.

More details: https://frontendmasters.com/courses/algorithms/arrays-vs-linked-list/


## Links (other)

### Source: The last algorithm course you'll need
(This is doubly linked list)
- https://frontendmasters.com/courses/algorithms/linked-list-data-structures/
- https://frontendmasters.com/courses/algorithms/linked-list-complexity/
