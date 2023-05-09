## 1. What are the key differences between classes and objects in Python, and how are they used to create and manage instances of a class?

__Objects__ are an encapsulation of variables and functions into a single entity. Objects get their variables and functions from classes. <br>
__Classes__ are essentially a template to create your objects.

1. assigin class to object
2. passing to class variables and functions using ( DOT notation)

## 2.Explain the concept of recursion and provide an example of how it can be used to solve a problem in Python. What are some best practices to follow when implementing a recursive function?

__A recursive function__ is a function defined in terms of itself via self-referential expressions.

- This means that the function will continue to call itself and repeat its behavior until some condition is met to return a result. 
- All recursive functions share a common structure made up of two parts: base case and recursive case.
**Decompose the original problem into simpler instances of the same problem. This is the recursive case:

       n! = n x (n−1) x (n−2) x (n−3) ⋅⋅⋅⋅ x 3 x 2 x 1
       n! = n x (n−1)!


- As the large problem is broken down into successively less complex ones, those subproblems must eventually become so simple that they can be solved without further subdivision. This is the base case:

      n! = n x (n−1)! 
      n! = n x (n−1) x (n−2)!
      n! = n x (n−1) x (n−2) x (n−3)!
      ⋅
      ⋅
      n! = n x (n−1) x (n−2) x (n−3) ⋅⋅⋅⋅ x 3!
      n! = n x (n−1) x (n−2) x (n−3) ⋅⋅⋅⋅ x 3 x 2!
      n! = n x (n−1) x (n−2) x (n−3) ⋅⋅⋅⋅ x 3 x 2 x 1!

- Here, 1! is our base case, and it equals 1.

### Behind the scenes, each recursive call adds a stack frame (containing its execution context) to the call stack until we reach the base case. Then, the stack begins to unwind as each call returns its results:

    def factorial_recursive(n):
    # Base case: 1! = 1
    if n == 1:
        return 1

    # Recursive case: n! = n * (n-1)!
    else:
        return n * factorial_recursive(n-1)


## 3. What is the purpose of pytest fixtures and code coverage in testing Python code? Explain how they can be used together to improve the quality and maintainability of a project.

__Pytest fixtures__ allow you to set up and tear down test objects or data before and after running tests. Fixtures are functions that return data, objects or resources that are needed for tests, and can be used across multiple tests.

__Code coverage__ is a measure of the amount of code that has been executed during the testing process. It can help identify untested or under-tested areas of your codebase, which can help improve the quality and reliability of your code.

### using pytest fixtures and code coverage together can help you write more maintainable, reliable, and efficient tests, which can lead to higher-quality Python projects.

### When used together, pytest fixtures and code coverage can help improve the quality and maintainability of your Python projects by providing a standardized way of creating test data and ensuring that your tests cover as much of your codebase as possible.
