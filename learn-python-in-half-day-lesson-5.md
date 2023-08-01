# Lesson 5: Functions (10 minutes)

Welcome to Lesson 5! In this lesson, we'll learn how to define and call functions in Python and explore function arguments and return values. We'll also compare Python functions with C#'s methods.

## Defining and Calling Functions in Python:
In Python, functions are defined using the `def` keyword, followed by the function name, a pair of parentheses, and a colon. The function body is indented beneath the function definition.

**C# Code:**
```csharp
// C# method definition
public void Greet(string name)
{
    Console.WriteLine($"Hello, {name}!");
}
```

**Python Equivalent:**
```python
# Python function definition
def greet(name):
    print(f"Hello, {name}!")
```

To call a function in Python, simply write the function name followed by parentheses, providing any required arguments.

**C# Code:**
```csharp
// C# method call
Greet("Alice");
```

**Python Equivalent:**
```python
# Python function call
greet("Alice")
```

## Function Arguments and Return Values:
Python functions can have default parameter values, allowing you to call the function without providing all arguments. You can also use keyword arguments to specify arguments by their parameter names.

**C# Code:**
```csharp
// C# method with default parameter value
public void Multiply(int a, int b = 2)
{
    Console.WriteLine(a * b);
}
```

**Python Equivalent:**
```python
# Python function with default parameter value
def multiply(a, b=2):
    print(a * b)
```

Python functions can return values using the `return` keyword. Unlike C#, Python allows functions to return multiple values as a tuple.

**C# Code:**
```csharp
// C# method with return value
public int Add(int a, int b)
{
    return a + b;
}
```

**Python Equivalent:**
```python
# Python function with return value
def add(a, b):
    return a + b
```

## Key Differences for C# Developers:
- Python uses the `def` keyword to define functions, while C# uses `public` or other access modifiers.
- Python allows default parameter values and keyword arguments for functions, which can make function calls more flexible.
- Python functions can return multiple values as a tuple, whereas C#'s methods can only return a single value.

Now that you've learned about functions in Python, you're ready to move on to Lesson 6, where we'll explore file handling in Python and compare it to C#'s file I/O.

## Additional Resources:
- Python Functions: https://docs.python.org/3/tutorial/controlflow.html#defining-functions

## Practice Project:
- Write a Python function that calculates the area of a rectangle given its length and width as arguments. Use default parameter values for the width to handle both square and rectangular shapes. Test the function with different input values.

🔗 [.. Back to TOC](./learn-python-in-half-day-lesson--toc.md)