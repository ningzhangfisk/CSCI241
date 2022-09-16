# 4.2 Queues
## 4.2.1 Introduction
+ a close “cousin” of the stack
+ a collection of objects that are inserted and removed according to the `first-in, first-out (FIFO)` principle
+ elements can be inserted at any time, but only the element that has been in the queue the longest can be next removed.

![queue](https://simplesnippets.tech/wp-content/uploads/2019/04/queue-data-structure-diagram.jpg)

+ A metaphor for this terminology is a line of people waiting to get on an amusement park ride. People waiting for such a ride enter at the back of the line and get on the ride from the front of the line. 
+ There are many other applications
  - Stores, theaters, reservation centers, and other similar services typically process customer requests according to the FIFO principle.
  - FIFO queues are also used by many computing devices, such as a networked printer, or a Web server responding to requests.


## 4.1.2 Operations
Formally, the queue abstract data type defines a collection that keeps objects in a sequence, where element access and deletion are restricted to the first element in the queue, and element insertion is restricted to the back of the sequence.

+ `enqueue(e)`: Adds element e to the back of queue.
+ `dequeue()`: Removes and returns the first element from the queue (or null if the queue is empty).
+ `first()`: Returns the first element of the queue, without removing it (or null if the queue is empty).
+ `size()`: Returns the number of elements in the queue.
+ `isEmpty()`: Returns a boolean indicating whether the queue is empty.

## 4.1.3 Array-bases Queues
