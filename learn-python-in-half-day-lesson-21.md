# Lesson 21: Multi-Threading in Python (10 minutes)

Welcome to Lesson 21! In this lesson, we'll explore multi-threading in Python, a powerful concept that allows you to perform concurrent operations efficiently. We'll cover the basics of multi-threading, how to create and manage threads in Python, and discuss the Global Interpreter Lock (GIL) and its implications on multi-threading.

## Understanding Multi-Threading:

Multi-threading is a programming technique that enables a program to perform multiple tasks simultaneously, improving the overall performance and responsiveness of applications. In Python, multi-threading can be especially beneficial when dealing with I/O-bound operations, where tasks involve waiting for external resources like files or network requests.

The `threading` module in Python provides built-in support for multi-threading. Each thread runs independently, and Python's Global Interpreter Lock (GIL) allows only one thread to execute Python bytecode at a time. This means that multi-threading in Python may not provide true parallelism for CPU-bound tasks due to the GIL.

## Creating and Managing Threads:

To create a new thread in Python, you need to create a new instance of the `Thread` class from the `threading` module. You can pass the target function that the thread will execute and any required arguments.

Here's an example of creating and starting a thread:

```python
import threading

def print_numbers():
    for i in range(1, 6):
        print(f"Number: {i}")

# Create a new thread
thread = threading.Thread(target=print_numbers)

# Start the thread
thread.start()

# Wait for the thread to complete
thread.join()

print("Thread execution completed.")
```

In this example, a new thread is created to execute the `print_numbers` function concurrently with the main thread. The `start()` method initiates the execution of the new thread, and `join()` is used to wait for the thread to finish before the main thread continues.

## Global Interpreter Lock (GIL):

The Global Interpreter Lock (GIL) in Python is a mechanism that allows only one thread to execute Python bytecode at a time. This means that even in a multi-threaded program, Python does not fully utilize multiple CPU cores for CPU-bound tasks. The GIL is in place to simplify memory management and avoid potential race conditions with shared data structures.

While the GIL may limit the performance of CPU-bound tasks in multi-threading, it doesn't impact I/O-bound tasks significantly. For I/O-bound operations, multi-threading can still provide substantial benefits as threads can yield control while waiting for I/O operations to complete.

## Key Points to Remember:

- Multi-threading in Python is suitable for I/O-bound tasks and can improve performance and responsiveness.
- Use the `threading` module to create and manage threads in Python.
- The Global Interpreter Lock (GIL) allows only one thread to execute Python bytecode at a time, which can affect CPU-bound tasks.

Now that you've learned about multi-threading in Python, you're ready to explore synchronization and thread safety in Lesson 22.

## Additional Resources:

- Python Threading Documentation: https://docs.python.org/3/library/threading.html
- Understanding the Python GIL: https://realpython.com/python-gil/

## Practice Project:

- Write a Python program that calculates the square of numbers from 1 to 10 using multi-threading. Create multiple threads to perform the calculations concurrently and print the results. Compare the performance with a sequential approach to see the benefits of multi-threading for this task.

🔗 [.. Back to TOC](./learn-python-in-half-day-lesson--toc.md)
