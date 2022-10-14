# 1. Tower of Hanoi
# 1.1 Game Description
Tower of Hanoi is a mathematical puzzle where we have three rods (`A`, `B`, and `C`) and `N` disks. Initially, all the disks are stacked in decreasing value of diameter i.e., the smallest disk is placed on the top and they are on rod `A`. The objective of the puzzle is to move the entire stack to another rod (here considered `C`), obeying the following simple rules:
+ Only one disk can be moved at a time.
+ Each move consists of taking the upper disk from one of the stacks and placing it on top of another stack i.e. a disk can only be moved if it is the uppermost disk on a stack.
+ No disk may be placed on top of a smaller disk.

## 1.2 Examples:
[Play the game here](https://www.mathplayground.com/logic_tower_of_hanoi.html)

~~~~
Input: 2
Output: Disk 1 moved from A to B
Disk 2 moved from A to C
Disk 1 moved from B to C
~~~~


~~~~
Input: 3
Output: Disk 1 moved from A to C
Disk 2 moved from A to B
Disk 1 moved from C to B
Disk 3 moved from A to C
Disk 1 moved from B to A
Disk 2 moved from B to C
Disk 1 moved from A to C
~~~~

## 1.3 Tower of Hanoi using Recursion:
The idea is to use the helper node to reach the destination using recursion. Below is the pattern for this problem:
+ Shift `N-1` disks from `A` to `B`, using `C`.
+ Shift last disk from `A` to `C`.
+ Shift `N-1` disks from `B` to `C`, using `A`.

![HANOI 3](https://media.geeksforgeeks.org/wp-content/uploads/tower-of-hanoi.png)

Follow the steps below to solve the problem:
+ Create a function `towerOfHanoi` where pass the `N` (current number of disk), `from_rod`, `to_rod`, `aux_rod`.
+ Call `towerOfHanoi` to move the top `N – 1` disks from `from_rod` to `aux_rod`.
+ Move the last (Nth) disk  from `from_rod` to `to_rod`.
+ Call `towerOfHanoi` to move the `N – 1` disks from `aux_rod` to `to_rod`.

~~~~~
static void towerOfHanoi(int n, char from_rod, char to_rod, char aux_rod)
    {
        if (n == 0) {
            return;
        }
        towerOfHanoi(n - 1, from_rod, aux_rod, to_rod);
        System.out.println("Move disk " + n + " from rod "
                           + from_rod + " to rod "
                           + to_rod);
        towerOfHanoi(n - 1, aux_rod, to_rod, from_rod);
    }
 
    // Driver code
    public static void main(String args[])
    {
        int N = 3;
 
        // A, B and C are names of rods
        towerOfHanoi(N, 'A', 'C', 'B');
    }
~~~~~
