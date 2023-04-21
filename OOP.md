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

*Overriding*
[*Exmaple*](https://www.geeksforgeeks.org/method-overriding-in-python/)
```
# Python program to demonstrate 
# method overriding
  
  
# Defining parent class
class Parent():
      
    # Constructor
    def __init__(self):
        self.value = "Inside Parent"
          
    # Parent's show method
    def show(self):
        print(self.value)
          
# Defining child class
class Child(Parent):
      
    # Constructor
    def __init__(self):
        self.value = "Inside Child"
          
    # Child's show method
    def show(self):
        print(self.value)
          
          
# Driver's code
obj1 = Parent()
obj2 = Child()
  
obj1.show()
obj2.show()
```
*Overloading*
[*Example*](https://www.javatpoint.com/what-is-operator-overloading-in-python)
```
class complex_1:  
    def __init__(self, X, Y):  
        self.X = X  
        self.Y = Y  
   
    # Now, we will add the two objects  
    def __add__(self, U):  
        return self.X + U.X, self.Y + U.Y  
   
Object_1 = complex_1(23, 12)  
Object_2 = complex_1(21, 22)  
Object_3 = Object_1 + Object_2  
print (Object_3)  
```

*Note, You can overload in python 3*

**Polymorphism**
 - Polymorphism is a method that cna be used across different classes and objects that are dependant on parameters

**Base overrides**:
 - when two **different** classes have the same attribute and methods
 - A child of a parent have an overrided method where the child would utilize the method differently
--------
[*Example*](https://docs.google.com/presentation/d/1BSBVPl27YKaFtiNa_6EPyUd5gnM5o60fKHdrmtp2jGk/edit#slide=id.g55ff3e348b_0_34)

-------

**Why override?**:
**Benifits**:
 - Can start to complete mathematical operations on custom **Objects**
 - Can also start to compare eqaulity between custom **Objects** 
*Note, we can manipulate how the **Object** behaves when met with built in methods and operators*

**__repr__() base functions**:
 - This function lets us control what cokes back from our repr() string

__repr__: Allows us to present a printable version of our object
__str__: Allows us to convert our object to a string

# SlideShow 3

**Inheritance**:

- When a object or class inherits features from the parent class
	- Single Inheritance: A subclass inheriting the features of a parent class
	- Multiple Inheritance: A subclass inheriting the features from multiple parent classes
	- Multilevel Inheritance: A subclass inhertting from a another subclass (*eg*, A -> B -> C)
- Inheritance can have a hierarchy or even be a hybrid
- A child will recieve all attributes and methods from the parent 
- A child can now enhance itself with the new attributes and methods it gained
- A child can override the attributes and methods to their own liking.
*Note, A child does not need a new __init__ () method unless it needs a new attribute*
~ Different types of Inheritance ~
	- Multi-Generational: Granparents -> Parents -> Child
	- Multi-Parent: Parent A and Parent B > child
	- Mixture of 1 and 2
[Example](https://docs.google.com/presentation/d/1Y_By4kpgBXSZrrpH0JwcwBKgZf3GcTAweFDXrnMZx-U/edit#slide=id.g55ff66ea53_0_14)

*Parent*
```class Person:
  def __init__(self, name):
  	self.__name = name 
  
  def getName(self):
    return self.__name
```

*Inheritance Class*
```class Student(Person):
  def __init__(self, name, num):
    Person.__init__(self, name)
    self.__sNum = num
  
  def getStudentName(self):
    return("%s: %s" % (self.__sNum,self.getName()))
```
-------
**Iterable Objects**:

- Iterable Objects are **Objects** that we can iterate through like a sequence 
- String and Lists are iterable
- to access indivdual values without indexing, we use for loops









