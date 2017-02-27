#Binary Trees

This folder focuses on the various binary tree implementations. A **binary tree** is made up of nodes where each node contains a "left" and "right" pointer, and data element. The "root" pointer points to the topmost node in the tree.


##Binary Search Trees

A binary tree where the nodes are ordered such that:

      1. all the elements to the left of the parent node are less than or equal to that of the value of the parent node.
      2. all the elements to the right of the parent node are greater than that of the value of the parent node.

####Search:
When searching an element in the tree, start from the root node and compare the element with the value at the right child/left child and continue down the proper subtree. Follow this algorithm at each node until the element is reached or not found.

####Insertion: 
When inserting an element in the tree, start from the root node and search for an empty location in the left or right subtree, dependent on the element's value in relation to each node.

####Deletion: 
To delete an element in the tree, you must first search for the node to remove. If found, consider the three cases below:

      1. Node to be removed has no children  -> algorithm sets the link of the parent to NULL and deletes the requested node.
      2. Node to be removed has one child    -> algorithm cuts node from the tree and links single child with parent of the removed node.
      3. Node to be removed has two children -> find the minumum value in the corresponding subtree. Replace value of the node to be removed with found minimum. Now, the subtree contains a duplicate. Remove the node on subtree to remove the duplicate.
      
#####Pros:

#####Cons:
* The shape of the tree depends on the order of insertions.
* When inserting or searching for an element, the key of each visited node has to be compared with the key of the element to be inserted/found. Keys may be long and hte run time may increase much. To improve the efficiency of the BST, keeping the tree balanced (AVL trees) or reduce the time for key comparison (Radix trees).

##Heaps

Heaps, or priority queues, are partially sorted binary trees where the value of the root is greater than that of the child (max heap) or the root is less than that of the child (min heap).

####Insertion: 
When pushing to the heap, nodes are automatically added to the end of the heap (from left to right). The value is compared with that of the parent node. If the value is less than/greater than (depending on min or max heap), swap accordingly. Repeat until the heap property holds.

####Deletion: 
When popping from the heap, the root node is removed and replaced with the last element in the heap. The value is then compared with the child nodes and swapped if the heap property (min/max) requires.

####Heapify: 
Heapify is the process of converting a binary tree to a heap structure. The process starts at the lowest (furthest in the tree) parent node. The value at the node is compared with its children and swapped if necessary. Move from parent to parent until the heap property holds throughout the tree.


##AVL Trees

#####Pros:
* Guaranteed fast lookup
* Strictly balanced
* Self-balancing by height of tree

#####Cons:
* Slow insert, delete


##Red-Black Trees


##Tree Operations
![trees](https://cloud.githubusercontent.com/assets/25939990/23381559/ca69843c-fcf3-11e6-81cf-c2d20e2e15d4.png)
