# Lesson 4: Control Flow (10 minutes)

Welcome to Lesson 4! In this lesson, we'll explore Python's control flow statements, including if-else, for loops, and while loops, and compare them to their C# counterparts.

## if-else Statements:
Python's if-else statement is similar to C#'s if-else statement in structure, but there are some key differences in syntax.

**C# Code:**
```csharp
// C# if-else statement
int number = 42;
if (number > 0)
{
    Console.WriteLine("Positive");
}
else if (number < 0)
{
    Console.WriteLine("Negative");
}
else
{
    Console.WriteLine("Zero");
}
```

**Python Equivalent:**
```python
# Python if-else statement
number = 42
if number > 0:
    print("Positive")
elif number < 0:
    print("Negative")
else:
    print("Zero")
```

## for Loops:
Python's for loop is more concise and flexible compared to C#'s for loop. In Python, you can directly iterate over elements of a collection or use the `range()` function to generate a sequence of numbers.

**C# Code:**
```csharp
// C# for loop
for (int i = 0; i < 5; i++)
{
    Console.WriteLine(i);
}
```

**Python Equivalent 1:**
```python
# Python for loop (iterate over a list)
fruits = ['apple', 'banana', 'orange']
for fruit in fruits:
    print(fruit)
```

**Python Equivalent 2:**
```python
# Python for loop (using range)
for i in range(5):
    print(i)
```

## while Loops:
Python's while loop works similarly to C#'s while loop, but again, the syntax is more straightforward.

**C# Code:**
```csharp
// C# while loop
int i = 0;
while (i < 5)
{
    Console.WriteLine(i);
    i++;
}
```

**Python Equivalent:**
```python
# Python while loop
i = 0
while i < 5:
    print(i)
    i += 1
```

## Key Differences for C# Developers:
- Python uses colons (`:`) after if, elif, else, for, and while statements, followed by an indented block, while C# uses curly braces `{}`.
- In Python, you don't need to explicitly declare a loop variable for for loops. It automatically takes the value of the current element in the iteration.
- Python's range function simplifies generating a sequence of numbers for loop iterations.

Now that you've learned about Python's control flow statements, you're ready to move on to Lesson 5, where we'll explore Python functions and compare them to C#'s methods.

## Additional Resources:
- Python Control Flow: https://docs.python.org/3/tutorial/controlflow.html

## Practice Project:
- Write a Python script that uses if-else statements to determine if a given number is odd or even. Use a for loop to iterate over a list of names and print a greeting message for each name. Use a while loop to calculate the sum of numbers from 1 to 10.

🔗 [.. Back to TOC](./learn-python-in-half-day-lesson--toc.md)