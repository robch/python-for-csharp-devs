# Lesson 14: Generators (10 minutes)

Welcome to Lesson 14! In this lesson, we'll explore Python generators, a powerful feature for lazy evaluation of sequences. Generators allow you to create iterators efficiently, especially for large datasets, without generating all the elements upfront.

## Creating Generators:
In Python, generators are defined using functions with the `yield` keyword instead of `return`. When a generator function is called, it returns a generator object, which can be iterated over using a loop or functions like `next()`.

**Example 1: Creating a Generator Function**
```python
def countdown(n):
    while n > 0:
        yield n
        n -= 1
```

## Using Generators:
Generators produce values lazily, one at a time, as they are requested. They do not store the entire sequence in memory, making them memory-efficient for large datasets.

**Example 2: Using the Generator**
```python
# Create the generator
counter = countdown(5)

# Use the generator with a loop
for number in counter:
    print(number)   # Output: 5, 4, 3, 2, 1
```

You can also use the `next()` function to retrieve the next value from the generator.

**Example 3: Using the next() Function**
```python
counter = countdown(5)

print(next(counter))  # Output: 5
print(next(counter))  # Output: 4
print(next(counter))  # Output: 3
```

## Generator Expressions:
Generator expressions are similar to list comprehensions but produce generator objects instead of lists. They are defined using parentheses `()` instead of square brackets `[]`.

**Example 4: Generator Expression**
```python
# Generator expression for even numbers
even_numbers = (x for x in range(10) if x % 2 == 0)

# Using the generator expression with a loop
for number in even_numbers:
    print(number)   # Output: 0, 2, 4, 6, 8
```

## Key Differences for C# Developers:
- Generators in Python provide a more memory-efficient way to work with sequences compared to C#'s enumerables.
- Python's generator functions use the `yield` keyword instead of `return`.

Now that you've learned about generators in Python, you can efficiently work with large datasets and sequences without consuming excessive memory.

## Additional Resources:
- Python Generators: https://docs.python.org/3/tutorial/classes.html#generators

## Practice Project:
- Write a Python script that generates an infinite sequence of Fibonacci numbers using a generator. Print the first 10 Fibonacci numbers from the generator.

🔗 [.. Back to TOC](./learn-python-in-half-day-lesson--toc.md)