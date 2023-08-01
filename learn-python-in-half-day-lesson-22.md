# Lesson 22: Synchronization and Thread Safety (10 minutes)

Welcome to Lesson 22! In this lesson, we'll explore the challenges of concurrent access in multi-threaded programs and learn about thread synchronization techniques to ensure thread safety. We'll cover locks, semaphores, and mutexes to coordinate access to shared resources among multiple threads.

## Challenges of Concurrent Access:

When multiple threads access shared resources concurrently, it can lead to data corruption, race conditions, and other unexpected behavior. It's essential to synchronize the access to shared resources to avoid such issues and maintain thread safety.

## Using Locks for Thread Synchronization:

In Python, the `Lock` class from the `threading` module can be used to synchronize access to shared resources. A lock acts as a binary semaphore that allows only one thread to acquire the lock at a time. If a thread attempts to acquire the lock while it is already held by another thread, the thread will be blocked until the lock becomes available.

Here's an example of using a lock for synchronization:

```python
import threading

counter = 0
counter_lock = threading.Lock()

def increment_counter():
    global counter
    with counter_lock:
        counter += 1

# Create multiple threads to increment the counter concurrently
threads = [threading.Thread(target=increment_counter) for _ in range(5)]

# Start the threads
for thread in threads:
    thread.start()

# Wait for all threads to complete
for thread in threads:
    thread.join()

print("Final counter value:", counter)
```

In this example, the `increment_counter` function increments the `counter` variable using a lock to ensure that only one thread can modify the counter at a time. This prevents race conditions and guarantees the thread safety of the shared `counter` variable.

## Other Synchronization Techniques:

Apart from locks, Python's `threading` module provides other synchronization primitives like semaphores and mutexes.

- **Semaphore**: A semaphore is a generalized version of a lock that can allow multiple threads to access a shared resource up to a specified limit. It's useful in scenarios where you want to control the maximum number of threads that can access a resource simultaneously.

- **Mutex**: A mutex (short for "mutual exclusion") is a lock that only the thread that acquires it can release. It's similar to a regular lock but has ownership semantics. If the thread that already owns the mutex attempts to acquire it again, it will succeed, preventing deadlocks.

The choice of synchronization technique depends on the specific requirements of your multi-threaded program.

## Key Points to Remember:

- Synchronization is crucial in multi-threaded programs to ensure thread safety and avoid data corruption and race conditions.
- Python's `Lock` class can be used for basic thread synchronization.
- Additional synchronization techniques like semaphores and mutexes are available for more specific requirements.

Now that you've learned about synchronization and thread safety in Python, you're ready to explore asynchronous programming with `async` and `await` in Lesson 23.

## Additional Resources:

- Python Threading Synchronization: https://docs.python.org/3/library/threading.html#synchronization
- Understanding Threading Semantics in Python: https://realpython.com/python-concurrency/

## Practice Project:

- Write a Python program that simulates a ticket booking system with multiple threads representing different users trying to book tickets concurrently. Use locks to ensure that only one user can book a ticket at a time to avoid overbooking or conflicts.
- Extend the ticket booking system to use semaphores, allowing a maximum number of users to book tickets simultaneously.

🔗 [.. Back to TOC](./learn-python-in-half-day-lesson--toc.md)
