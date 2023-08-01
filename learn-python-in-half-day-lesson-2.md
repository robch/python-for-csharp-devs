# Lesson 2: Basic Syntax and Indentation (10 minutes)

Welcome to Lesson 2! In this lesson, we'll explore Python's significant use of indentation for block structuring, discuss statement terminators, comment syntax, and variable naming conventions.

### Indentation and Block Structuring:
In Python, indentation is not just for readability; it's a fundamental part of the language's syntax. Unlike C#, which uses curly braces `{}` to define code blocks, Python uses indentation (usually four spaces) to group statements within a block. Proper indentation is essential for code organization and determining the scope of statements.

**C# Code:**
```csharp
// C# code block
if (condition)
{
    Console.WriteLine("True branch");
}
else
{
    Console.WriteLine("False branch");
}
```

**Python Equivalent:**
```python
# Python code block
if condition:
    print("True branch")
else:
    print("False branch")
```

### Statement Termination and Comments:
- **Statement Termination**: In Python, you don't need to use semicolons `;` to terminate statements like in C#. Each line typically represents one statement, and Python interprets the line break as the end of the statement.

- **Comments**: Python uses the `#` symbol for single-line comments, similar to C#'s `//` notation. Anything after `#` on the same line is considered a comment and is ignored by the Python interpreter.

**C# Code:**
```csharp
// C# statement termination and comments
int number = 42; // This is a comment
Console.WriteLine(number); // Print the number
```

**Python Equivalent:**
```python
# Python statement termination and comments
number = 42  # This is a comment
print(number)  # Print the number
```

### Variable Naming Conventions:
Python has its own naming conventions for variables, which might differ from what you're used to in C#. Here are some key points:

- Variable names are case-sensitive (`count` and `Count` are different variables).
- Use lowercase for variable names (e.g., `my_variable`).
- Separate words in variable names with underscores (e.g., `word_list`, `first_name`).
- Avoid starting variable names with numbers or special characters.

### Key Differences for C# Developers:
- Indentation is crucial in Python, and forgetting to indent properly will result in syntax errors.
- No need for semicolons to terminate statements in Python; each line is a separate statement.
- Python uses the `#` symbol for single-line comments, not `//`.
- Python variable naming conventions use lowercase and underscores, unlike C#'s camelCase or PascalCase conventions.

Now that you've familiarized yourself with Python's basic syntax and indentation, you're ready to move on to Lesson 3, where we'll explore Python's dynamic typing and data types.

### Additional Resources:
- Python Indentation Guide: https://www.python.org/dev/peps/pep-0008/#indentation

### Practice Project:
- Write a Python script that calculates the area of a rectangle and uses proper indentation for the code block inside the function. Use comments to explain the steps in the calculation.

🔗 [.. Back to TOC](./learn-python-in-half-day-lesson--toc.md)