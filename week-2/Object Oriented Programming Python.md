# OOP in python 

## Contents
1.	Python OOP Introduction
2.	Creating Classes and Objects
3.	Principles of OOP 
4.	Lists


## Python OPP Introduction
The programming paradigm known as "object-oriented programming" offers a way to organize programs so that individual objects are composed of properties and behaviors.
An object might, for instance, represent a person by having attributes like a name, age, and address as well as actions like running, talking, breathing, and walking. Alternatively, it might stand in for an email, complete with attributes like a recipient list, subject, and text as well as actions like attaching files and sending.

## Creating Classes and Objects  
Numbers, strings, and lists, which are examples of primitive data structures, are intended to represent basic pieces of information like the price of an apple, the title of a poem, or your favorite colors. What if you wish to illustrate a more complicated idea?
Let's take the example of vehicle a vehicle may a type, brand, model and so on, this type of information is stored in variables called attributes, and a vehicle can drive stop, honk its horn so, these are behaviors in OOP called methods. 

**Class:** A class is a user-defined blueprint or prototype from which objects are created. Class creates a user-defined data structure, which holds its own data members and member functions, which can be accessed and used by creating an instance of that class. <br>

```python
Class vehicle:
	Pass
```
**Objects:** An Object is an instance of a Class. A class is like a blueprint while an instance is a copy of the class with actual values. <br>
```python
Veh1 = vehicle()
```
**An object consists of:** <br>
State: It is represented by the attributes of an object. It also reflects the properties of an object. <br>
Behavior: It is represented by the methods of an object. It also reflects the response of an object to other objects.<br>
Identity: It gives a unique name to an object and enables one object to interact with other objects. <br>

**The self parmater:** <br>
•	Class methods must have an extra first parameter in the method definition. We do not give a value for this parameter when we call the method, Python provides it.<br>
•	If we have a method that takes no arguments, we still have one argument. <br>
•	This is similar to this pointer in C++ and this reference in Java. <br>

When we call a method of this object as myobject.method(arg1, arg2), this is automatically converted by Python into MyClass.method(myobject, arg1, arg2) this is all the special self is about. <br>


**The __init__ method** <br>
The __init__ method is similar to constructors in C++ and Java. Constructors are used to initialize the object’s state. Like methods, a constructor also contains a collection of statements(i.e. instructions) that are executed at the time of Object creation. It runs as soon as an object of a class is instantiated. The method is useful to do any initialization you want to do with your object.<br>

**Example class and object**
```python

class vehicle:
	“This is vehicle class”
# The init method or constructor
def __init__(self, brand, model, type):
		# Instance Variables or attributes
self.brand = brand
		self.model = model
		self.type  = type 

# Insatiate the vehicle class
veh1 = vehicle(‘Mercedes-Benz’, ‘Mercedes C 300 e’, ‘Car’)
veh2 = vehicle(‘Ford’, ‘F-150’, ‘Truck’)

# accessing the attributes
print(veh1.brand, veh1.model, veh1.type)
print(veh2.brand, veh2.model, veh2.type)
```

**Methods**<br>
methods are functions that are defined inside a class and can only be called from an instance of that class. Just like. __init__(), an instance method’s first parameter is always self.<br>


 ```python
class vehicle:
	“This is vehicle class”
# The init method or constructor
def __init__(self, brand, model, type):
		# Instance Variables or attributes
self.brand = brand
		self.model = model
		self.type  = type
		self.gas_tank_size = 14
		self.fuel_level = 0

	def fuel_up(self):
		self.fuel_level = self.gas_tank_size
		print(‘Gass tank is full now’)
	
	def drive(self):
		print(f’The {self.model} is now driving.’)

```


## Principles of OOP 
•	Inheritance <br>
•	Encapsulation <br>
•	Abstraction <br>
•	Polymorphism <br>
### Inheritance
A key component of object-oriented programming is class inheritance. By incorporating properties and methods from parent classes, this enables you to extend your classes. One class immediately has access to all of the attributes and methods of the parent class when it inherits from another. In the child class, you can override parent class methods and attributes as well as introduce new ones. When defining a new class, the name of the parent class is included in parenthesis in order to inherit from another class. see Composition Over Inheritance as well.<br>

