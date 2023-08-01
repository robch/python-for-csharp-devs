# Lesson 9: Modules and Packages (10 minutes)

Welcome to Lesson 9! In this lesson, we'll learn how to organize code into modules and packages in Python. Modules and packages help break down large codebases into smaller, manageable units and facilitate code reuse.

## Modules in Python:
A module in Python is a file containing Python definitions and statements. The file name is the module name with the `.py` extension. You can access the functions, classes, and variables defined in a module using the `import` statement.

**Example 1: Creating and Importing a Module**
1. Create a file named `my_module.py` with the following content:
```python
# my_module.py

def greet(name):
    print(f"Hello, {name}!")

def add(a, b):
    return a + b
```

2. In another file, you can import and use the functions defined in `my_module.py`:
```python
# main.py

import my_module

my_module.greet("John")     # Output: Hello, John!
result = my_module.add(2, 3)
print(result)               # Output: 5
```

## Packages in Python:
A package in Python is a collection of modules organized in directories. A directory containing an empty file named `__init__.py` is considered a package. The `__init__.py` file can contain initialization code for the package.

**Example 2: Creating and Importing a Package**
1. Create a directory named `mypackage`.
2. Inside the `mypackage` directory, create two files:
   - `__init__.py` (can be empty)
   - `my_module.py` with the following content:
```python
# my_module.py

def greet(name):
    print(f"Hello, {name}!")

def add(a, b):
    return a + b
```

3. In another file, you can import and use the functions defined in `my_module.py` within the `mypackage` package:
```python
# main.py

from mypackage import my_module

my_module.greet("Alice")    # Output: Hello, Alice!
result = my_module.add(4, 6)
print(result)               # Output: 10
```

## Importing Specific Functions:
You can also import specific functions or variables from a module or package using the `from` keyword.

**Example 3: Importing Specific Functions from a Module**
```python
# main.py

from my_module import greet

greet("Bob")    # Output: Hello, Bob!
```

**Example 4: Importing Specific Functions from a Package**
```python
# main.py

from mypackage.my_module import add

result = add(8, 12)
print(result)   # Output: 20
```

## Key Differences for C# Developers:
- Modules in Python are similar to C#'s source files, but C# does not require an explicit import statement for files within the same project.
- Packages in Python are like C#'s namespaces but organized as directories containing `__init__.py` files.

Now that you've learned about modules and packages in Python, you're ready to move on to Lesson 10, where we'll explore object-oriented programming (OOP) in Python and compare it to C#'s class-based approach.

## Additional Resources:
- Python Modules and Packages: https://docs.python.org/3/tutorial/modules.html

## Practice Project:
- Organize the functions from the previous practice projects (area of rectangle and word lengths) into separate modules within a package. Import and use these functions in a new main script.

🔗 [.. Back to TOC](./learn-python-in-half-day-lesson--toc.md)