# Object-Oriented-Programming

# Slideshow 1 Notes:
---

**Objects:**
  - There are two types of objects.
  - **In computer science**, an object is reffered as a variable, a data structure, a function, or a method. it is reffered as an identifier in computer science.
  - **In Object Orientated Porgramming**, it is similar to an object in computer science but the difference is that an in OOP is an instance of a **class** where this object can either be a variable or function, data structure or even a combinationof such.

### **The OOP Paradigm**: 
~ **OOP** is a programming practice to design modular reusable software systems
~ **OOP** uses definitions to interpret code
~ **OOP** makes programs with the creation of **Objects**

**Procedure Orientated**:
~ A human may require to be: 
  - Logical
  - must be able to complete tasks
  - must be able to complete tasks other can do

**OOP**:
~ creating a human object:
  - A Name attribute
  - A Home attribute
  - A attribute that can relate to other humans (ex.likes and dislikes)

**Classes and Objects**:
- Class is an abstract description of all objects that can be made from a set classwhere an object can be instantiated from.
- Classes contain attributes
- An attribute is an **Objects** accessible tool
- Fields are variables that belong to an object or class
- Mehtods are functions that 

**OOP in Python 3**
~ Class is a keyword built into python 3 that allows to create our own classes
[*example*](https://docs.google.com/presentation/d/1wJ1SqLBaVSahdJUO41QRkyyLDmXpMWCROxV5TzdWsvU/edit#slide=id.g2a79f171fd_0_28)

```# Person Class
class Person:
	pass # An Empty Block
#end of Person Class

student1 = Person() #student1 is now a Person Object
print(student1)
```
- Methods in python 3 are declared as new functions
- initializing method is used as soon as an object is called upon in a class
- self perameter is used to denote that the method is applied and accesible for the object itself
- self will also treat its own attribute as local
- The double underscore can overrite built in python features

# Slideshow 2:

Encapsulation:

- **encapsulation** is Information Hiding. It's basically restricting the access to the classes and objects certain attributes and methods
- **encapsulation** can be used for data protection and restricting certain methods to callable
- To hide attributes and methods, you use the double underscore **__** as a prefix

[*example*](https://docs.google.com/presentation/d/1BSBVPl27YKaFtiNa_6EPyUd5gnM5o60fKHdrmtp2jGk/edit#slide=id.g2a84dd718b_0_9)
```class Student:
  def __init__(self,nameF, nameL, num):
    self.firstName = nameF
    self.lastName = nameL
    self.__studentNumber = num
  
  def __getStudentNumber(self):
    return self.__studentNumber

#end of Student
s1 = Student("Mr.", "Park", 10)
print(s1.__getStudentNumber()) # Will cause an error
print(s1.__studentNumber) # Will also cause an error
```
**Overides**:
Overloading:
  - Two methods in one class that have the same method name, but different parameters
Overriding:
  - Two methods with the same method name and parameters

# Note, You can overload in python 3 #






