# Lesson 3: Data Types and Variables (10 minutes)

Welcome to Lesson 3! In this lesson, we'll explore Python's dynamic typing system and cover common data types like numbers, strings, lists, tuples, and dictionaries.

## Dynamic Typing in Python:
One of the key differences between Python and C# is Python's dynamic typing. In C#, you need to explicitly declare the data type of a variable before using it. In Python, however, you don't need to specify the data type explicitly. The data type is determined dynamically at runtime based on the value assigned to the variable.

**C# Code:**
```csharp
// C# - Explicitly declaring data type
int number = 42;
string name = "John";
```

**Python Equivalent:**
```python
# Python - Dynamic typing
number = 42
name = "John"
```

## Common Data Types in Python:

1. **Numbers:**
   - Integers (int): Whole numbers without a fractional part, e.g., 42, -10.
   - Floating-Point Numbers (float): Numbers with a decimal point or in scientific notation, e.g., 3.14, -2.5e2.

   **Python Code:**
   ```python
   # Numbers
   age = 30
   pi = 3.14
   ```

2. **Strings:**
   - Strings (str): Sequence of characters enclosed in single (' ') or double (" ") quotes.

   **Python Code:**
   ```python
   # Strings
   name = "Alice"
   message = 'Hello, Python!'
   ```

3. **Lists:**
   - Lists (list): Ordered collection of items, mutable (can be changed after creation).

   **Python Code:**
   ```python
   # Lists
   numbers = [1, 2, 3, 4]
   fruits = ['apple', 'banana', 'orange']
   ```

4. **Tuples:**
   - Tuples (tuple): Ordered collection of items, immutable (cannot be changed after creation).

   **Python Code:**
   ```python
   # Tuples
   point = (10, 20)
   rgb_color = (255, 128, 0)
   ```

5. **Dictionaries:**
   - Dictionaries (dict): Collection of key-value pairs, unordered, and mutable.

   **Python Code:**
   ```python
   # Dictionaries
   person = {'name': 'John', 'age': 30, 'occupation': 'developer'}
   ```

## Key Differences for C# Developers:
- Python allows you to assign values of different data types to the same variable during runtime, whereas C# requires explicit declaration and enforces strict typing.
- Python uses different syntax for strings, lists, tuples, and dictionaries compared to C#.

Now that you've learned about Python's dynamic typing and common data types, you're ready to move on to Lesson 4, where we'll explore Python's control flow statements.

## Additional Resources:
- Python Data Types: https://docs.python.org/3/library/stdtypes.html
- Python Lists, Tuples, and Dictionaries: https://docs.python.org/3/tutorial/introduction.html#lists

## Practice Project:
- Write a Python script that defines variables for different data types (numbers, strings, lists, tuples, and dictionaries). Print the values and their corresponding data types to the console.

🔗 [.. Back to TOC](./learn-python-in-half-day-lesson--toc.md)