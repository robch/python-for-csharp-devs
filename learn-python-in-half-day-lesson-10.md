# Lesson 10: Object-Oriented Programming (10 minutes)

Welcome to Lesson 10! In this lesson, we'll introduce you to classes and objects in Python, which are fundamental concepts of object-oriented programming (OOP). We'll compare Python's approach to OOP with C#'s class-based approach.

## Classes and Objects in Python:
In Python, a class is a blueprint for creating objects. It defines a set of attributes (variables) and methods (functions) that the objects of the class will have. An object is an instance of a class, representing a specific entity with its own unique state.

**Example 1: Creating a Class**
```python
# Class definition
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def greet(self):
        print(f"Hello, my name is {self.name} and I am {self.age} years old.")
```

To create an object of the class, you simply call the class as if it were a function, passing any required arguments.

**Example 2: Creating Objects from a Class**
```python
# Creating objects
person1 = Person("John", 30)
person2 = Person("Alice", 25)
```

## Accessing Object Attributes and Methods:
You can access the attributes and methods of an object using the dot notation.

**Example 3: Accessing Object Attributes and Methods**
```python
# Accessing attributes and methods
print(person1.name)    # Output: John
print(person2.age)     # Output: 25

person1.greet()        # Output: Hello, my name is John and I am 30 years old.
person2.greet()        # Output: Hello, my name is Alice and I am 25 years old.
```

## Inheritance in Python:
Python supports class inheritance, allowing you to create a new class based on an existing class (the parent or base class). The new class (the child or derived class) inherits the attributes and methods of the parent class.

**Example 4: Inheritance in Python**
```python
# Parent class
class Animal:
    def __init__(self, species):
        self.species = species

    def sound(self):
        print("Some generic animal sound.")

# Child class
class Dog(Animal):
    def sound(self):
        print("Woof! Woof!")

dog = Dog("Canine")
print(dog.species)   # Output: Canine
dog.sound()         # Output: Woof! Woof!
```

## Key Differences for C# Developers:
- Python uses the `class` keyword to define classes, similar to C#'s class-based approach to OOP.
- In Python, the `__init__` method is a special method (constructor) called when creating an object from a class. It initializes the object's attributes.
- Python's dot notation is used to access object attributes and methods, similar to C#'s member access operator (`.`).
- Inheritance in Python is defined by using parentheses after the class name in the child class definition, followed by the parent class name.

Now that you've learned about classes and objects in Python, you have a solid foundation in object-oriented programming. You're ready to explore more advanced topics and build more complex projects using Python!

## Additional Resources:
- Python Classes and Objects: https://docs.python.org/3/tutorial/classes.html

## Practice Project:
- Create a `Rectangle` class with attributes `length` and `width`. Add methods to calculate the area and perimeter of the rectangle. Create two `Rectangle` objects and print their attributes and calculated values.

🔗 [.. Back to TOC](./learn-python-in-half-day-lesson--toc.md)