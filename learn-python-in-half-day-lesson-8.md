# Lesson 8: Dictionaries (10 minutes)

Welcome to Lesson 8! In this lesson, we'll explore Python dictionaries and their usage. Dictionaries are powerful data structures that store key-value pairs and allow fast retrieval of values based on their keys.

## Creating and Accessing Dictionaries:
In Python, dictionaries are defined using curly braces `{}` and consist of key-value pairs separated by colons `:`.

**Example 1: Creating a Dictionary**
```python
# Empty dictionary
empty_dict = {}

# Dictionary with key-value pairs
person = {"name": "John", "age": 30, "occupation": "developer"}
```

To access the value associated with a specific key in a dictionary, you can use square brackets `[]` with the key inside.

**Example 2: Accessing Values in a Dictionary**
```python
person = {"name": "John", "age": 30, "occupation": "developer"}

print(person["name"])       # Output: John
print(person["age"])        # Output: 30
print(person["occupation"]) # Output: developer
```

If the key is not present in the dictionary, accessing it will raise a `KeyError`. To avoid this, you can use the `get()` method, which returns a default value if the key is not found.

**Example 3: Using get() method to Handle Missing Keys**
```python
person = {"name": "John", "age": 30}

print(person.get("name"))         # Output: John
print(person.get("occupation"))   # Output: None (key not found, returns None)
print(person.get("occupation", "-"))  # Output: - (key not found, returns default value "-")
```

## Modifying and Adding Elements in a Dictionary:
You can modify the value associated with a key or add a new key-value pair to a dictionary using the assignment operator `=`.

**Example 4: Modifying and Adding Elements in a Dictionary**
```python
person = {"name": "John", "age": 30}

person["age"] = 32       # Modify the value of "age"
person["occupation"] = "developer"  # Add a new key-value pair

print(person)           # Output: {"name": "John", "age": 32, "occupation": "developer"}
```

## Removing Elements from a Dictionary:
To remove a key-value pair from a dictionary, you can use the `del` keyword or the `pop()` method.

**Example 5: Removing Elements from a Dictionary**
```python
person = {"name": "John", "age": 30, "occupation": "developer"}

del person["age"]      # Remove "age" key and its value using del

# Remove "occupation" key and its value using pop()
occupation = person.pop("occupation")

print(person)         # Output: {"name": "John"}
print(occupation)     # Output: developer
```

## Key Differences for C# Developers:
- Python dictionaries are similar to C#'s dictionary or hash table data structure.
- In Python, dictionaries use curly braces `{}` for defining key-value pairs, while C#'s dictionary initialization uses the `Dictionary<TKey, TValue>` class.

Now that you've learned about dictionaries in Python, you're ready to move on to Lesson 9, where we'll explore modules and packages, essential for organizing code in Python.

## Additional Resources:
- Python Dictionaries: https://docs.python.org/3/tutorial/datastructures.html#dictionaries

## Practice Project:
- Write a Python script that takes a list of words as input and creates a dictionary where the keys are the words, and the values are the lengths of the corresponding words.

🔗 [.. Back to TOC](./learn-python-in-half-day-lesson--toc.md)