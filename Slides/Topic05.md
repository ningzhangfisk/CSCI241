<script
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"
  type="text/javascript">
</script>


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
+ We consider four cases:
  - If `low` > `high`, then we could not found the `target`.
  - If `target` equals `data[mid]`, then we have found the `target`.
  - If `target` < `data[mid]`, then we recur on the first half of the sequence.
  - If `target` > `data[mid]`, then we recur on the second half of the sequence.

![binary search](https://miro.medium.com/max/898/1*0OJ3eF9eO3FlPl5A_RtCSw.png)

+ Base cases:
  - `low > high`
  - `target == data[mid]`
+ Recursive calls
  - `target` < `data[mid]
  - `target` > `data[mid]`

+ Analyze binary search
  - Each recursive call divides the search region  in half. Hence, there can be at most `log(n)` levels.(We will learn the details in next topic)

# 4. Fibonacci Numbers
+ Fibonacci numbers are defined recursively:

![fibonacci](http://jwilson.coe.uga.edu/EMAT6680Su07/Brown/Assignment%2012/image62.gif)

+ Recursive algorithm(binary recursive method)

~~~~
Algorithm: Fibonacci(n):
  Input: non-negative integer n
  Output: the nth Fibonacci number Fn
  if n=0 or n=1 then
    return n
  else
    return Fibonacci(n-1) + Fibonacci(n-2)
~~~~

# 5. Recursive Issues

![Recursive Issues](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTgL7qjMSKVvgITDfi4PqHmwNPZNm6pVfLNR9Nytb7oIXZWiunsO_XSZkyoexQErYgxpDk&usqp=CAU)


