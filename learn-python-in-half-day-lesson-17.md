# Lesson 17: Virtual Environments (10 minutes)

Welcome to Lesson 17! In this lesson, we'll explore virtual environments in Python, which allow you to create isolated and independent environments for different Python projects. Virtual environments help manage dependencies and avoid conflicts between project requirements.

## Why Use Virtual Environments?
In Python, different projects may require different versions of libraries or dependencies. Using a virtual environment allows you to keep each project isolated, so changes made to one project's dependencies do not affect other projects.

## Creating a Virtual Environment:
Python 3 comes with the `venv` module, which allows you to create virtual environments.

**Example 1: Creating a Virtual Environment**
Open your command line or terminal, navigate to your project's directory, and run the following command:

```
python -m venv myenv
```

This will create a new virtual environment named `myenv` in your project directory.

## Activating the Virtual Environment:
After creating a virtual environment, you need to activate it to start using it.

**On Windows:**
```
myenv\Scripts\activate
```

**On macOS/Linux:**
```
source myenv/bin/activate
```

When the virtual environment is activated, you'll see the environment's name in your command prompt.

## Installing Libraries in the Virtual Environment:
Once the virtual environment is activated, you can use `pip` to install libraries as usual. The installed libraries will be specific to the virtual environment.

**Example 2: Installing a Library in the Virtual Environment**
```
pip install library_name
```

## Deactivating the Virtual Environment:
To deactivate the virtual environment and return to the system's Python environment, use the `deactivate` command.

**Example 3: Deactivating the Virtual Environment**
```
deactivate
```

## Key Differences for C# Developers:
- Virtual environments in Python are similar in concept to using separate package managers like NuGet for each C# project, but virtual environments provide a more integrated and consistent way to manage dependencies.
- Virtual environments are especially helpful when working on multiple Python projects with different library requirements.

Now that you've learned about virtual environments in Python, you can create isolated environments for your projects and manage dependencies effectively.

## Additional Resources:
- Python Virtual Environments: https://docs.python.org/3/tutorial/venv.html

## Practice Project:
- Create a new virtual environment for a Python project of your choice. Activate the environment, install some libraries, and run your project's code within the virtual environment.

🔗 [.. Back to TOC](./learn-python-in-half-day-lesson--toc.md)