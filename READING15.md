# Tree data structure
- is a hierarchical structure that is used to represent and organize data in a way that is easy to navigate and search. 
- It is a collection of nodes that are connected by edges and has a hierarchical relationship between the nodes. 

- The topmost node of the tree is called the root, and the nodes below it are called the child nodes. 
- Each node can have multiple child nodes, and these child nodes can also have their own child nodes, forming a __recursive structure__.

### Common Terminology

- Node - A Tree node is a component which may contain its own values, and references to other nodes
- Root - The root is the node at the beginning of the tree
- K - A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.
- Left - A reference to one child node, in a binary tree
- Right - A reference to the other child node, in a binary tree
- Edge - The edge in a tree is the link between a parent and child node
- Leaf - A leaf is a node that does not have any children
- Height - The height of a tree is the number of edges from the root to the furthest leaf

## Two categories of traversals :

- __Depth First:__   prioritize going through the depth (height) of the tree first. 
__Three methods:__

   + Pre-order: root >> left >> right
   - In-order: left >> root >> right
   - Post-order: left >> right >> root
- __Breadth First:__  traversal iterates through the tree by going through each level of the tree node-by-node.


## deferent traverse category Algorithm:
1. pre-order traversal:

   - Pre-order means that the root has to be looked at first.
  
        ALGORITHM preOrder(root)

        OUTPUT <-- root.value

        if root.left is not NULL
        preOrder(root.left)

        if root.right is not NULL
        preOrder(root.right)
     
2. In-order:

        ALGORITHM inOrder(root)
        // INPUT <-- root node
        // OUTPUT <-- in-order output of tree node's values

        if root.left is not NULL
        inOrder(root.left)

        OUTPUT <-- root.value

        if root.right is not NULL
        inOrder(root.right)


***The biggest difference between each of the traversals is when you are looking at the root node.***

### utilizing a built-in queue to implement a breadth first traversal:

     ALGORITHM breadthFirst(root)
     // INPUT  <-- root node
     // OUTPUT <-- front node of queue to console

      Queue breadth <-- new Queue()
      breadth.enqueue(root)

      while breadth.peek()
      node front = breadth.dequeue()
      OUTPUT <-- front.value

      if front.left is not NULL
      breadth.enqueue(front.left)

      if front.right is not NULL
      breadth.enqueue(front.right)


## Notes:
 - no structural rules for where nodes are “supposed to go” in a binary tree. it really doesn’t matter where a new node gets placed.
- The Big O time complexity for inserting a new node is O(n).
- The Big O space complexity for a node insertion using breadth first insertion will be O(w) (w is the largest width of tree).
- maximum width for a perfect binary tree, is 2^(h-1), where h is the height of the tree.
- A Binary Search Tree (BST) is a type of tree that does have some structure attached to it.
- The best way to approach a BST search is with a while loop.
- The Big O time complexity of a Binary Search Tree’s insertion and search operations is O(h), or O(height).
- The Big O space complexity of a BST search would be O(1). 
- During a search, we are not allocating any additional space.