**Example of Inheritance**<br>
Create a class named vehicle, with brand, type and model properties, and a disp_prop method:<br>

 ```python
class vehicle:
	“This is vehicle class”
# The init method or constructor
def __init__(self, brand, model, type):
		# Instance Variables or attributes
self.brand = brand
		self.model = model
		self.type  = type
		
	def disp_prop(self):
		print(self.brand, self.model, self.type)
	


	#Use the vehicle class to create an object, and then execute the disp_prop method:

	veh = vehicle(“Mercedes-Benz”, “Mercedes C 300 e”, “Car”)
	veh.disp_prop()
```

**Creating a Child Class**<br>
To create a class that inherits the functionality from another class, send the parent class as a parameter when creating the child class:<br>
Create a class named Electric_vehicle, which will inherit the properties and methods from the vehicle class:<br>
**Example of Child Class**<br>

 ```python
class Electric_vehicle:
	“This is Electric_vehicle class”
# The init method or constructor
def __init__(self, brand, model, type):
		super().__init__(brand, model, type)
		self.battery_size = 85
		self.charge_level = 0
	
def charge(self):
        	self.charge_level = 100
        	print('The vehicle is now charged.')

    	def fuel_up(self):
        	print('This vehicle has no fuel tank!')

	#Use the child and parent methods:

	E_veh = Electric_vehicle(‘Ford’, ‘F-150’, ‘Truck’)
	E_veh.disp_prop()
	E_veh.charge()
	E_veh.fuel_up()
```
### Encapsulation
In Python, the idea of combining data and methods into one unit is known as encapsulation. Thus, creating a class indicates that you are implementing encapsulation. A class is a good illustration of encapsulation since it unifies all the methods and data members (instance variables) into a single entity.<br>
•	Encapsulation is the packing of data and methods into a class so that you can hide the information and restrict access from outside.<br>
•	Prefix an attribute with a single underscore (_) to make it private by convention.<br>
•	Prefix an attribute with double underscores (__) to use the name mangling <br>

**Access Modifiers in Python** <br>
By designating a class's data members and methods as private or protected, encapsulation can be accomplished. Direct access modifiers like public, private, and protected are not available in Python. Utilizing single and double underscores will help us do this.<br>
Access modifiers control who can access a class's variables and methods. Private, public, and protected are the three types of access modifiers offered by Python.<br>

•	**Public Member:** Accessible anywhere from outside class.<br>
•	**Private Member:** Accessible within the class <br>
•	**Protected Member:** Accessible within the class and its sub-classes <br>

 

we can’t access the private variable from the outside of that class. <br>
We can access private members from outside of a class using the following two approaches<br>
•	Create public method to access private members<br>
•	Use name mangling <br>

**Public method to access private members**<br> 
**Example:** Access Private member outside of a class using an instance method<br>


 ```python
class Employee:
    # constructor
    def __init__(self, name, salary):
        # public data member
        self.name = name
        # private member
        self.__salary = salary

    # public instance methods
    def show(self):
        # private members are accessible from a class
         print("Name: ", self.name, 'Salary:', self.__salary)

# creating object of a class
emp = Employee('Jessa', 10000)

# calling public method of the class
emp.show()

```
**Name Mangling to access private members**<br>
Through name mangling, we can directly access private and protected variables from outside of a class. Two leading underscores and one trailing underscore are added to an identifier to generate a name mangling, such as this: _classname dataMember, where classname is the name of the current class and data member is the name of the private variable.<br>

**Example:** Access private member<br>
```python
class Employee:
    # constructor
    def __init__(self, name, salary):
        # public data member
        self.name = name
        # private member
        self.__salary = salary

# creating object of a class
emp = Employee('Jessa', 10000)

print('Name:', emp.name)
# direct access to private member using name mangling
print('Salary:', emp._Employee__salary)

```

