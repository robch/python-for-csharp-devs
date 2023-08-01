# Lesson 6: File Handling (10 minutes)

Welcome to Lesson 6! In this lesson, we'll learn how to read and write files using Python's file handling methods. We'll also compare file handling in Python with C#'s file I/O.

## Reading Files in Python:
To read the contents of a file in Python, you can use the `open()` function with the file mode set to `'r'` (read mode). The `open()` function returns a file object, which you can use to read the file's content using methods like `read()`, `readline()`, or `readlines()`.

**C# Code:**
```csharp
// C# file reading
string content = File.ReadAllText("example.txt");
```

**Python Equivalent:**
```python
# Python file reading
with open("example.txt", "r") as file:
    content = file.read()
```

The `with` statement in Python is used with file handling to ensure that the file is properly closed after its suite finishes, even if an exception is raised.

## Writing Files in Python:
To write to a file in Python, you can use the `open()` function with the file mode set to `'w'` (write mode). This mode will create a new file or overwrite the existing file if it already exists. You can use the `write()` method of the file object to write content to the file.

**C# Code:**
```csharp
// C# file writing
string content = "Hello, C#!";
File.WriteAllText("example.txt", content);
```

**Python Equivalent:**
```python
# Python file writing
content = "Hello, Python!"
with open("example.txt", "w") as file:
    file.write(content)
```

## Appending to Files in Python:
To append content to an existing file in Python, you can use the file mode `'a'` (append mode) with the `open()` function.

**C# Code:**
```csharp
// C# file appending
string content = "This is a new line.";
File.AppendAllText("example.txt", content);
```

**Python Equivalent:**
```python
# Python file appending
content = "This is a new line."
with open("example.txt", "a") as file:
    file.write(content)
```

## Key Differences for C# Developers:
- Python's file handling uses the `open()` function to work with files, while C# provides static methods in the `File` class for file I/O.
- The `with` statement in Python simplifies file handling by ensuring proper file closure.
- Python provides three different modes for file handling: `'r'` (read mode), `'w'` (write mode), and `'a'` (append mode), which cover most file manipulation scenarios.

Now that you've learned about file handling in Python, you're ready to move on to Lesson 7, where we'll explore list comprehensions, a powerful feature unique to Python.

## Additional Resources:
- Python File Handling: https://docs.python.org/3/tutorial/inputoutput.html#reading-and-writing-files

## Practice Project:
- Write a Python script that reads the contents of a text file, performs some string manipulation (e.g., converting to uppercase), and writes the modified content back to a new file.

🔗 [.. Back to TOC](./learn-python-in-half-day-lesson--toc.md)