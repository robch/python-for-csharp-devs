# Lesson 16: Third-Party Libraries and pip (10 minutes)

Welcome to Lesson 16! In this lesson, we'll explore third-party libraries in Python and learn how to install and manage them using `pip`, the package manager for Python.

## What are Third-Party Libraries?
In addition to the Python Standard Library, there is a vast ecosystem of third-party libraries developed by the Python community. These libraries extend Python's capabilities and offer solutions for various tasks, such as web development, data analysis, machine learning, and more.

## Using `pip` to Install Libraries:
`pip` is the standard package manager for Python, and it comes pre-installed with most Python distributions. You can use `pip` to install, upgrade, and uninstall third-party libraries easily.

**Example 1: Installing a Library with pip**
Open your command line or terminal and run the following command to install a library (replace `library_name` with the name of the library you want to install):

```
pip install library_name
```

For example, to install the `requests` library for making HTTP requests:

```
pip install requests
```

## Using Installed Libraries in Your Code:
After installing a library, you can use it in your Python code by importing it just like the Python Standard Library modules.

**Example 2: Using the `requests` Library**
```python
import requests

response = requests.get("https://www.example.com")
print(response.status_code)    # Output: 200
```

## Managing Library Versions:
`pip` allows you to install specific versions of libraries or upgrade to the latest versions.

**Example 3: Specifying a Library Version**
```
pip install library_name==1.2.3
```

**Example 4: Upgrading a Library to the Latest Version**
```
pip install --upgrade library_name
```

## Listing Installed Libraries:
You can see a list of installed libraries and their versions using the `pip list` command.

**Example 5: Listing Installed Libraries**
```
pip list
```

## Uninstalling Libraries:
If you no longer need a library, you can uninstall it using `pip`.

**Example 6: Uninstalling a Library**
```
pip uninstall library_name
```

## Key Differences for C# Developers:
- `pip` is the Python equivalent of NuGet for C#. It allows you to easily manage third-party libraries in your Python projects.
- Unlike NuGet, `pip` installs libraries globally by default. If you want to manage dependencies per project, you can use virtual environments (covered in Lesson 17).

Now that you've learned about third-party libraries and `pip`, you can enhance your Python projects by leveraging the power of the Python community's extensive library ecosystem.

## Additional Resources:
- Python Package Index (PyPI): https://pypi.org/
- `pip` documentation: https://pip.pypa.io/en/stable/

## Practice Project:
- Choose a third-party library from the Python Package Index (PyPI) that interests you. Install the library using `pip`, and write a Python script to demonstrate its functionality.

🔗 [.. Back to TOC](./learn-python-in-half-day-lesson--toc.md)