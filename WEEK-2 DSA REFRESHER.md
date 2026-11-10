## ++Day 3++

## ++Tree++:

It is a hierarchical, non-linear data structure made up of nodes connected by edges. It starts with a single root node, and every child node has exactly one parent, creating a parent-child relationship.  
Widely used -

- to represent hierarchical data such as file systems,
- organisational structures,
- XML/HTML documents,
- decision trees  
  ![Parent Node](Attachments/973BE538-6A17-4A78-A584-1033C2C5BE94.png)

* **Root node**: topmost node of the tree that has no parent. Every non-empty tree has exactly one root node.
* **Parent node**: node that has one or more child nodes.
* **Child node**: node connected directly below a parent node.
* **Leaf node**: a node that has no children.
* **Internal node**: a node that has at least one child.
* **Descendent**: any node that lies below another node in the tree.
* **Level of a node**: the number of edges from the root node to that node. (_Root node is always at level 0_)
* **Subtree**: a tree formed by any node along with all its descendants.  
  _A tree is built using nodes, where each node stores some data and references to its child nodes. A node can be represented by creating a class with a data field and a list to store its children._

### ++Properties of Trees++:

1. ++Number of edges++: a tree with N nodes will always have N-1 edges
2. ++Depth of a node++: length of the path from the root to that node
3. ++Height of the tree++: it is the length of the longest path from the root node to any leaf node
4. ++Degree of a node++: it is the number of subtrees attached to a node

##

##

##

## ++Binary tree:++

It is a hierarchical, non-linear data structure where each node has **at most 2 children** (**_left child and right child)_**.  
The topmost node is called the **_root_**, and the bottom-most nodes are **_leaves_**.  
Each node has 3 parts -

- Data
- Pointer to the left child
- Pointer to the right child  
  ![class Node:](Attachments/FBD521A9-695F-479B-AE59-2ECBE95D26DA.png)

## ++Binary Search Tree (BST)++:

It is a type of binary tree in which each node contains a unique key and satisfies a specific ordering property:

- All nodes in the left subtree of a node contains values strictly less than the node’s value
- All nodes in the right subtree of a node contains values strictly greater than the node’s value  
  This structure enables efficient operations for searching, insertion, and deletion of elements, especially when the tree remains balanced.

### ++Key properties++ -

- Unique ordering of elements means duplicates are usually not allowed.
- In-order traversal of BST gives sorted order of elements.
- Average height: O(log n) —> for balanced BST.
- Worst-case height: O(n) —> when tree is skewed or forms a line.  
  ![Screenshot 2026-11-05 at 2.02.31 PM.png](Attachments/97F2939F-66F6-4385-9144-91EBD4C05A28.png)

## ++In-order tree traversal++:

It is basically traversing the **_left, root, and right node_** of each subtree.

- Traverse the left subtree
- Visit the root node
- Traverse the right subtree  
  ![print norder (root. bete)](Attachments/9F04D00D-3B71-4355-B2B2-16D9174D3D77.png)

## ++Pre-order tree traversal++:

It is basically traversing the **_root, left and right node_** of each subtree.

- Visit the root node
- Traverse the left subtree
- Traverse the right subtree  
  ![class Node:](Attachments/2B1491F3-6FFC-408A-ABD2-66D5272BA199.png)

## ++Post-order tree traversal++:

It is basically traversing the **_left, right and root node_** of each subtree.

- Traverse the left subtree
- Traverse the right subtree
- Visit the root node  
  ![class](Attachments/3439092C-5AA4-47FE-B1A8-77C490AE31A4.png)

## ++Level-order search or Breadth-First Search (BFS):++

It is a graph traversal algorithm that starts from the source node and explores the graph level by level.

- First it visits all nodes adjacent to the source
- Then moves to adjacent nodes of those nodes  
  This process continues until all reachable nodes are visited.  
  —> it can be used to detect cycle in a graph, finding shortest path in an unweighted graph, etc.  
  ![Input: adj!!] = [(1, 2). [0, 2). [O, 1, 3, 4], (2], (2]]](Attachments/796DB2A8-CE92-4C8A-9E1B-799B186CB3F9.png)

## ++BFS v/s DFS:++

| BFS                                                                                                   | DFS                                                                                                  |
| ----------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| Uses queue                                                                                            | Uses stack                                                                                           |
| Traversal approach in which all nodes on the same level all traversed before moving to the next level | Traversal begins at the root node and proceeds as far as possible until an unvisited node is reached |
| It builds the tree level-by-level                                                                     | Builds the tree subtree-by-subtree                                                                   |
| It works on the concept of FIFO                                                                       | It works on the concept of LIFO                                                                      |
| It is suitable for searching vertices closer to the given source                                      | Suitable for solutions that are away from the source                                                 |
