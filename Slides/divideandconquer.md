# Divide and Conquer
## 1. Introduction
This technique can be divided into the following three parts:
+ **Divide**: This involves dividing the problem into smaller sub-problems.
+ **Conquer**: Solve sub-problems by calling recursively until solved.
+ **Combine**: Combine the sub-problems to get the final solution of the whole problem.

![Divide and Conquer](https://i.imgur.com/Gmt6i6F.png)

## 2. Examples
[Complete the code here](https://replit.com/@ZhangNing1/CSCI241NingZhang#CSCI241/DivideandConquer.java)
### 2.1 merge-sort
To sort a sequence `S` with `n` elements using the three divide-and-conquer steps, the merge-sort algorithm proceeds as follows:
+ **Divide**: If S has zero or one element, return S immediately; it is already sorted. Otherwise (S has at least two elements), remove all the elements from S and put them into two sequences, S1 and S2, each containing about half of the elements of S; that is, S1 contains the first ⌊n/2⌋ elements of S, and S2 contains the remaining ⌈n/2⌉ elements.
+ **Conquer**: Recursively sort sequences S1 and S2.
+ **Combine**: Put the elements back into S by merging the sorted sequences S1 and S2 into a sorted sequence.

~~~~
step 1: start
step 2: declare array and left, right, mid variable
step 3: perform merge function.
    if left > right
        return
    mid= (left+right)/2
    mergesort(array, left, mid)
    mergesort(array, mid+1, right)
    merge(array, left, mid, right)
step 4: Stop
~~~~
![merge sort](https://media.geeksforgeeks.org/wp-content/uploads/20220722205737/MergeSortTutorial.png))


### 2.2 quick-sort
Quick sort picks an element as a pivot and partitions the given array around the picked pivot. There are many different versions of quickSort that pick pivot in different ways. 
+ Always pick the first element as a pivot.
+ Always pick the last element as a pivot (implemented below)
+ Pick a random element as a pivot.
+ Pick median as the pivot.

We divide `S` into subsequences, recur to sort each subsequence, and then combine the sorted subsequences by a simple concatenation. In particular, the quick-sort algorithm consists of the following three steps"
+ `Divide`: If S has at least two elements (nothing needs to be done if S has zero or one element), select a specific element `x` from S, which is called the pivot. As is common practice, choose the pivot `x` to be the last element in S. Remove all the elements from S and put them into three sequences:
  - L, storing the elements in S less than x
  - E, storing the elements in S equal to x (Of course, if the elements of S are distinct, then E holds just one element—
the pivot itself.)
  - G, storing the elements in S greater than x
+ Conquer: Recursively sort sequences L and G.
+ Combine:Put back the elements into S in order by first inserting the elements of L, then those of E, and finally those of G.

![quick sort](https://www.geeksforgeeks.org/wp-content/uploads/gq/2014/01/QuickSort2.png)

+ Pseudocode for QuickSort

~~~~
/* low  –> Starting index,  high  –> Ending index */
quickSort(arr[], low, high) {
    if (low < high) {
        /* pi is partitioning index, arr[pi] is now at right place */
        pi = partition(arr, low, high);
        quickSort(arr, low, pi – 1);  // Before pi
        quickSort(arr, pi + 1, high); // After pi
    }
}
~~~~

+ Pseudo code for partition() 

~~~~
/* This function takes last element as pivot, places the pivot element at its correct position in sorted array, and places all smaller (smaller than pivot) to left of pivot and all greater elements to right of pivot */

partition (arr[], low, high)
{
    // pivot (Element to be placed at right position)
    pivot = arr[high];  
    i = (low – 1)  // Index of smaller element and indicates the 
    // right position of pivot found so far
    for (j = low; j <= high- 1; j++){
        // If current element is smaller than the pivot
        if (arr[j] < pivot){
            i++;    // increment index of smaller element
            swap arr[i] and arr[j]
        }
    }
    swap arr[i + 1] and arr[high])
    return (i + 1)
}
~~~~

## Other Examples
+ LeetCode 0004, 0023, 0053, 0241, 0169, 0050, 0014
