# Python Modules & Packages 
## Contents
1.	Python Module <br>
2.	Python Packages <br>

## Python Module
A module helps you to structure your Python code logically. Grouping related code into modules makes it easier to comprehend and use the code. A module is a Python object that has attributes with arbitrary names that you can bind and reference.<br>

Module is a file that contains code to perform a specific task. A module may contain variables, functions, classes etc.<br>

**Example of Module** <br>
 
Let's construct a module. Enter the next text and name the file test.py. <br>
```python
def print_func( par ):
   print "Hello : ", par
   return

```
### The import statement <br>
By using an import statement in another Python source file, you can utilise any Python source file as a module. The syntax for the import is as follows:<br>
```python
import test
```
If the module is found in the search path when the interpreter comes across an import statement, it is imported. Before importing a module, the interpreter scans a list of directories called a search path. For instance, you would place the following command at the top of the script to import the module test.py:<br>

**Example of Importing a module and function**<br>
```python

# Import module support
import test

# Now you can call defined function that module as follows
test.print_func("Saleem Raza")

```

### from import statement
Python's from statement lets you import specific attributes from a module into the current namespace. The from...import has the following syntax –<br>
```python
from random import shuffle
numbers = [1, 23, 44, 77, 91, 21]
random.shuffle(numbers)
>>> numbers
[21, 44, 1, 77, 23, 92]
```

## Python Packages
Let's say you've created a sizable application with numerous modules. If all the modules are put in one place, it gets harder to keep track of them as the number increases. This is especially true if their names or functions are similar. You might need a way to categories and arrange them. A directory must contain <br>
```python
__init__.py
```
The module namespace can be organized hierarchically using packages and dot notation. Similar to how modules assist in preventing name conflicts between global variables, packages assist in preventing name conflicts between module names.<br>

Since a package uses the operating system's built-in hierarchical file structure, creating one is rather simple. Think about the following configuration:<br>
**Example**

### Importing module from a package
We can import modules from packages using the dot (.) operator.<br>
For example, if we want to import the start module it can be done as follows:<br>
```python
import Car.machine
```
Now, if this module contains a function named engine(), we must use the full name to reference it.<br>
```python
Car.machine.engine()
```
If this construct seems lengthy, we can import the module without the package prefix as follows:<br>

```python
from Car.parts import glass

```

We can now call the function simply as follows:<br>
```python
parts.glass()

```

