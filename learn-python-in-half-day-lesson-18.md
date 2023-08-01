# Lesson 18: Pythonic Idioms (10 minutes)

Welcome to Lesson 18! In this lesson, we'll explore Pythonic idioms, which are specific coding styles and patterns that are considered more elegant and readable in Python.

## 1. List Comprehensions:
Python offers list comprehensions, a concise way to create lists. They are often preferred over traditional loops when constructing lists.

**Example 1: List Comprehension**
```python
# Using a for loop
squares = []
for i in range(1, 6):
    squares.append(i ** 2)

# Using a list comprehension
squares_comp = [i ** 2 for i in range(1, 6)]
```

## 2. Pythonic Looping:
When looping through a list, you can use Python's `for item in list` syntax directly, instead of using an index-based approach.

**Example 2: Pythonic Looping**
```python
fruits = ["apple", "banana", "cherry"]

# Non-Pythonic approach
for i in range(len(fruits)):
    print(fruits[i])

# Pythonic approach
for fruit in fruits:
    print(fruit)
```

## 3. Enumerate:
Python's `enumerate()` function provides a more elegant way to loop through a list while keeping track of the index.

**Example 3: Using enumerate()**
```python
fruits = ["apple", "banana", "cherry"]

# Non-Pythonic approach
for i in range(len(fruits)):
    print(i, fruits[i])

# Pythonic approach
for index, fruit in enumerate(fruits):
    print(index, fruit)
```

## 4. Unpacking:
Python allows you to unpack elements from iterables like lists or tuples into individual variables.

**Example 4: Unpacking**
```python
# Unpacking a list
a, b, c = [1, 2, 3]
print(a, b, c)  # Output: 1 2 3

# Unpacking a tuple
x, y = (10, 20)
print(x, y)     # Output: 10 20
```

## 5. Multiple Assignments in One Line:
Python allows you to assign multiple variables in a single line.

**Example 5: Multiple Assignments**
```python
x = y = z = 0
```

## Key Differences for C# Developers:
- Pythonic idioms focus on brevity and readability, often using expressive one-liners.
- Python's list comprehensions, enumerate, and unpacking offer more concise alternatives to common tasks compared to traditional loops and indexing.

Now that you've learned about Pythonic idioms, you can write more elegant and concise Python code following the community's best practices.

## Additional Resources:
- PEP 8 - Style Guide for Python Code: https://www.python.org/dev/peps/pep-0008/

## Practice Project:
- Rewrite some of your previous Python code using Pythonic idioms, such as list comprehensions and unpacking. Compare the new code with the original and observe the differences in readability and conciseness.

🔗 [.. Back to TOC](./learn-python-in-half-day-lesson--toc.md)