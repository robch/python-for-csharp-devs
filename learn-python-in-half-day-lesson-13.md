# Lesson 13: List Slicing (10 minutes)

Welcome to Lesson 13! In this lesson, we'll explore list slicing in Python. List slicing allows you to create new lists by extracting a portion of an existing list, making it easy to work with subsets of data.

## Basic List Slicing:
In Python, you can use list slicing to extract a portion of a list using the following syntax:

```python
new_list = original_list[start_index:end_index]
```

- `start_index` is the index from which the slice starts (inclusive).
- `end_index` is the index where the slice ends (exclusive).

**Example 1: Basic List Slicing**
```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

# Slice from index 2 to 5 (exclusive)
slice1 = numbers[2:5]    # Output: [3, 4, 5]

# Slice from the beginning to index 6 (exclusive)
slice2 = numbers[:6]     # Output: [1, 2, 3, 4, 5, 6]

# Slice from index 5 to the end
slice3 = numbers[5:]     # Output: [6, 7, 8, 9, 10]
```

## Slicing with Step:
You can specify a step value to skip elements in the slice.

```python
new_list = original_list[start_index:end_index:step]
```

**Example 2: Slicing with Step**
```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

# Slice from index 1 to 9 (exclusive) with a step of 2
slice4 = numbers[1:9:2]    # Output: [2, 4, 6, 8]
```

## Negative Indexing:
In Python, you can use negative indices to slice the list from the end.

**Example 3: Negative Indexing**
```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

# Slice the last three elements
slice5 = numbers[-3:]      # Output: [8, 9, 10]

# Slice all elements except the last two
slice6 = numbers[:-2]      # Output: [1, 2, 3, 4, 5, 6, 7, 8]
```

## Modifying List Slices:
You can also modify elements in a list slice.

**Example 4: Modifying List Slices**
```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

# Replace elements in the slice
numbers[1:4] = [20, 30, 40]
print(numbers)    # Output: [1, 20, 30, 40, 5, 6, 7, 8, 9, 10]
```

## Key Differences for C# Developers:
- List slicing in Python is similar to C#'s array slicing, but Python uses different syntax and supports more advanced features like negative indexing and slicing with a step.

Now that you've learned about list slicing in Python, you can efficiently work with subsets of data within lists.

## Additional Resources:
- Python List Slicing: https://docs.python.org/3/tutorial/introduction.html#lists

## Practice Project:
- Write a Python script that takes a list of words as input and creates a new list containing only the words with three or more characters using list slicing. Print the new list.

🔗 [.. Back to TOC](./learn-python-in-half-day-lesson--toc.md)