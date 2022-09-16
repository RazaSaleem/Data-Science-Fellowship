# Introduction to Python
## Contents
1.	Python Introduction
2.	Hello world in python
3.	Variables and types 
4.	Lists


## Python Introduction
Python is an interpreted high-level, programming language. It is a popular general-purpose programming language. It is used in machine learning, web development, desktop applications, and many other fields. Fortunately for beginners, Python has a simple, easy-to-use syntax. This makes Python a great language to learn for beginners. <br>


## Hello world! In python 
Create a program named Hello World that is quite basic. A straightforward program that displays Hello, World! is called "Hello, World!" on the display. It's frequently used to introduce a new programming language to beginners because it's a very basic program. <br>

Save the following code as hello world.py in any text editor or IDE. <br>
```Python

print("Hello, world!")

```
Then, run the file. You will get the following output. <br>

```Python
Hello, world!
```

Congratulations! You just wrote your first program in Python. <br>

You can see that it was a somewhat simple task. This is what makes the Python programming language so beautiful. <br>


## Variables and types 
Python is a type-inferred language, so you don't have to explicitly define the variable type. It automatically knows that apple.com is a string and declares the website variable as a string.
One more thing we don’t need to declare the variables before using them like other languages e.g., C, java <br>
We will discuss few basis types of variables <br>
### 1.	Numbers
-	Integer
-	Float
	
Integer example to define integer use the following syntax <br>
```python
my_int = 5
print (my_int)
```
The output will be 
```Python
5
```

**Float example to define Float use the following syntax** <br>
```python
my_float = 4.0
print(my_float)

# we can also do this 
myfloat = float(5)
print(myfloat)
```
The output will be <br>
```python
4.0
5.0
```

### 2.	String
An array of Unicode characters is a string. To represent strings, we can use single or double quotations. Triple quotes can be used to indicate multi-line strings.<br>

```pthon
str_s = ‘world’
print(str_s)
str_d = “hello! Dear xyz”
print(str_d)
str_m = ‘’’ This is multiline 
string’’’
print(str_m)
```
Out of the above will be <br>
```python
World
Hello! Dear xyz
This is multiline
String
```
*The difference between the two is that using double quotes makes it easy to include apostrophes (whereas these would terminate the string if using single quotes)* <br>

```python
str_dob = “Don’t worry about the apostrophes”
print(str_dob)
```

```python
Don’t worry about the apostrophes
```


**We can assign values to multiple variable "simultaneously at same time** <br>
```python
x, y, z = 5, 6, 8
print(x, y, z)

```
Output wil be <br>

```python
5 6 8
```

**We can do simple operations with numbers and strings** <br>
```python
num1 = 3
num2 = 7
sum = num1 + num2
print(sum)

Saleem = “Saleem”
Raza = “Raza”
print(Saleem + “ “ + Raza)

```

Output the above code <br>
```python
10
Saleem Raza
```

**Applying operators’ operation on numbers and strings is not supported in python** <br>

```python
# This will give error
num_1 = 3
num_2 = 9
Hi = “Hi”

print(num_1 + num_2 + Hi)
```

Output as below
```python

Traceback (most recent call last):
  File "<stdin>", line 6, in <module>
    print(num_1 + num_2 + Hi)
TypeError: unsupported operand type(s) for +: 'int' and 'str'

```

## Lists
List is an ordered sequence of items. It is one of the most used datatypes in Python and is very flexible. Arrays and lists have a lot in common. They are open to containing any kind of variable and any number of variables. Additionally, lists may be iterated over quite easily. Here's a guide on how to create a list. <br>
```python
my_list  = [1,2, ‘python’]
print(my_list)
```

Output
```python
[1, 2, ‘python’]
```
  *Lists are mutable, meaning, the value of elements of a list can be altered.* <br>

```python
mylist  = [1,2, 3,4]
mylist[3] = 5
print(my_list)
```

Output <br>
```python
[1, 2, 3, 5]
```
### Some of list methods are useful while dealing or working with List in python
**append ()**
Add a single element to the end of the list

**clear ()**
Removes all Items from the List

**copy ()**
returns a shallow copy of the list

**count ()**
returns count of the element in the list

**extend ()**
adds iterable elements to the end of the list

**index ()**
returns the index of the element in the list

**insert ()**
insert an element to the list

**pop ()**
Removes element at the given index

**remove ()**
Removes item from the list

**reverse ()**
reverses the list

**sort ()**
sorts of elements of a list
