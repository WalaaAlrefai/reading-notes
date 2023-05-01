## Data Structures and Algorithms
### Recursion:
it is a function that calls it self directly or indirectly and the corresponding function is called a recursive function. Using recursive algorithm, certain problems can be solved quite easily.
Data Structure :
A data structure is a storage that is used to store and organize data. It is a way of arranging data on a computer so that it can be accessed and updated efficiently.
 

### BIG O:
Big O notation is a mathematical notation that describes the limiting behavior of a function when the argument tends towards a particular value or infinity. It is a member of a family of notations invented by Paul Bachmann, Edmund Landau, and others, collectively called Bachmann–Landau notation or asymptotic notation.

__1. What is 1 of the more important things you should consider when deciding which data structure is best suited to solve a particular problem?__
the choice of data structure depends on the specific problem's requirements, including the types of operations involved, efficiency considerations, memory constraints, access patterns, and concurrency requirements. Analyzing these factors will help you select the most suitable data structure for your problem.
__2.How can we ensure that we’ll avoid an infinite recursive call stack?__

Define a base case to stop the recursion.
Ensure each recursive call progresses towards the base case.
Consider limiting recursion depth or utilizing tail recursion optimization for efficiency.