# 🐍 Python Basics
![image](https://github.com/user-attachments/assets/cbb28a9f-a2d1-4575-9c5f-5f570716099a)

Welcome to the Python Basics section of the Data Science and AI Roadmap! Python is the most widely used programming language in the world of Data Science and AI due to its simplicity and powerful libraries. In this section, we will cover the fundamentals of Python that will serve as the building blocks for more advanced topics later on.

---

## Table of Contents

1. [Why Python for Data Science?](#1-why-python-for-data-science)
2. [Setting Up Python](#2-setting-up-python)
3. [Basic Syntax and Variables](#3-basic-syntax-and-variables)
4. [Data Types and Structures](#4-data-types-and-structures)
5. [Control Flow](#5-control-flow)
6. [Functions and Modules](#6-functions-and-modules)
7. [File Handling](#7-file-handling)
8. [Python Libraries for Data Science](#8-python-libraries-for-data-science)
9. [Exercises](#9-exercises)

---

## 1. Why Python for Data Science?

Python is the go-to language for Data Science due to several reasons:

- **Simplicity**: Python has a readable and easy-to-learn syntax that is beginner-friendly.
- **Vast Libraries**: Python provides numerous libraries such as `NumPy`, `Pandas`, `Matplotlib`, and `Seaborn` that are crucial for data manipulation and visualization.
- **Community Support**: With an active and large community, Python has vast documentation, tutorials, and libraries that can assist in almost any challenge.
- **Integration**: Python integrates seamlessly with other programming languages and big data tools, making it versatile.

---

## 2. Setting Up Python

Before starting with Python, you need to set up the development environment. Here's how:

### Step 1: Install Python

- Download the latest version of Python from the official site: [Python.org](https://www.python.org/downloads/).
- During installation, make sure to check the box for "Add Python to PATH."

### Step 2: Install an IDE or Code Editor

You can write Python code in any text editor, but it's recommended to use an Integrated Development Environment (IDE) or code editor like:
- **VS Code**
- **Jupyter Notebooks**
- **PyCharm**

### Step 3: Verify the Installation

Once installed, open a terminal or command prompt and type:

```bash
python --version

```

If the installation was successful, you should see an output like this:

```bash
Python 3.x.x
```

---

## 3. Basic Syntax and Variables

### Introduction
Python is known for its simplicity and readability. The syntax of Python is designed to be clean and straightforward, making it an excellent language for beginners while also being powerful for advanced users. Below is an introduction to the basic syntax and variable handling in Python.

### 1. Python Indentation
Unlike many programming languages that use braces `{}` to define blocks of code, Python uses **indentation** (spaces or tabs) to denote block structures. This is a key feature of Python, and it is critical to ensure the correct indentation level, as improper indentation will result in an error.

**Example:**
```python
if True:
    print("This is inside an if block")  # This line is indented
```
### 2. Comments in Python
Python supports two types of comments:

- **Single-line comments** start with a #.
- **Multi-line comments** can be made using triple quotes ''' or """.
  
**Example:**
```python
# This is a single-line comment

"""
This is a multi-line comment
spanning multiple lines
"""

```
### 3. Variables in Python
Variables in Python do not require explicit declaration, and their data types are inferred based on the value assigned. You can assign values to variables and change their types dynamically.
**
Rules for Variable Names:**

- Variable names must start with a letter or an underscore (_).
- The rest of the name can contain letters, numbers, or underscores.
- Variable names are **case-sensitive** (name and Name are different).

**Example:**
 ```python
x = 10         # x is an integer
y = "Hello"    # y is a string
z = 3.14       # z is a floating-point number

# Variable reassignment
x = "Python"   # x is now a string
```

### 4. Variable Types
Python is dynamically typed, meaning you do not need to declare the type of a variable. Python will automatically interpret the variable type based on the assigned value.

- **Integers:** Whole numbers (e.g., x = 10)
- **Floating-point numbers**: Decimal numbers (e.g., y = 3.14)
- **Strings:** Text enclosed in quotes (e.g., z = "Hello")
- **Boolean**: True or False values (e.g., a = True)
- 
```python
age = 25                 # Integer
price = 19.99            # Float
name = "Alice"           # String
is_active = True         # Boolean
``` 
### 5. Assigning Multiple Variables

Python allows for multiple variables to be assigned in a single line.

**Example:**
```python
a, b, c = 1, 2, 3
x = y = z = "Same value"
``` 
### 6. Variable Type Casting
Python allows you to convert between types using casting functions:

- **int()** - Converts to an integer
- **float()** - Converts to a float
- **str()** - Converts to a string
- **bool()** - Converts to a boolean
**Example: ** 
```python
x = int(3.14)      # x will be 3
y = float("7.5")   # y will be 7.5
z = str(25)        # z will be '25'

```
### 7. Printing Variables
In Python, you can print variables using the **print()** function. You can also format output using f-strings for easy embedding of variables into strings.

**Example:**

```python
name = "John"
age = 30

# Simple print
print(name)

# Print with formatting
print(f"My name is {name} and I am {age} years old.")

```
### 8. Reserved Keywords
 Python has a set of reserved keywords that cannot be used as variable names. These include if, else, for, while, def, return, etc.

**Example of Reserved Keywords:**
```python
# Don't use these as variable names
if, else, for, while, class, return, True, False
```
This concludes the basics of Python's syntax and variable handling. With these foundational concepts, you can begin exploring more advanced language features.

---

# Data Types and Structures

## 1. Introduction
Python provides several built-in data types and data structures that make it easy to store and manipulate data. Understanding these is crucial for efficient programming. Below is a comprehensive guide to Python's key data types and structures.

## 2. Basic Data Types
Data Types already discussed in above for more you can check phyton doc

## 3. Data Structures

### 1. Lists
Lists are ordered, mutable (changeable) collections of items. Items in a list can be of different data types. Lists are defined using square brackets [].

**Example:**

```python
numbers = [1, 2, 3, 4, 5]
mixed_list = [1, "hello", True, 3.14]
```
- Accessing elements:

```python
 first_element = numbers[0]    # 1
```
- Modifying elements:
```python
  numbers[2] = 10
```
- List methods:
- 
  ```python
  numbers.append(6)      # Adds 6 at the end
  numbers.remove(10)     # Removes 10 from the list
 ```

### 2. Tuples
Tuples are similar to lists but are immutable (cannot be changed after creation). They are defined using parentheses ().

**Example:**

```python
coordinates = (10, 20)
  ```
- Accessing elements:
```python
x = coordinates[0]    # 10
```
- Tuples cannot be modified:
```python
# coordinates[0] = 15  -> This will raise an error
```
### 3. Dictionaries
Dictionaries store data in **key-value pairs**. They are unordered and mutable. Defined using curly braces {}, where each item is a key-value pair separated by a colon : .
**Example:**
```python
person = {
    "name": "Alice",
    "age": 30,
    "is_student": False
}
```

- Accessing values by key:
  ```python
  name = person["name"]    # "Alice"
  ```
- Modifying values:
   ```python
   person["age"] = 31
  ```
- Adding a new key-value pair:
   ```python
   person["city"] = "New York"
  ```
