# Object Oriented Programming Note #1
---
## What is an Object?
* In OOP, and object is a combination of data and functional code
* Like real-world objects, objects in OOP have states and behavior
## Object Oriented Programming
* For creating modular, reusable software. 
* Designs programs through creating Objects which you can provide functionality to
* Focuses on the definition of data
Object's Data -> attributes
Object's Code -> methods
## Classes and Objects
Class -> A class is a a template for creating objects. It is a user-defined data type that contains data (attributes) and methods that operate on that data.
* Attributes are an objects accessible tools. 
* Fields are variables which belong to an object or class
    * Type 1: belongs to an instance of a class
    * Type 2: belongs to the class itself
* Methods are functions that the object can call
Note: Class names are capitalized 
## __init__ method and self parameter
* Executed as soon as an object of the class is intiated
* Allows us to intialize an objects attributes
* self denotes that the method is accessible for the object itself
* self attributes are treated as local

## Encapsulation
* Restricting access to certain attributes of the class/object.
* In Python, attributes are hidden by using a __ (double underscore), as prefix.

**Setter and Getter Methods (Accessing Encapsulated Attributes)**
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
Explaination: 
* Even though __firstName is encapsulated, getFirstName is not encapsulated.
* Since getFirstName is inside the Student class, getFirstName can retrieve and “pass on” the student name to somewhere outside the class
## Overrides
Overloading: Two methods in the same class that have the name, but different parameters. (Overloading is not possible in Python 3)
Overriding: Two methods with the same method name and parameters.
* One method is in the parent class 
* One method is in the child class 
* Overriding allows the child class to provide different implementation for a method that exists in the parent class
* Overriding can also be done with built-in magic-methods or base-functions
## Polymorphism




