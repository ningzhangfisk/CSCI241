# Backtracking Algorithm
# 1. Introduction
+ Backtracking: An brute force search algorithm that avoids unnecessary searches.  
+ Using the idea of trial and error, we search for the solution of the problem during the search attempts, and when we reach a certain step of exploration, we find that the original choice does not satisfy the solution conditions, or we need to satisfy more solution conditions, we go back one step (backtracking) and choose again
+ This technique of going back if it does not work is called "backtracking", and the point of a state that satisfies the backtracking condition is called "backtracking point".
+ In short, the backtracking algorithm adopts an algorithmic idea of "backtracking if it does not work".
+ Backtracking algorithms are usually implemented using simple recursive methods, and two situations are more likely to arise when performing backtracking.
  - Finding a correct answer that may exist.
  - Declaring that the problem has no answer after trying all possible distribution methods.

# 2. Understanding backtracking algorithms from the permuation problem.

[LeetCode Permutations](https://leetcode.com/problems/permutations/)

Taking the example of solving the full permutation of `[1, 2, 3]`, we will explain the procedure of the backtracking algorithm.
+ 1. Permuations starting with `1`.
  - 1.1 If you select 2 as the middle number, you can only select 3 as the last number, i.e., `[1, 2, 3]`.
  - 1.2 Undo the selection of 3 as the last number, and then undo the selection of 2 as the middle number. Then select 3 as the middle number, then only 2 can be selected as the last number, i.e., the permutaion is [1, 3, 2].

+ 2. Undo 2 as the last number, undo 3 as the middle number, undo 1 as the first number, then select 2 as the first number
  - 2.1 Select 1 as the middle number, you can only select 3 as the last number, i.e., `[2,1,3]`
  - 2.2 Undo the selection of 3 as the last number, and then undo the selection of 1 as the middle number. Then select 3 as the middle number, then only 1 can be selected as the last number, i.e., the permutaion is [2, 3, 1].

+ 3. Undo 1 as the last number, undo 3 as the middle number, undo 2 as the first number, then select 3 as the first number
  - 2.1 Select 1 as the middle number, you can only select 2 as the last number, i.e., `[3,1,2]`
  - 2.2 Undo the selection of 2 as the last number, and then undo the selection of 1 as the middle number. Then select 2 as the middle number, then only 1 can be selected as the last number, i.e., the permutaion is [3, 2, 1].

To summarize the permuation backtracking process
+ The numbers that may appear on each position are enumerated in order, and the numbers that have appeared before cannot appear again for the next number to be selected.
+ For the position:
  - 1. `Select an element`: Select an element from the list of available elements that has not appeared before.
  - 2. `Recursive search`: Starting from the selected element, the remaining numbers are recursively searched one level at a time until **a boundary condition is encountered**, then no further search is performed.
  - 3. `Undo selection`: Undo the previously selected element one layer at a time and move on to another branch of the search. Until all possible paths are completely traversed

+ For the above decision process, we can also use a decision tree to represent it as follows.

![above decision process](../Resources/permutation.png)

+ From the decision tree we can see that
  - Each layer has one or more different nodes, and these nodes and the branches connected to them represent "different options"
  - Each node represents a 'state' for permutation problem, and these states are represented by 'different values'
  - Going a level down is to select an "element" from the "list of available elements" and add it to the "current state"
  - Going a level upwards is to remove the selected "element" from the "current state" and backtrack to the state it would have been in if the element had not been selected (or reset the state), so that other branches can be explored.


+  Code

~~~~~
class Solution {
    public List<List<Integer>> permute(int[] nums) {
        List<List<Integer>> list = new ArrayList<>();// store all the permutations
        List<Integer> tempList = new ArrayList<>(); // store the current permutation
        // Arrays.sort(nums); // not necessary
        backtrack(list, tempList, nums);
        return list;
    }

    private void backtrack(List<List<Integer>> list, List<Integer> tempList, int [] nums){
        if(tempList.size() == nums.length){ // find a permuation (the condition is true)
            list.add(new ArrayList<>(tempList)); // add the current permutation into list
        } else{
            for(int i = 0; i < nums.length; i++){ //enumerate all the elements we can choose
                if(tempList.contains(nums[i])) continue; // element already exists, skip
                tempList.add(nums[i]);                   // select the element
                backtrack(list, tempList, nums);         // backtracking search
                tempList.remove(tempList.size() - 1);    // undo the selection
            }
        }
    } 
}
~~~~~
