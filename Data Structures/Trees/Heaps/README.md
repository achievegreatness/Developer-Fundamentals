##Heaps

Heaps, or priority queues, are partially sorted binary trees where the value of the root is greater than that of the child (max heap) or the root is less than that of the child (min heap).

####Insertion: 
When pushing to the heap, nodes are automatically added to the end of the heap (from left to right). The value is compared with that of the parent node. If the value is less than/greater than (depending on min or max heap), swap accordingly. Repeat until the heap property holds.

####Deletion: 
When popping from the heap, the root node is removed and replaced with the last element in the heap. The value is then compared with the child nodes and swapped if the heap property (min/max) requires.

####Heapify: 
Heapify is the process of converting a binary tree to a heap structure. The process starts at the lowest (furthest in the tree) parent node. The value at the node is compared with its children and swapped if necessary. Move from parent to parent until the heap property holds throughout the tree.

