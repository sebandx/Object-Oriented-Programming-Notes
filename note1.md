# Object Oriented Programming
---
## What is an Object?
* An object is a combination of data and functional code
* Objects have states and behavior
## Object Oriented Programming
* For creating modular, reusable software through focusing on the definition of data.
* Designs programs through creating objects which you can provide functionality to
Object's Data -> attributes
Object's Code -> methods
## Classes and Objects
Class -> A class is a template for creating objects. It is a user-defined data type that contains data (attributes) and methods that operate on that data.
* Attributes are objects accessible tools. 
* Fields are variables which belong to an object or class. It can either belong to...
    * An instance of a class
    * The class itself
* Methods are functions that the object can call
Note: Class names are always capitalized 
## ```__init__``` method and self parameter
* Executed as soon as an object of the class is initiated
* Allows us to initialize an object's attributes
* self means that the method is accessible for the object itself
* self attributes are local to the instance of the class

Example:
```python
class Rectangle:
    def __init__(self, width, height): # Intializes attributes of the rectangle class: width and height
        self.width = width
        self.height = height
    def area(self):
        return self.width * self.height
```

## Encapsulation
* Restricting access to certain attributes of the class/object.
* In Python, attributes are hidden by using double underscores as prefixes.

### Setter and Getter Methods (Accessing Encapsulated Attributes)
```python
class Student:
  def __init__(self,nameF, nameL, num):
    self.__firstName = nameF
    self.__lastName = nameL
    self.__studentNumber = num
  
  def setFirstName(self, newName): # Setter method
    self.__firstName = newName
    
  def getFirstName(self): # Getter method
    return self.__firstName
```
Explanation: 
* Even though firstName is encapsulated, getFirstName is not encapsulated.
* Since getFirstName is inside the Student class, getFirstName can retrieve and return the student name to somewhere outside the class
## Overrides
Overloading: Two methods in the same class that have the name, but different parameters. (Overloading is not possible in Python 3)
Overriding: Two methods with the same method name and parameters.
* One method is in the parent class 
* One method is in the child class 
* Overriding allows the child class to provide different implementation for a method that exists in the parent class
* Overriding can also be done with built-in magic-methods or base-functions
## Polymorphism
A method that can be used throughout different classes and objects that is dependent on parameters. 
* Different Classes (non-inherited) can have methods with the same names. 
* A set of inherited classes can also have the same methods.
```python
class Bear:
    def sound(self):
        print("Groarrr")
 
class Dog:
    def sound(self):
        print("Woof woof!")
 
def makeSound(animalType):
    animalType.sound()
bearObj = Bear()
dogObj = Dog()
 
makeSound(bearObj)
makeSound(dogObj)
```
This is an example polymorphism (the sound method exists in both the Bear and Dog class).
### Polymorphism and Inheritance
* Overloading is an example of polymorphism, however it's illegal in python 3. Overloading is when a class or function to have multiple implementations of the same method.
* Overriding is another example of polymorphism and is legal. It is when inherited classes modify inherited methods from the parent class. 
Example of Overloading:
```python
class Person:
    def __init__(self, name, age):
        self.__name = name
        self.__age = age

    def show(self):
        return self.__name

    def show(self, num):
        return "%s %d" % (self.__name, self.__age)
```
### Base Overrides
* Overriding methods in a child class that were inherited from a parent class.
* It's also possible to override built in methods that we use in Python. 
Example:
```python
class Dog:
	def __init__(self,name):
		self.__name = name
	
	def __str__(self):
		return “Woof, I’m %s.” % self.__name

corgi = Dog(“Tobasco”)
print(corgi) → “Woof, I’m Tobasco.”
```
Overriding can allow you to manipulate how an object behaves with built in functions. For example it can allow you to...
* Perform mathematical operations on custom objects
* Compare equality between two custom objects
**repr base function**
* In order to make custom objects printable, the ``` __str__``` and ```__repr__``` method need to be overridden
	* ```__repr__``` allows us to present a printable version of the object
	* ```__str__``` converts the object into a string

## Inheritance 
When an object or class is based on another class.
* The child class will inherit its features from a parent class. 
* A child class will receive all the attributes and methods of the parent class. 
* A child can then add new attributes and new methods.
* A child class can also override attributes and methods 
* A child class does not need to a new ```__init__``` method unless it requires new attributes
### Types of Inheritance
* Single Inheritance: When a child class inherits the features of one parent class. 
* Multiple Inheritance: When a child class inherits features from multiple parent classes. 
* Multilevel Inheritance: When a child class inherits from another class which inherited from another class...
### super() method
* a built-in method for classes to refer to their parent class
* Helps us avoid doing ParentClass.method(self) to avoid confusion
Note: In general inheritance should be avoided. This is because modifying a parent class could easily break the child classes, making less convinient to modify your code. 
## Iterable Objects
* Objects you can iterate through like a sequence
* The portion of the iterable object must be a sequence
* Even if a object is iterable it may not be indexable







