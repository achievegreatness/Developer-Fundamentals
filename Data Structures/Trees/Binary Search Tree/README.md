##Binary Search Trees

A binary tree where the nodes are ordered such that:

1. Elements to the left of the parent node are less than or equal to that of the value of the parent node.
2. Elements to the right of the parent node are greater than that of the value of the parent node.

####Search:
When searching an element in the tree, start from the root node and compare the element with the value at the right child/left child and continue down the proper subtree. Follow this algorithm at each node until the element is reached or not found.

####Insertion: 
When inserting an element in the tree, start from the root node and search for an empty location in the left or right subtree, dependent on the element's value in relation to each node.

####Deletion: 
To delete an element in the tree, you must first search for the node to remove. If found, consider the three cases below:

1. Node to be removed has no children  -> algorithm sets the link of the parent to NULL and deletes the requested node.
2. Node to be removed has one child    -> algorithm cuts node from the tree and links single child with parent of the removed node.
3. Node to be removed has two children -> find the minumum value in the corresponding subtree. Replace value of the node to be removed with found minimum. 
   Now, the subtree contains a duplicate. Remove the node on subtree to remove the duplicate.
