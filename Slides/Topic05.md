# CSCI 241
# Topic 5: Recursion

# 1. The Recursion Pattern
+ `Recursion`: when a method calls itself
+ Classic example – the factorial function:

~~~~
n! = n*(n-1)*(n-2)*....*2*1
~~~~

+ Recursive definition:

![fact1](../Resources/fact1.png)

# 2. Content of a Recursion Method

+ Base case(s):
  - Values of the input variables for which we perform no recursive calls are called base cases (there should be at least one base case).
  - Every possible chain of recursive calls must eventually reach a base case.
+ Recursive calls
  - calls to the recursive method
  - each recursive call should be defined so that it makes progress towards a base case.
+ Visualizing Recursion
  - A box for each recursive call
  - An arrow from each caller to callee
  - An arrow from each callee to caller showing return value
![factorial recursion](https://bigaidream.gitbooks.io/subsets-of-algorithms/content/basic_algo/recursion/etc/factorial_flowchart.PNG)

# 3. Binary search
+ Search for an integer in an ordered array.
+ We consider three cases:
  - If `target` equals `data[mid]`, then we have found the `target`,
  - If `target` < `data[mid]`, then we recur on the first half of the sequence.
  - If `target` > `data[mid]`, then we recur on the second half of the sequence.

![binary search](https://miro.medium.com/max/898/1*0OJ3eF9eO3FlPl5A_RtCSw.png)
