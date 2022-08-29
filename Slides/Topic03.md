# CSCI241
# Dr. Ning Zhang
# Topic 3: Lists
+ Singly Linked Lists(section 3.2 in textbook)
+ Circularly Linked Lists(section 3.3 in textbook)
+ Doubly Linked Lists(section 3.4 in textbook)

# 3.1 Singly Linked Lists

![single list0](../Resources/single_list-0.png)

## 3.1.1 Introduction



+ A singly linked list is a concrete data structure consisting of a sequence of nodes, starting from a head pointer.

![single list2](../Resources/single_list-2.png)

+ Each node stores
  - element
  - link to the next node

![single list1](../Resources/single_list-1.png)

+ For `Singly Linked List` data structure, we use [SingleLinkedList class](https://replit.com/@ZhangNing1/CSCI241NingZhang#CSCI241/SingleLinkedList.java).

## 3.1.2 Operations
+ **traverse**: To traverse all the nodes one after another.
+ **insert**: To add a node at the given position.
+ **delete**: To delete a node.
+ **search**: To search an element(s) by value.
+ **update**: To update a node.
+ **sort**: To arrange nodes in a linked list in a specific order.(not covered in this topic)
+ **merge**: To merge two linked lists into one.

### 3.1.2.1 traverse
+ The idea here is to step through the list from beginning to end.
+ The algorithm for traversing a list
  - Start with the head of the list. Access the content of the head node if it is not null.
  - Then go to the next node(if exists) and access the node information
  - Continue until no more nodes (that is, you have reached the null node)
### 3.1.2.2 insert
+ There can be three cases that will occur when we are inserting a node in a linked list.
  - Insertion at the head
  - Insertion at the tail (Append)
  - Insertion after a given node or position
+ **Insertion at the head**
  - step 1: Allocate memory for `new node` and store data
  - step 2: Change `next` of new node to point to `head`
  - step 3: Change `head` to point to `new node`

  ![single list3](../Resources/single_list-3.png)
  
+ **Insertion at the tail**
  - step 1: Allocate memory for `new node` and store data
  - step 2: Traverse to last node(or use `tail` attribute)
  - step 3: Change `next` of last node to `new node`
  - step 4: change `tail` to point to `new node`

![single list4](../Resources/single_list-4.png)

+ **Insertion after a node**
  - step 1: Allocate memory for `new node` and store data
  - step 2: Change `next` of `new node` to `next` of `previous node`
  - step 3: Change `next` of `previous node` to `new node`

![single list5](../Resources/single_list-5.png)

+ **Insert after a position**
  - step 1: Allocate memory for `new node` and store data
  - step 2: Traverse to node just before the required position of new node(e.g., if we need to insert a node after the 4th node, the key is to start from the `head` and find the 4th node or `next` of the 3rd node, then define it as `prevNode`)
  - step 3: follow the same steps(steps 2 and 3) in **Insertion after a node** operation

### 3.1.2.3 delete
+ To delete a node from a linked list, we need to do these steps
  - Deletion at the head
  - Deletion at the tail (Append)
  - Deletion at a given node or position

+ **Delete head**
  - step 1: Change `head` to point to `next` of `head`

![single list7](../Resources/single_list-7.png)

+ **Delete tail**
  - step 1: traverse to find `previous node` before `tail`
  - step 2: change `tail` to `previous node`
  - step 3: change `next` of new `tail` to `null`

![single list8](../Resources/single_list-8.png)

+ **Delete node**
  - step 1: traverse to find `previous node` before `delete node`
  - step 2: change `next` of `previous node` to `next` of `delete node`

![single list9](../Resources/single_list-9.png)

### 3.1.2.4 search
+ Traverse the list to compare the `element` of each node with the `key` value
+ Return `true` if the `key` matches `element`
+ Return `false` if no match in the entire list

![single list10](../Resources/single_list-10.png)

### 3.1.2.5 update

+ Update the first element with `key` value to `newValue`
+ Traverse the list to compare the `element` of each node with the `key` value
+ Update `element` to `newValue` if the `key` matches `element`

![single list11](../Resources/single_list-11.png)

### 3.1.2.6 merge
+ change `next` of `tail` of the first list to `head` of the second list
+ change `next` of the first list  to `next` of the second list


![single list12](../Resources/single_list-12.png)

# References
+ [Types of Linked List and Operation on Linked List](https://afteracademy.com/blog/types-of-linked-list-and-operation-on-linked-list)
