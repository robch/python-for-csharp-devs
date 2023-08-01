# Lesson 11: Exception Handling (10 minutes)

Welcome to Lesson 11! In this lesson, we'll explore Python's exception handling mechanism. Exception handling allows you to gracefully handle errors and unexpected situations in your code, preventing it from crashing.

## Handling Exceptions with try-except:
In Python, you can use a `try-except` block to handle exceptions. The `try` block contains the code that might raise an exception, and the `except` block specifies how to handle the exception if it occurs.

**Example 1: Handling Division by Zero**
```python
try:
    dividend = 10
    divisor = 0
    result = dividend / divisor
except ZeroDivisionError as e:
    print(f"Error: {e}")
```

## Handling Multiple Exceptions:
You can handle different types of exceptions using multiple `except` blocks.

**Example 2: Handling Multiple Exceptions**
```python
try:
    # Some code that might raise an exception
except ZeroDivisionError as e:
    # Handle ZeroDivisionError
except ValueError as e:
    # Handle ValueError
except Exception as e:
    # Handle any other exception (catch-all)
```

## Handling Exceptions with else and finally:
- The `else` block is executed if no exceptions occur in the `try` block. It is useful for code that should run only when no exceptions are raised.
- The `finally` block is executed regardless of whether an exception occurred or not. It is used for cleanup operations that need to be performed, such as closing files or releasing resources.

**Example 3: Using else and finally**
```python
try:
    # Some code that might raise an exception
except ZeroDivisionError as e:
    # Handle ZeroDivisionError
else:
    # Code to be executed if no exception occurred
finally:
    # Code to be executed regardless of exceptions
```

## Raising Exceptions:
You can raise exceptions explicitly using the `raise` keyword.

**Example 4: Raising an Exception**
```python
def divide(a, b):
    if b == 0:
        raise ValueError("Division by zero is not allowed.")
    return a / b

try:
    result = divide(10, 0)
except ValueError as e:
    print(f"Error: {e}")
```

## Key Differences for C# Developers:
- Exception handling in Python uses the `try-except` block instead of C#'s `try-catch` block.
- Python's exception handling does not require explicit declaration of exceptions that a function may throw, unlike C#'s `throws` clause.

Now that you've learned about exception handling in Python, you're better equipped to handle errors and unexpected situations in your Python projects.

## Additional Resources:
- Python Exception Handling: https://docs.python.org/3/tutorial/errors.html

## Practice Project:
- Modify the `Rectangle` class from the previous practice project to include exception handling for invalid length or width inputs (e.g., negative or zero values). Test the exception handling by creating a rectangle with invalid inputs.

🔗 [.. Back to TOC](./learn-python-in-half-day-lesson--toc.md)