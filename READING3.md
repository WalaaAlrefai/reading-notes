## 1. What is the purpose of the ‘with’ statement when opening a file in Python, and how does it help manage resources while reading and writing files?

In Python, with statement is used in exception handling to make the code cleaner and much more readable. It simplifies the management of common resources like file streams.

there is no need to call file.close() when using with statement. The with statement itself ensures proper acquisition and release of resources. An exception during the file.write() call in the first implementation can prevent the file from closing properly which may introduce several bugs in the code, i.e. many changes in files do not go into effect until the file is properly closed. 
using the with statement makes the code compact and much more readable. Thus, with statement helps avoiding bugs and leaks by ensuring that a resource is properly released when the code using the resource is completely executed.

## 2. Explain the difference between the ‘read()’ and ‘readline()’ methods for file objects in Python. Provide examples of when to use each method.

read() reads all of the file's contents into a string, readline reads just a single line from the file 
<code>with open("test.txt", "r") as file:
    line = file.readline()
    print(line)
Will produce this output:

first line</code>

<code>with open("test.txt", "r") as file:
    content = file.read()
    print(content)
Output:

first line
second line
third line</code>

## 3.Briefly describe the concept of exception handling in Python. How can the ‘try’, ‘except’, and ‘finally’ blocks be used to handle exceptions and ensure proper execution of code? Provide a simple example.

exceptions are raised when some internal events occur which change the normal flow of the program.

Try and Except Statement :Statements that can raise exceptions are kept inside the try clause and the statements that handle the exception are written inside except clause. 

<code># Python program to handle simple runtime error
#Python 3

a = [1, 2, 3]
try:
print ("Second element = %d" %(a[1]))

Throws error since there are only 3 elements in array
	print ("Fourth element = %d" %(a[3]))

except:
	print ("An error occurred")
</code>

In the above example, the statements that can cause the error are placed inside the try statement (second print statement in our case). The second print statement tries to access the fourth element of the list which is not there and this throws an exception. This exception is then caught by the except statement.