# Lesson 19: Common Gotchas (10 minutes)

Welcome to Lesson 19! In this lesson, we'll highlight some common pitfalls and gotchas that C# developers transitioning to Python should be aware of. Understanding these differences will help you avoid potential issues in your Python code.

## 1. Indentation Errors:
In Python, proper indentation is crucial for code structure. Mixing tabs and spaces or inconsistent indentation can lead to syntax errors.

**Example 1: Indentation Error**
```python
if condition:
    print("True branch")
   print("Indented incorrectly")  # This will cause an IndentationError
```

## 2. Mutable Default Arguments:
Default arguments in Python are evaluated only once when the function is defined. Be cautious when using mutable objects like lists or dictionaries as default arguments, as they can lead to unexpected behavior.

**Example 2: Mutable Default Argument**
```python
def add_item(item, items=[]):
    items.append(item)
    return items

print(add_item("apple"))   # Output: ['apple']
print(add_item("banana"))  # Output: ['apple', 'banana'] (Unexpected!)
```

To avoid this, use `None` as the default value and create a new list inside the function.

**Example 3: Avoiding Mutable Default Argument**
```python
def add_item(item, items=None):
    if items is None:
        items = []
    items.append(item)
    return items

print(add_item("apple"))   # Output: ['apple']
print(add_item("banana"))  # Output: ['banana'] (Expected)
```

## 3. Object Identity vs. Equality:
In Python, `is` checks for object identity (whether two variables refer to the same object), while `==` checks for equality (whether two objects have the same value).

**Example 4: Object Identity vs. Equality**
```python
list1 = [1, 2, 3]
list2 = list1

print(list1 is list2)  # Output: True
print(list1 == list2)  # Output: True

list3 = [1, 2, 3]

print(list1 is list3)  # Output: False
print(list1 == list3)  # Output: True
```

## 4. Global Variables:
Be careful when modifying global variables within functions. If you want to modify a global variable, use the `global` keyword to indicate that the variable is global.

**Example 5: Modifying a Global Variable**
```python
count = 0

def increment_count():
    global count
    count += 1

increment_count()
print(count)  # Output: 1
```

## Key Differences for C# Developers:
- Pay close attention to indentation in Python, as it defines code blocks and scopes.
- Understand the difference between mutable and immutable default function arguments.
- Be aware of the distinction between object identity (`is`) and equality (`==`).
- When working with global variables inside functions, use the `global` keyword to indicate that you are modifying the global variable.

Now that you are aware of these common gotchas, you can write more robust and error-free Python code.

## Additional Resources:
- Python Documentation on Errors and Exceptions: https://docs.python.org/3/tutorial/errors.html

## Practice Project:
- Review your existing Python code for any potential gotchas and apply the necessary fixes to avoid common pitfalls.

🔗 [.. Back to TOC](./learn-python-in-half-day-lesson--toc.md)