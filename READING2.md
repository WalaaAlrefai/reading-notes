# Testing and Modules

## why this topic matters


## Reading Questions
 ### 1. What are the key principles of Test-Driven Development (TDD) in Python, and how do they contribute to the overall quality of code?<br>
 __Test Driven Development__ is the process in which test cases are written before the code that validates those cases. It depends on repetition of a very short development cycle.<br> __Test driven Development__ is a technique in which automated Unit test are used to drive the design and free decoupling of dependencies

__Benefits:__

 - Unit test provides constant feedback about the functions.
 - Quality of design increases which further helps in proper maintenance.
 - Test driven development act as a safety net against the bugs.
 - TDD ensures that your application actually meets requirements defined for it.
 - TDD have very short development lifecycle.

### 2. Explain the purpose of the if \_\_name\_\_ == '\_\_main\_\_': statement in Python scripts. What are some use cases for including this conditional in your code?

used in Python scripts to __control the execution of the script__. It checks the value of the __name__ attribute, which is a built-in variable that is set by the Python interpreter when a script is executed.
###execute the code only if it is called as a script and not execute when it is imported as a module.
- used to import and test modules in Python. This can be useful for testing and debugging purposes. Because it allows you to run a module’s test functions without having to import the module into another script.
 - statement should be used in a Python script when you want to control the execution of the script based on whether it is being run directly or being imported as a module by another script.
  - statement can be used to define the entry point of a Python script that is intended to be run from the command line.

### 3. Describe the concept of recursion in Python.
The term __Recursion__ can be defined as the process of defining something in terms of itself. In simple words, it is a process in which a function calls itself directly or indirectly. 

### 4. What is the difference between Python modules and packages? Explain how to create, import, and use them in your Python programs.
__Modules in Python__
A module is a file with the extension.py that contains Python or C executable code. A module is made up of a number of Python statements and expressions. 

__Packages in Python__
To provide an application development environment, a python package establishes a hierarchical directory structure with several modules and sub-packages. They are nothing more than a bundle of modules and sub-packages.

### differencies

 - A Package is a directory containing numerous modules and sub-packages, whereas a Module is a.py file containing Python code. 
 - An __init__  .py file is required to create a package. There is no such necessity when it comes to creating modules.
 - We can import all objects in a module at once by using the asterisk (*) operator but we can’t import all modules in a package at once.

 ### how to create ,import ,and use modules?

  - __Create__<br>
 def display():
    print("modulename")
if __name__ == "__main__":
    display()
 - We can import a module by using the import keyword
 ### how to create, import, and use them?

 - To create a Python package, we need to create a directory with a __init__.py file and a module.
 - To import ==>
 import pkgname
 modulename.display()