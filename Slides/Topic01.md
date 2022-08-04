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

# 1. Classic Algorithm Interview Questions
## 1.1 [String matching](https://en.wikipedia.org/wiki/String-searching_algorithm)
+ Given a string `str1="I love Fisk, I love Fisk University, I love Fisk University"` and a substring `str2="Fisk University"`,
+ Find if `str1` contains `str2`. If so, return the position of the first occurence, otherwise, return -1.
+ Complete the matching/searching as soon as possible
+ Your solution?
  - Brutal force
  - [KMP](https://en.wikipedia.org/wiki/Knuth%E2%80%93Morris%E2%80%93Pratt_algorithm)(`partial match table`) 

## 1.2 Tower of Hanoi
+ [Play the game here](https://www.mathplayground.com/logic_tower_of_hanoi.html)
+ Divide-and-Conquer
## 1.3 [8 Queens](https://en.wikipedia.org/wiki/Eight_queens_puzzle#:~:text=The%20eight%20queens%20puzzle%20is,in%20the%20mid%2D19th%20century.)
+ The eight queens puzzle is the problem of placing eight chess queens on an 8×8 chessboard so that no two queens threaten each other; thus, a solution requires that no two queens share the same row, column, or diagonal. There are 92 solutions. The problem was first posed in the mid-19th century. In the modern era, it is often used as an example problem for various computer programming techniques.

![chessboard](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d7/Chessboard480.svg/312px-Chessboard480.svg.png)

+ [Play the game here.](https://www.brainmetrix.com/8-queens/)
+ number of answers?
  - Gauss: 72
  - Mathematical way (Graph theory): 92
  - Divide-and-Conquer: 92
+ [Divide-and-conquer algorithm](https://en.wikipedia.org/wiki/Divide-and-conquer_algorithm)

## 1.4 [Knight's tour](https://en.wikipedia.org/wiki/Knight%27s_tour)
+ A knight's tour is a sequence of moves of a knight on a chessboard such that the knight visits every square exactly once. If the knight ends on a square that is one knight's move from the beginning square (so that it could tour the board again immediately, following the same path), the tour is closed (or re-entrant); otherwise, it is open.
+ [Play the game here.](http://www.maths-resources.com/knights/)
+ Solution: DFS + Greedy Algorithm
  - [DFS: Depth-first_search](https://en.wikipedia.org/wiki/Depth-first_search)
  - [Greedy Algorithm](https://en.wikipedia.org/wiki/Greedy_algorithm)
# 2. The importance of data structures and algorithms
+ **The algorithm is the soul of the program**, and a good program can maintain the high speed of computation even when the huge amount of data is calculated.
 




