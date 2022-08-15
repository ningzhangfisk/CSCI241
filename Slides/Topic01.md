# CSCI241 - Data Structures and Algorithms
# Dr. Ning Zhang
# Topic 1: Introduction to CSCI241
# 1. Data structures and algorithms
## 1.1 Why Data structures and algorithms(DSA)?
+ CSCI241 and CSCI241L are in the Balance Sheet.
+ DSA is one of the CS core courses.
  - <details>
    <summary>Click to expand!</summary>
  
    + Computer Architecture
    + Computer Networks
    + Operating Systems
    + Database
    + Programming Languages
    + ...
    + **Data structures and algorithms**
  </details>
+ Data structures and algorithms are the building blocks of large software systems.
+ By the time you learn how to use these techniques, you will have a **great chance of getting a job**.
+ If you learn how to use data structures and algorithms, it will make your life easier. You will be able to solve many problems using this knowledge.
+ [See more reasons here](https://dev.to/codewithshan/13-reasons-to-learn-data-structures-and-algorithms-2022-bbl#:~:text=Computer%20scientists%20use%20data%20structures,systems%20for%20their%20research%20projects.&text=This%20is%20a%20subject%20that,in%20data%20structures%20and%20algorithms.&text=You%20can%20learn%20this%20skill%20for%20free.)

## 1.2 What are Data Structures?
+ Data structure is a storage that is used to store and organize data. It is a way of arranging data on a computer so that it can be accessed and updated efficiently.
+ Depending on your requirement and project, it is important to choose the right data structure for your project.
### 1.2.1 Types of Data Structures
+ Primitive vs Non-primitive

![Primitive vs Non-primitive](https://www.tutorialscan.com/wp-content/uploads/2018/11/Data-Structure-Types.png)

+ **Linear vs. Non-linear**

![Linear vs. Non-linear](https://media.geeksforgeeks.org/wp-content/uploads/20191010170332/Untitled-Diagram-183.png)

#### 1.2.1.1 Linear data structures
+ In linear data structures, the elements are arranged in sequence one after the other. Since elements are arranged in particular order, they are easy to implement.
+ However, when the complexity of the program increases, the linear data structures might not be the best choice because of operational complexities.
+ **Array**: In an array, elements in memory are arranged in continuous memory. All the elements of an array are of the same type. And, the type of elements that can be stored in the form of arrays is determined by the programming language.

![Array](https://beginnersbook.com/wp-content/uploads/2018/10/array.jpg)

+ **Stack**: In stack data structure, elements are stored in the LIFO principle. That is, the last element stored in a stack will be removed first. It works just like a pile of plates where the last plate kept on the pile will be removed first.

![Stack](http://www.technotaught.com/wp-content/uploads/2018/11/stack-1.jpg)

+ **Queue**: Unlike stack, the queue data structure works in the FIFO principle where first element stored in the queue will be removed first. It works just like a queue of people in the ticket counter where first person on the queue will get the ticket first.

![Queue](https://cdn.programiz.com/sites/tutorial2program/files/queue.png)

+ **Linked List**: In linked list data structure, data elements are connected through a series of nodes. And, each node contains the data items and address to the next node.

![linked list](https://www.tutorialspoint.com/data_structures_algorithms/images/dsa_linkedlist.jpg)

#### 1.2.1.2 Non-Linear data structures
+ Unlike linear data structures, elements in non-linear data structures are not in any sequence. Instead they are arranged in a hierarchical manner where one element will be connected to one or more elements.
+ Non-linear data structures are further divided into graph and tree based data structures.

+ **Graph**: In graph data structure, each node is called vertex and each vertex is connected to other vertices through edges.

![Graph](https://miro.medium.com/max/1838/1*ippUFJwESODRk9SQK4Fn8Q.png)

+ **Tree**: Similar to a graph, a tree is also a collection of vertices and edges. However, in tree data structure, there can only be one edge between two vertices.

![tree](https://cdn.programiz.com/sites/tutorial2program/files/tree_0.png)

#### 1.2.1.3 Summary
|Linear|Non-linear|
|----|----|
|The data items are arranged in sequential order, one after the other.|The data items are arranged in non-sequential order (hierarchical manner).|
|All the items are present on the single layer.|The data items are present at different layers.|
|It can be traversed on a single run. That is, if we start from the first element, we can traverse all the elements sequentially in a single pass.|It requires multiple runs. That is, if we start from the first element it might not be possible to traverse all the elements in a single pass.|
|The memory utilization is not efficient.|Different structures utilize memory in different efficient ways depending on the need.|
|The time complexity increase with the data size.|Time complexity remains the same.|
|Example: Arrays, Stack, Queue|Example: Tree, Graph, Map|

## 1.3 What is an Algorithm?
+ In computer programming terms, an algorithm is a set of well-defined instructions to solve a particular problem. It takes a set of input(s) and produces the desired output.
~~~~
An algorithm to add two numbers:

1. Take two number inputs
2. Add numbers using the + operator
3. Display the result
~~~~
+ Qualities of a Good Algorithm
  - Input and output should be defined precisely.
  - Each step in the algorithm should be clear and unambiguous.
  - Algorithms should be most effective among many different ways to solve a problem.
  - An algorithm shouldn't include computer code. Instead, the algorithm should be written in such a way that it can be used in different programming languages.
    + [Pseudocode](https://en.wikipedia.org/wiki/Pseudocode)


# 1.3.1 Classic Algorithm Interview Questions
## 1.3.1.1 [String matching](https://en.wikipedia.org/wiki/String-searching_algorithm)
+ Given a string `str1="I love Fisk, I love Fisk University, I love Fisk University"` and a substring `str2="Fisk University"`,
+ Find if `str1` contains `str2`. If so, return the position of the first occurence, otherwise, return -1.
+ Complete the matching/searching as soon as possible
+ Your solution?
  - Brutal force
  - [KMP](https://en.wikipedia.org/wiki/Knuth%E2%80%93Morris%E2%80%93Pratt_algorithm)(`partial match table`) 

## 1.3.1.2 Tower of Hanoi
+ [Play the game here](https://www.mathplayground.com/logic_tower_of_hanoi.html)
+ Divide-and-Conquer
## 1.3.1.3 [8 Queens](https://en.wikipedia.org/wiki/Eight_queens_puzzle#:~:text=The%20eight%20queens%20puzzle%20is,in%20the%20mid%2D19th%20century.)
+ The eight queens puzzle is the problem of placing eight chess queens on an 8×8 chessboard so that no two queens threaten each other; thus, a solution requires that no two queens share the same row, column, or diagonal. There are 92 solutions. The problem was first posed in the mid-19th century. In the modern era, it is often used as an example problem for various computer programming techniques.

![chessboard](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d7/Chessboard480.svg/312px-Chessboard480.svg.png)

+ [Play the game here.](https://www.brainmetrix.com/8-queens/)
+ number of answers?
  - Gauss: 72
  - Mathematical way (Graph theory): 92
  - Divide-and-Conquer: 92
+ [Divide-and-conquer algorithm](https://en.wikipedia.org/wiki/Divide-and-conquer_algorithm)

## 1.3.1.4 [Knight's tour](https://en.wikipedia.org/wiki/Knight%27s_tour)
+ A knight's tour is a sequence of moves of a knight on a chessboard such that the knight visits every square exactly once. If the knight ends on a square that is one knight's move from the beginning square (so that it could tour the board again immediately, following the same path), the tour is closed (or re-entrant); otherwise, it is open.
+ [Play the game here.](http://www.maths-resources.com/knights/)
+ Solution: DFS + Greedy Algorithm
  - [DFS: Depth-first_search](https://en.wikipedia.org/wiki/Depth-first_search)
  - [Greedy Algorithm](https://en.wikipedia.org/wiki/Greedy_algorithm)


## 1.4 How to become a DSA expert?
+ Take this course to learn DAS fundamentals.
+ More practices.
  - [LeetCode](https://leetcode.com/)
  - [LeetCode Solutions](https://ningzhangfisk.github.io/CSCI241/Resources/leetcode%20solutions.pdf)
+ Real-world projects and applications.

# 2. Java Programming Language
+ Go through Chapters 1 and 2 in the textbook or any tutorial online to review Java programming language.
  - See the handouts for these two chapters [here](../Handouts)
+ You can use any online/offline text editor or IDE in this class. 
  - Text editor: Notepad++, Sublime, VI, Emacs...
  - IDE: Ecllipes, BlueJ, IntelliJ,...
+ I will be using an online IDE named [Replit](https://replit.com/)
  - [Replit Documentations](https://docs.replit.com/category/getting-started)
## 2.1 An example
+ [Two dimensional array](https://replit.com/@ZhangNing1/CSCI241#CSCI241/Array.java)


# References
+ [DSA Introduction](https://www.programiz.com/dsa/algorithm)
+ [13 Reasons to Learn DSA](https://dev.to/codewithshan/13-reasons-to-learn-data-structures-and-algorithms-2022-bbl#:~:text=Computer%20scientists%20use%20data%20structures,systems%20for%20their%20research%20projects.&text=This%20is%20a%20subject%20that,in%20data%20structures%20and%20algorithms.&text=You%20can%20learn%20this%20skill%20for%20free.)
