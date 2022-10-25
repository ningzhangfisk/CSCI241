# 7.2 Binary Trees
## 7.2.1 Binary Tree Definition
+ A binary tree is an ordered tree with the following properties:
  - Every node has at most `two children`.
  - Each child node is labeled as being either a `left child` or a `right child`.
  - A left child precedes a right child in the order of children of a node.
+ The subtree rooted at a left or right child of an internal node v is called a `left subtree` or `right subtree`, respectively, of v.
+ A binary tree is `proper` if each node has either zero or two children. Some people also refer to such trees as being full binary trees. Thus, in a proper binary tree, every internal node has exactly two children. A binary tree that is not proper is `improper`.
+ Example 1: An important class of binary trees arises in contexts where we wish to represent a number of different outcomes that can result from answering a series of yes-or-no questions.
![binary tree 1]([https://miro.medium.com/max/1024/1*EFCePNEkqoGmxm5qR-nqrA.gif](https://sbme-tutorials.github.io/2020/data-structure-FALL/images/Tree03.png))

+ Example 2: An arithmetic expression can be represented by a binary tree whose leaves are associated with variables or constants, and whose internal nodes are associated with one of the operators 

![binary tree 2](https://i.ytimg.com/vi/_LxbhLNRZkI/maxresdefault.jpg)

## 7.2.2 A Recursive Binary Tree Definition
+ In this case, a binary tree is either:
  -  An empty tree.
  -  A nonempty tree having a root node r, which stores an element, and two binary trees that are respectively the left and right subtrees of r. We note that one or both of those subtrees can be empty by this definition.

## 7.2.3 The Binary Tree Abstract Data Type
+ A binary tree is a specialization of a tree that supports three additional accessor methods:
  - left(p): Returns the node of the left child of p (or null if p has no left child).
  - rigth(p): Returns the node of the right child of p (or null if p has no right child).
  - sibling(p): Returns the node of the sibling of p (or null if p has no sibling).
## 7.2.4 Properties of Binary Trees
+ Binary trees have several interesting properties dealing with relationships between their heights and number of nodes. We denote the set of all nodes of a tree T at the same depth d as level d of T . In a binary tree, level 0 has at most one node (the root), level 1 has at most two nodes (the children of the root), level 2 has at most four nodes, and so on. In general, level d has at most 2^d nodes.

![Properties of Binary Trees](https://sbme-tutorials.github.io/2020/data-structure-FALL/images/Tree04.png)
## Tree Implementation (using Liked Structures)
+ natural way to realize a binary tree T is to use a linked structure, with a node in the following graph that maintains references to the element stored at a position p and to the nodes associated with the children and parent of p.
+ If p is the root of T , then the parent field of p is null. Likewise, if p does not have a left child (respectively, right child), the associated field is null. 
+ The tree itself maintains an instance variable storing a reference to the root node (if any), and a variable, called size, that represents the overall number of nodes of T .

![binary tree](https://sbme-tutorials.github.io/2020/data-structure-FALL/images/Tree05.png)

## 7.2.6 Operations for Updating a Linked Binary Tree
+ The Tree and BinaryTree interfaces define a variety of methods for inspecting an existing tree, yet they do not declare any update methods. Presuming that a newly constructed tree is empty, we would like to have means for changing the structure of content of a tree.
+ Although the principle of encapsulation suggests that the outward behaviors of an abstract data type need not depend on the internal representation, the efficiency of the operations depends greatly upon the representation. We therefore prefer to have each concrete implementation of a tree class support the most suitable behaviors for updating a tree. In the case of a linked binary tree, we suggest that the following update methods be supported:
  - `addRoot(e)`: Creates a root for an empty tree, storing e as the element, and returns the position of that root; an error occurs if the tree is not empty.
  - `addLeft(p, e)`: Creates a left child of position p, storing element e, and returns the position of the new node; an error occurs if p already has a left child.
  - `addRight(p, e)`: Creates a right child of position p, storing element e, and returns the position of the new node; an error occurs if p already has a right child.
  - `set(p, e)`: Replaces the element stored at position p with element e, and returns the previously stored element.
  - `attach(p, T1 , T2 )`: Attaches the internal structure of trees T 1 and T 2 as the respective left and right subtrees of leaf position p and resets T1 and T2 to empty trees; an error condition occurs if p is not a leaf.
  - `remove(p)`: Removes the node at position p, replacing it with its child (if any), and returns the element that had been stored at p; an error occurs if p has two children.

See code [here](https://replit.com/@ZhangNing1/CSCI241NingZhang#CSCI241/LinkedBinaryTree.java)
