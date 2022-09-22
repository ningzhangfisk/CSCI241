# 4.3 Deques
## 4.3.1 Introduction
+ a queue-like data structure that supports insertion and deletion at both the front and the back of the queue.
+ Such a structure is called a double- ended queue, or deque, which is usually pronounced `deck`.
+ The deque abstract data type is more general than both the stack and the queue ADTs.
+ Application example: a restaurant using a queue to maintain a waitlist
  - Occasionally, the first person might be removed from the queue only to find that a table was not available; typically, the restaurant will reinsert the person at the first position in the queue.It may also be that a customer at the end of the queue may grow impatient and leave the restaurant.


![deque](https://s3.ap-south-1.amazonaws.com/s3.studytonight.com/tutorials/uploads/pictures/1627372174-103268.png)

## 4.3.2 Operations
+ `addFirst(e)`: Insert a new element e at the front of the deque.
+ `addLast(e)`: Insert a new element e at the back of the deque.
+ `removeFirst()`: Remove and return the first element of the deque(or null if the deque is empty).
+ `removeLast()`: Remove and return the last element of the deque(or null if the deque is empty).
+ `first()`: Returns the first element of the deque, without removing it(or null if the deque is empty)
+ `last()`: Returns the last element of the deque, without removing it(or null if the deque is empty).
+ `size()`: Returns the number of elements in the deque.
+ `isEmpty()`: Returns a boolean indicating whether the deque is empty.

## 4.3.3 Implementing a Deque with a Circular Array
+ a representation similar to the [ArrayQueue class](https://replit.com/@ZhangNing1/CSCI241NingZhang#CSCI241/ArrayQueue.java).
+ treating the array in circular fashion and storing the index of the first element and the current size of the deque as fields
+ the index of the last element can be calculated, as needed, using modular arithmetic.
  - When removing the first element, the front index is advanced in circular fashion, with the assignment `first = (first+1) % N`, where N is the length of the array.
  - **One concern**: when an element is inserted at the front, the first index must effectively be decremented in circular fashion and it is a mistake to assign `first = (first−1) % N`. The problem is that when `first` is 0, the goal should be to “decrement” it to the other end of the array, and thus to index N−1. However, a calculation such as −1 % 10 in Java results in the value −1. A standard way to decrement an index circularly is instead to assign `first = (first−1+N) % N`. Adding the additional term of N before the modulus is calculated assures that the result is a positive value. 
+ See code [here](https://replit.com/@ZhangNing1/CSCI241NingZhang#CSCI241/ArrayDeque.java)
## 4.3.4 Implementing a Deque with a Doubly Linked List
+ the `DoublyLinkedList` class from [Section 3.3](DoubleList.md) already implements the entire Deque interface.
+ See code [here](https://replit.com/@ZhangNing1/CSCI241NingZhang#CSCI241/ListDeque.java)
