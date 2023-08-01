# Lesson 15: Python Standard Library (10 minutes)

Welcome to Lesson 15! In this lesson, we'll introduce you to the Python Standard Library, a collection of modules and packages that come with Python. The standard library provides a wide range of functionalities, making it a valuable resource for many common tasks.

## Using Modules from the Standard Library:
To use modules from the Python Standard Library, you need to import them into your code using the `import` statement.

**Example 1: Using the `math` Module**
```python
import math

# Calculate the square root
result = math.sqrt(25)
print(result)    # Output: 5.0
```

## Commonly Used Modules in the Standard Library:
Here are some commonly used modules from the Python Standard Library:

- `math`: Provides mathematical functions and constants.
- `random`: Generates random numbers and elements from sequences.
- `datetime`: Manipulates dates and times.
- `os`: Interacts with the operating system, such as file and directory operations.
- `json`: Encodes and decodes JSON data.
- `csv`: Handles CSV (Comma-Separated Values) files.
- `urllib`: Deals with URL-related operations like fetching data from URLs.

**Example 2: Using the `random` Module**
```python
import random

# Generate a random integer between 1 and 100
random_number = random.randint(1, 100)
print(random_number)
```

**Example 3: Using the `datetime` Module**
```python
import datetime

# Get the current date and time
current_time = datetime.datetime.now()
print(current_time)
```

## Exploring the Standard Library:
The Python Standard Library is extensive, covering various areas such as data processing, networking, web development, and more. You can find the full list of modules in the official Python documentation.

## Key Differences for C# Developers:
- Python's Standard Library provides a wide range of functionalities, similar to C#'s .NET Framework Class Library (FCL).
- The process of importing and using modules from the Standard Library is similar to referencing and using assemblies in C#.

Now that you've learned about the Python Standard Library, you can explore its modules and leverage its functionalities in your Python projects.

## Additional Resources:
- Python Standard Library: https://docs.python.org/3/library/

## Practice Project:
- Write a Python script that uses the `random` module to generate a list of 10 random integers between 1 and 100. Use the `datetime` module to print the current date and time before and after generating the random list.

🔗 [.. Back to TOC](./learn-python-in-half-day-lesson--toc.md)