# scope in Python
- how variables and names are looked up in your code.
- It determines the visibility of a variable within the code 
- The scope of a name or variable depends on the place in your code where you create that variable
- The Python scope concept is generally presented using a rule known as the LEGB rule:

    ***__Local, Enclosing, Global, and Built-in scopes.__***
**
 ## local and global scope.

__Global :__

    Trying to update a global variable from within a function:

<code>

        counter = 0  # A global name
       >>> def update_counter():
       ... counter = counter + 1  # Fail trying to update counter
       ...
       >>> update_counter()
       Traceback (most recent call last):
       File "<stdin>", line 1, in <module>
       File "<stdin>", line 2, in update_counter

       UnboundLocalError: local variable 'counter' referenced before assignment

</code>


- As you can see above, this did not work. Now let's see what happens when you use the global statement:

<code>

    >>> counter = 0  # A global name
    >>> def update_counter():
    ...     global counter  # Declare counter as global
    ...     counter = counter + 1  # Successfully update the counter
    ...
    >>> update_counter()
    >>> counter
    1
    >>> update_counter()
    >>> counter
    2
    >>> update_counter()
    >>> counter
    3

</code>

- As you can see, adding the global keyword allowed us to update the global scoped counter from inside the function.
- __Note:__ The use of global is considered bad practice in general. If you find yourself using global to fix problems like the one above, then stop and think if there is a better way to write your code. For example, you can try to write a self-contained function that relies on local names rather than on global names as follows:

<code>

     >>> global_counter = 0  # A global name
     >>> def update_counter(counter):
     ...     return counter + 1  # Rely on a local name
     ...
     >>> global_counter = update_counter(global_counter)
     >>> global_counter
     1
     >>> global_counter = update_counter(global_counter)
     >>> global_counter
     2
     >>> global_counter = update_counter(global_counter)
     >>> global_counter
     3

</code>

__Nonlocal :__

    The following example shows how you can use nonlocal to modify a variable defined in the enclosing or nonlocal scope:
  
<code>
  
    >>> def func():
    ...     var = 100  # A nonlocal variable
    ...     def nested():
    ...         nonlocal var  # Declare var as nonlocal
    ...         var += 100
    ...
    ...     nested()
    ...     print(var)
    ...
    >>> func()
    200

</code>

- With the statement nonlocal var, you tell Python that you’ll be modifying var inside nested().
- You can’t use a nonlocal statement in either the global scope or in a local scope. Here’s an example:

<code>

    >>> nonlocal my_var  # Try to use nonlocal in the global scope
    File "<stdin>", line 1
    SyntaxError: nonlocal declaration not allowed at module level
    >>> def func():
    ...     nonlocal var  # Try to use nonlocal in a local scope
    ...     print(var)
    ...
    File "<stdin>", line 2
    SyntaxError: no binding for nonlocal 'var' found

</code>



## purpose and importance of Big O notation in the context of 
   algorithm analysis.

- Big O Time: Basically how long it takes an algorithm to do things.
- Big O Space: ^How much memory that algorithm takes while doing it.
- __Why is it necessary?__ It is a good way to compare algorithms and determine performance/efficiency.
- Big O is also useful for measuring how an algorithm will respond to an increasing amount of data it has to process.
- Big O notation will always give you the worst scenerio.
  - O(1): Constant running time
  - O(log n): Logarithmic running time
  - O(n): Linear running time
  - O(n logn): Log-linear running time
  - O(n^k): Polynominal running time.
  - O(c^n): Exponential running time.



## Based on the Rolling Dice Example
 -  simulating a dice roll using Python: 
      Here we will be using the random module since we randomize the dice simulator for random outputs.

 - Function used:<br>
   __random.randint()__ : This function generates a random number in the given range. Below is the implementation.
