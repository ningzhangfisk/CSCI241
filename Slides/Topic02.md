# CSCI241: Data Structures and Algorithms
# Dr. Ning Zhang
# Topic 2: Arrays
+ One dimensional arrays(section 3.1 in textbook)
+ Two dimensional arrays()
+ Sparse matrices

# 2.1 One dimensional arrays
## 2.1.1 Introduction
+ Array is a container which can hold a fix number of items and these items should be of the same type.
+ Following are the important terms to understand the concept of Array.
  - **Element** − Each item stored in an array is called an element.
  - **Index** − Each location of an element in an array has a numerical index, which is used to identify the element.
  
![element index](https://www.tutorialspoint.com/data_structures_algorithms/images/array_representation.jpg)

+ As per the above illustration, following are the important points to be considered.
  - Index starts with 0.
  - Array length is 10 which means it can store 10 elements.
  - Each element can be accessed via its index. For example, we can fetch an element at index 6 as 27.
  
## 2.1.2 Basic Operations
+ Following are the basic operations supported by an array.
  - **Traverse** − print all the array elements one by one.
  - **Insertion** − Adds an element at the given index.
  - **Deletion** − Deletes an element at the given index.
  - **Search** − Searches an element using the given index or by the value.
  - **Update** − Updates an element at the given index.
  - **Sort** - Sort elements in order(we will learn this in later topics).

### 2.1.2.1 Create an array
+ Method 1: $$elementType[] arrayName = {initialValue0, initialValue1, ..., initialValueN-1};$$
~~~~
// example
int[] nums = {1,2,3,4,5};
~~~~
