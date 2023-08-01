# Lesson 24: Combining Threads and Async in Python (10 minutes)

Welcome to Lesson 24! In this lesson, we'll explore scenarios where combining multi-threading and asynchronous programming can be effective. We'll discuss best practices and potential challenges when using both techniques together. Additionally, we'll demonstrate an example of combining threads and async in a Python application.

## Effective Scenarios for Combining Threads and Async:

Combining multi-threading and asynchronous programming can be advantageous in certain situations:

1. **I/O-bound tasks with CPU-bound processing**: If your program performs I/O-bound tasks (e.g., making network requests) but also requires CPU-bound processing (e.g., data processing), you can use threads for I/O-bound tasks and async for CPU-bound tasks. This way, I/O-bound tasks can run concurrently, and CPU-bound tasks can use async for efficient execution.

2. **Parallelizing I/O-bound tasks**: When dealing with multiple I/O-bound tasks that can be executed concurrently, you can use threads to achieve parallelism for I/O operations. Asynchronous programming allows the program to efficiently switch between tasks while waiting for I/O.

## Best Practices and Challenges:

While combining threads and async can provide performance benefits, it requires careful consideration and adherence to best practices:

1. **Avoid CPU-bound tasks with the GIL**: When combining threads and async, avoid using CPU-bound tasks that heavily rely on the Global Interpreter Lock (GIL) in Python. The GIL can limit the performance gain of multi-threading for CPU-bound tasks.

2. **Synchronization**: Be cautious when accessing shared resources between threads and async tasks. Proper synchronization using locks or other techniques is essential to maintain thread safety and avoid race conditions.

3. **Avoid nested event loops**: If you are using a library that already utilizes an event loop, avoid creating additional nested event loops, as this can lead to unexpected behavior.

## Example: Combining Threads and Async:

Let's see an example of combining threads and async to fetch data from multiple URLs concurrently and perform CPU-bound processing on the fetched data.

```python
import asyncio
import requests
import threading

async def process_data(data):
    # Simulate CPU-bound processing
    await asyncio.sleep(1)
    return data.upper()

def fetch_data(url):
    response = requests.get(url)
    return response.text

async def main():
    urls = ["https://example.com", "https://example.org", "https://example.net"]

    # Fetch data from URLs using threads
    with concurrent.futures.ThreadPoolExecutor() as executor:
        fetch_tasks = [loop.run_in_executor(executor, fetch_data, url) for url in urls]
        fetched_data = await asyncio.gather(*fetch_tasks)

    # Process fetched data using async
    process_tasks = [process_data(data) for data in fetched_data]
    processed_data = await asyncio.gather(*process_tasks)

    print("Processed data:", processed_data)

if __name__ == "__main__":
    loop = asyncio.get_event_loop()
    loop.run_until_complete(main())
```

In this example, we use a ThreadPoolExecutor from the concurrent.futures module to fetch data from multiple URLs concurrently using threads. Then, we use async and await to perform CPU-bound processing on the fetched data asynchronously.

## Key Points to Remember:

- Combining threads and async can be effective for specific scenarios involving I/O-bound and CPU-bound tasks.
- Be cautious of using CPU-bound tasks that rely heavily on the GIL when combining threads and async.
- Proper synchronization and avoiding nested event loops are essential best practices.

Now that you've learned about combining threads and async in Python, you're ready to explore performance considerations with threads and async in Lesson 25.

## Additional Resources:

- Combining Threads and Async: https://asyncio.readthedocs.io/en/latest/threading.html

## Practice Project:

- Write a Python program that fetches data from multiple URLs concurrently using threads and processes the fetched data concurrently using async. Measure the performance gain compared to sequential execution for both fetching and processing data.

🔗 [.. Back to TOC](./learn-python-in-half-day-lesson--toc.md)