### Abstraction
In Python, abstraction is described as the technique of dealing with complexity by hiding superfluous information from the user. This is a fundamental concept in object-oriented programming (OOP) languages. This allows the user to build even more complex logic on top of the provided abstraction without having to understand or even consider all of the hidden background/back-end complexity.<br>

Abstraction in Python works by incorporating abstract classes and methods.<br>

**Abstract Class:** A class specified in the code that has abstract methods is named Abstract Class.<br>
**Abstract Method:** Here, it doesn’t have any implementation. All the implementations are done inside the sub-classes.<br>

**Example of Abstraction**<br>

 ```python
class Shape:
    __metaclass__ = ABCMeta 
    def __init__ (self, shapeType):
        ”’Objective: To initialize object of class Shape Input Parameters:
        self (implicit parameter) – object of type Shape
        shapeType – string
        Return Value: None
        ”’
        self.shapeType = shape Type
    @abstractmethod 
    def area(self) :
        pass
    @abstractmethod
    def perimeter (self):
        pass
class Rectangle(Shape):
    def __init__(self, length, breadth):
        ”’Objective: To initialize object of class Rectangle Input Parameters: self (implicit parameter) – object of type Rectangle length, breadth – numeric value 
        Return Value: None ”’
        Shape.__init__(self, ‘Rectangle’)
        self.length = length 
        self.breadth = breadth
    def area (self):
        ”’Objective: To compute area of the Rectangle Input Parameter: 
        self (implicit parameter) object of type Rectangle
        Return Value: numeric value
        ”’
        return self.length * self.breadth
    def perimeter (self):
        return 2 * (self.lenght + self.breadth)
class Circle (Shape):
    pi = 3.14
    def __init__ (self, radius):
        ”’Objective: To initialize object of class Circle Input Parameters: self (implicit parameter) – object of type Circle 
            radius – numeric value 
            Return Value: None”’
        Shape.__init__(self, ‘Circle’)
        self.radius = radius
    def area (self):
        ”’Objective: To compute the area of the Circle
        Input Parameter:
        self (implicit parameter) – object of type Circle 
        Return Value: area – numeric value”’
        return round(Circle.pi * (self.radius ** 2), 2)
    def perimeter(self):
        ``` Objective: To compute the perimeter of the Circle
        Input Parameter:
        self (implicit parameter) – object of type Circle
        Return Value: perimeter – numeric value```
        return round (2 * Circle.pi * self.radius, 2)
```
We indicate that a method is abstract by preceding its definition by @abstractmethod (function decorator). Note that the definition of an abstract class begins with
```
>>> rectangle = Rectangle (30, 15)
>>> rectangle.area ()
450
>>> rectangle.perimeter ()
90 
>>> circle = Circle (5)
>>> circle.area ()
78.5
>>> circle.perimeter ()
31.4

```

### Polymorphism
Polymorphism is derived from the Greek words poly (many) and morphism (change). That is, the same function name can be used for multiple types. This makes programming more intuitive and straightforward.<br>
A child class inherits all of the parent class's methods. In other cases, however, the method inherited from the parent class does not fully fit into the child class. In such circumstances, you must re-implement the method in the child class. Polymorphism can be used in a variety of ways in Python. Polymorphism can be defined using various functions, class methods, or objects.<br>

**Example of Polymorphism:** with inheritance <br>

```python
class Bird:
     def intro(self):
       print("There are different types of birds")
 
     def flight(self):
       print("Most of the birds can fly but some cannot")
 
class parrot(Bird):
     def flight(self):
       print("Parrots can fly")
 
class penguin(Bird):
     def flight(self):
       print("Penguins do not fly")
 
obj_bird = Bird()
obj_parr = parrot()
obj_peng = penguin()
 
obj_bird.intro()
obj_bird.flight()
 
obj_parr.intro()
obj_parr.flight()
 
obj_peng.intro()
obj_peng.flight()

```
Output

```python
There are different types of birds
Most of the birds can fly but some cannot
There are different types of bird
Parrots can fly
There are many types of birds
Penguins do not fly

```

