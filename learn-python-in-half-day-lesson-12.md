# Lesson 12: Lambda Functions (10 minutes)

Welcome to Lesson 12! In this lesson, we'll explore lambda functions, a feature in Python that allows you to create small, anonymous functions. Lambda functions are useful for quick, one-line operations and can be used as arguments to higher-order functions.

## Creating Lambda Functions:
In Python, lambda functions are defined using the `lambda` keyword, followed by the function's parameters and a single expression.

**Example 1: Creating a Simple Lambda Function**
```python
# Regular function
def square(x):
    return x ** 2

# Equivalent lambda function
square_lambda = lambda x: x ** 2
```

## Using Lambda Functions:
Lambda functions are often used as throwaway functions for short operations or as arguments to other functions like `map()`, `filter()`, and `sorted()`.

**Example 2: Using Lambda Functions with `map()`**
```python
numbers = [1, 2, 3, 4, 5]

# Using regular function with map()
squared = list(map(square, numbers))

# Using lambda function with map()
squared_lambda = list(map(lambda x: x ** 2, numbers))
```

**Example 3: Using Lambda Functions with `filter()`**
```python
numbers = [1, 2, 3, 4, 5]

# Using regular function with filter()
even = list(filter(lambda x: x % 2 == 0, numbers))
```

**Example 4: Using Lambda Functions with `sorted()`**
```python
words = ["apple", "banana", "orange", "grape"]

# Using regular function with sorted()
sorted_words = sorted(words, key=len)

# Using lambda function with sorted()
sorted_words_lambda = sorted(words, key=lambda word: len(word))
```

## Key Differences for C# Developers:
- Lambda functions in Python are similar to C#'s lambda expressions, but in Python, they can be used more extensively with built-in functions like `map()`, `filter()`, and `sorted()`.
- Python's lambda functions are limited to a single expression, while C#'s lambda expressions can contain multiple statements.

Now that you've learned about lambda functions in Python, you can use them to write more concise and expressive code for certain operations.

## Additional Resources:
- Python Lambda Functions: https://docs.python.org/3/tutorial/controlflow.html#lambda-expressions

## Practice Project:
- Write a Python script that takes a list of numbers as input and uses a lambda function with `map()` to calculate the square of each number and print the results.

🔗 [.. Back to TOC](./learn-python-in-half-day-lesson--toc.md)