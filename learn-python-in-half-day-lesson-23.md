# Lesson 23: Asynchronous Programming with Async/Await (10 minutes)

Welcome to Lesson 23! In this lesson, we'll explore asynchronous programming in Python, a powerful technique for handling I/O-bound tasks efficiently. We'll introduce the `async` and `await` keywords, which allow you to define and await asynchronous functions, and we'll compare synchronous and asynchronous approaches for I/O-bound operations.

## Understanding Asynchronous Programming:

Asynchronous programming allows a program to perform I/O-bound tasks efficiently by executing multiple tasks concurrently without blocking the execution flow. This is especially beneficial when dealing with operations that involve waiting for external resources like reading from files, making network requests, or accessing databases.

Python provides native support for asynchronous programming using the `asyncio` module, which allows you to define and run asynchronous functions and coroutines.

## Defining and Awaiting Asynchronous Functions:

To define an asynchronous function in Python, you use the `async` keyword before the `def` keyword. Within the function, you can use the `await` keyword to pause the execution and wait for an asynchronous operation to complete.

Here's an example of an asynchronous function using `async` and `await`:

```python
import asyncio

async def fetch_data(url):
    print(f"Fetching data from {url}...")
    await asyncio.sleep(2)  # Simulate a delay (async I/O operation)
    print(f"Data fetched from {url}.")

# Using asyncio.run to run the asynchronous function
asyncio.run(fetch_data("https://example.com"))
```

In this example, the `fetch_data` function simulates an I/O-bound operation by using `await asyncio.sleep(2)`. This operation suspends the function's execution for 2 seconds, allowing other tasks to run concurrently during that time.

## Comparing Synchronous and Asynchronous Approaches:

Let's compare the synchronous and asynchronous approaches for fetching data from multiple URLs:

```python
# Synchronous (Sequential) Approach
def fetch_all_data(urls):
    for url in urls:
        print(f"Fetching data from {url}...")
        # Simulate a delay (I/O operation)
        time.sleep(2)
        print(f"Data fetched from {url}.")

# Asynchronous Approach
async def fetch_all_data_async(urls):
    tasks = [fetch_data(url) for url in urls]
    await asyncio.gather(*tasks)

urls = ["https://example.com", "https://example.org", "https://example.net"]

# Synchronous (Sequential) Execution
fetch_all_data(urls)

# Asynchronous Execution
asyncio.run(fetch_all_data_async(urls))
```

In the synchronous approach, fetching data from each URL occurs sequentially, leading to a total delay of 6 seconds (2 seconds for each URL). In contrast, the asynchronous approach fetches data from all URLs concurrently, resulting in a total delay of only 2 seconds (the maximum delay of all tasks).

## Key Points to Remember:

- Asynchronous programming in Python allows efficient handling of I/O-bound tasks.
- Use the `async` and `await` keywords to define and await asynchronous functions.
- The `asyncio` module provides support for asynchronous programming.

Now that you've learned about asynchronous programming with `async` and `await` in Python, you're ready to explore combining threads and async in Lesson 24.

## Additional Resources:

- Python Asynchronous Programming: https://docs.python.org/3/library/asyncio.html
- Async IO in Python: A Complete Walkthrough: https://realpython.com/async-io-python/

## Practice Project:

- Write a Python program that fetches data from multiple URLs using both synchronous and asynchronous approaches. Measure the execution time for each approach and compare the performance when fetching data from a large number of URLs.

🔗 [.. Back to TOC](./learn-python-in-half-day-lesson--toc.md)