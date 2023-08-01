# Lesson 7: List Comprehensions (10 minutes)

Welcome to Lesson 7! In this lesson, we'll explore list comprehensions, a powerful feature unique to Python. List comprehensions provide a concise and expressive way to create lists based on existing lists or other iterable objects.

## Creating Lists with List Comprehensions:
In Python, you can use list comprehensions to generate new lists by applying an expression to each item in an existing iterable. The basic syntax for a list comprehension is:

```python
new_list = [expression for item in iterable]
```

**Example 1: Squaring Numbers**
```python
# Using a loop to create a list of squares
numbers = [1, 2, 3, 4, 5]
squares = []
for num in numbers:
    squares.append(num ** 2)

# Using list comprehension for the same result
squares = [num ** 2 for num in numbers]
```

**Example 2: Filtering even numbers**
```python
# Using a loop to filter even numbers from a list
numbers = [1, 2, 3, 4, 5]
even_numbers = []
for num in numbers:
    if num % 2 == 0:
        even_numbers.append(num)

# Using list comprehension for the same result
even_numbers = [num for num in numbers if num % 2 == 0]
```

List comprehensions can also include conditional expressions, allowing you to apply different expressions based on specific conditions.

**Example 3: Mapping and Filtering**
```python
# Using a loop for mapping and filtering
numbers = [1, 2, 3, 4, 5]
result = []
for num in numbers:
    if num % 2 == 0:
        result.append("Even")
    else:
        result.append("Odd")

# Using list comprehension for the same result
result = ["Even" if num % 2 == 0 else "Odd" for num in numbers]
```

## Key Differences for C# Developers:
- List comprehensions provide a concise and expressive way to generate lists in Python, which can be more compact than using explicit loops in C#.
- List comprehensions can combine mapping and filtering operations into a single expression, making the code more readable and efficient.

Now that you've learned about list comprehensions in Python, you're ready to move on to Lesson 8, where we'll explore dictionaries, another essential data structure in Python.

## Additional Resources:
- Python List Comprehensions: https://docs.python.org/3/tutorial/datastructures.html#list-comprehensions

## Practice Project:
- Write a Python script that takes a list of names and creates a new list containing only the names with more than five characters using list comprehension.

🔗 [.. Back to TOC](./learn-python-in-half-day-lesson--toc.md)