# Recursion
is a technique for solving problems by breaking them down into smaller subproblems and solving those subproblems recursively. It involves defining a function that calls itself with a smaller version of the original problem until the problem can be solved directly.

Here is a simple example of a recursive function that calculates the factorial of a given number using Python:

```python
def factorial(n):
  # Base case: factorial of 0 is 1
  if n == 0:
    return 1
  # Recursive case: calculate the factorial of n by multiplying it by the factorial of n - 1
  else:
    return n * factorial(n - 1)

print(factorial(5)) # Output: 120
```
In this example, the factorial function calls itself with a smaller version of the original problem (n - 1) until the base case is reached (n == 0). The results of the recursive calls are then combined to calculate the final result.

Recursion can be a powerful tool for solving problems, but it can also be computationally expensive, as it requires the creation of a new stack frame for each recursive call. It is important to use it judiciously and to have a clear base case to avoid infinite recursion.