# Python Interview Questions for Freshers

## Questions

1. [What is Python? What are the benefits of using Python?](#1-what-is-python-what-are-the-benefits-of-using-python)
2. [What is a dynamically typed language?](#2-what-is-a-dynamically-typed-language)
3. [What is an interpreted language?](#3-what-is-an-interpreted-language)
4. [What is PEP 8 and why is it important?](#4-what-is-pep-8-and-why-is-it-important)
5. [What is scope in Python?](#5-what-is-scope-in-python)
6. [What are lists and tuples? What is the key difference between them?](#6-what-are-lists-and-tuples-what-is-the-key-difference-between-them)
7. [What are the common built-in data types in Python?](#7-what-are-the-common-built-in-data-types-in-python)
8. [What is `pass` in Python?](#8-what-is-pass-in-python)
9. [What are modules and packages in Python?](#9-what-are-modules-and-packages-in-python)
10. [What are global, protected, and private attributes in Python?](#10-what-are-global-protected-and-private-attributes-in-python)
11. [What is the use of `self` in Python?](#11-what-is-the-use-of-self-in-python)
12. [What is `__init__()`?](#12-what-is-__init__)
13. [What are `break`, `continue`, and `pass` in Python?](#13-what-are-break-continue-and-pass-in-python)
14. [What are unit tests in Python?](#14-what-are-unit-tests-in-python)
15. [What is a docstring in Python?](#15-what-is-a-docstring-in-python)
16. [What is slicing in Python?](#16-what-is-slicing-in-python)
17. [How can you make a Python script executable on Unix?](#17-how-can-you-make-a-python-script-executable-on-unix)
18. [What is the difference between Python arrays and lists?](#18-what-is-the-difference-between-python-arrays-and-lists)

---

# Answers

## 1. What is Python? What are the benefits of using Python?

Python is a **high-level, interpreted, general-purpose programming language** known for simple syntax and readability.

### Key Benefits

* Easy to learn and read
* Dynamically typed
* Supports object-oriented programming
* Large standard library
* Large third-party ecosystem
* Cross-platform
* Open source
* Useful for web development, automation, data engineering, AI, machine learning, and scripting

### Example

```python
def greet(name):
    return f"Hello, {name}"

print(greet("Alice"))
```

**Interview answer:**
Python is a high-level, interpreted, dynamically typed programming language known for readable syntax, rapid development, and a large ecosystem of libraries.

[Back to Questions](#questions)

---

## 2. What is a dynamically typed language?

A dynamically typed language determines variable types at **runtime**.

Python does not require explicit variable type declarations.

```python
x = 10
print(type(x))

x = "Python"
print(type(x))
```

The same variable can reference objects of different types.

**Interview answer:**
Python is dynamically typed because variable types are determined at runtime rather than being declared in advance.

[Back to Questions](#questions)

---

## 3. What is an interpreted language?

Python is commonly described as an interpreted language.

In CPython, source code is first converted into **bytecode**, which is then executed by the Python Virtual Machine.

```text
Python source (.py)
        ↓
     Bytecode
        ↓
Python Virtual Machine
        ↓
     Execution
```

**Interview answer:**
Python is generally called interpreted, although CPython first compiles source code into bytecode and then executes that bytecode.

[Back to Questions](#questions)

---

## 4. What is PEP 8 and why is it important?

PEP stands for **Python Enhancement Proposal**.

PEP 8 is Python's official style guide.

It provides conventions for:

* Naming
* Indentation
* Imports
* Whitespace
* Code formatting
* Line length

Example:

```python
def calculate_total_price():
    pass
```

PEP 8 improves readability and consistency across Python projects.

**Interview answer:**
PEP 8 is Python's official coding style guide. It defines conventions that make Python code more readable and consistent.

[Back to Questions](#questions)

---

## 5. What is scope in Python?

Scope defines where a variable can be accessed.

Python follows the **LEGB** rule:

* **L**ocal
* **E**nclosing
* **G**lobal
* **B**uilt-in

Example:

```python
x = 10

def test():
    y = 20
    print(x, y)

test()
```

Here:

* `x` is global
* `y` is local

**Interview answer:**
Scope determines where names are accessible. Python resolves names using the LEGB rule: Local, Enclosing, Global, and Built-in.

[Back to Questions](#questions)

---

## 6. What are lists and tuples? What is the key difference between them?

Lists and tuples are ordered collections.

### List

```python
numbers = [1, 2, 3]
```

Lists are **mutable**.

### Tuple

```python
numbers = (1, 2, 3)
```

Tuples are **immutable**.

| List                       | Tuple                   |
| -------------------------- | ----------------------- |
| Mutable                    | Immutable               |
| Uses `[]`                  | Uses `()`               |
| Can be modified            | Cannot be modified      |
| Suitable for changing data | Suitable for fixed data |

**Interview answer:**
The key difference is that lists are mutable while tuples are immutable.

[Back to Questions](#questions)

---

## 7. What are the common built-in data types in Python?

Common Python built-in types include:

| Category | Types                     |
| -------- | ------------------------- |
| Numeric  | `int`, `float`, `complex` |
| Boolean  | `bool`                    |
| Text     | `str`                     |
| Sequence | `list`, `tuple`, `range`  |
| Mapping  | `dict`                    |
| Set      | `set`, `frozenset`        |
| Null     | `NoneType`                |

Example:

```python
age = 30
name = "Alice"
skills = ["Python", "SQL"]
user = {"name": "Alice", "age": 30}
```

**Interview answer:**
Common built-in Python types include integers, floats, strings, lists, tuples, dictionaries, sets, booleans, ranges, and `None`.

[Back to Questions](#questions)

---

## 8. What is `pass` in Python?

`pass` is a null statement.

It performs no operation.

It is commonly used as a placeholder.

```python
def future_function():
    pass
```

**Interview answer:**
`pass` does nothing and is used when Python requires a statement syntactically but no implementation is needed yet.

[Back to Questions](#questions)

---

## 9. What are modules and packages in Python?

A **module** is typically a Python file containing reusable code.

Example:

```python
import math
```

A **package** organizes multiple modules under a common namespace.

Example structure:

```text
utilities/
├── __init__.py
├── math_utils.py
└── string_utils.py
```

**Interview answer:**
A module is usually a single `.py` file, while a package groups related modules together.

[Back to Questions](#questions)

---

## 10. What are global, protected, and private attributes in Python?

Python does not use strict access modifiers like Java.

Instead, naming conventions are used.

```python
class Employee:
    def __init__(self):
        self.name = "Alice"
        self._salary = 50000
        self.__password = "secret"
```

Meaning:

* `name` → public
* `_salary` → protected/internal-use convention
* `__password` → name-mangled

Double underscores do not provide true security.

**Interview answer:**
Python uses naming conventions instead of strict access modifiers. A single underscore indicates internal use, while double underscores trigger name mangling.

[Back to Questions](#questions)

---

## 11. What is the use of `self` in Python?

`self` refers to the current instance of a class.

```python
class Employee:
    def __init__(self, name):
        self.name = name
```

Here:

```python
self.name
```

belongs to the current object.

`self` is a convention, not a Python keyword.

**Interview answer:**
`self` represents the current instance and allows instance methods to access the object's attributes and methods.

[Back to Questions](#questions)

---

## 12. What is `__init__()`?

`__init__()` initializes an object after it has been created.

```python
class Employee:
    def __init__(self, name):
        self.name = name

employee = Employee("Alice")
```

More precisely:

```text
__new__()  → creates the object
__init__() → initializes the object
```

**Interview answer:**
`__init__()` is a special method automatically called after object creation and is normally used to initialize instance attributes.

[Back to Questions](#questions)

---

## 13. What are `break`, `continue`, and `pass` in Python?

| Keyword    | Purpose                    |
| ---------- | -------------------------- |
| `break`    | Exit the loop              |
| `continue` | Skip the current iteration |
| `pass`     | Do nothing                 |

Example:

```python
for i in range(5):
    if i == 2:
        continue

    print(i)
```

Output:

```text
0
1
3
4
```

**Interview answer:**
`break` exits a loop, `continue` skips the current iteration, and `pass` performs no operation.

[Back to Questions](#questions)

---

## 14. What are unit tests in Python?

Unit tests test small parts of an application independently.

Common examples include testing:

* Functions
* Methods
* Classes

Python provides the built-in `unittest` framework.

```python
import unittest

class TestMath(unittest.TestCase):

    def test_addition(self):
        self.assertEqual(2 + 3, 5)
```

Popular Python testing frameworks include:

* `unittest`
* `pytest`

**Interview answer:**
Unit tests verify individual components independently to catch defects and prevent regressions.

[Back to Questions](#questions)

---

## 15. What is a docstring in Python?

A docstring documents a module, class, function, or method.

```python
def add(a, b):
    """Return the sum of two numbers."""
    return a + b
```

A docstring can be accessed using:

```python
print(add.__doc__)
```

or:

```python
help(add)
```

**Interview answer:**
A docstring is a documentation string associated with Python modules, classes, functions, or methods.

[Back to Questions](#questions)

---

## 16. What is slicing in Python?

Slicing extracts part of a sequence.

Syntax:

```python
sequence[start:stop:step]
```

Example:

```python
numbers = [1, 2, 3, 4, 5]

print(numbers[1:4])
```

Output:

```text
[2, 3, 4]
```

Reverse a sequence:

```python
numbers[::-1]
```

**Interview answer:**
Slicing extracts part of a sequence using `[start:stop:step]`. The start is inclusive and the stop is exclusive.

[Back to Questions](#questions)

---

## 17. How can you make a Python script executable on Unix?

Add a shebang:

```python
#!/usr/bin/env python3
```

Give the file executable permission:

```bash
chmod +x script.py
```

Then run:

```bash
./script.py
```

**Interview answer:**
Add a Python shebang, make the file executable with `chmod +x`, and execute it directly.

[Back to Questions](#questions)

---

## 18. What is the difference between Python arrays and lists?

Python lists are general-purpose containers.

```python
values = [1, "Python", 3.14]
```

Typed arrays contain compatible element types.

```python
from array import array

numbers = array("i", [1, 2, 3])
```

| List                               | Array                   |
| ---------------------------------- | ----------------------- |
| Can contain different object types | Usually homogeneous     |
| General-purpose                    | Typed/numerical         |
| Built-in syntax                    | Requires module/library |

For data-science workloads, NumPy arrays are commonly used.

```python
import numpy as np

numbers = np.array([1, 2, 3])
```

**Interview answer:**
Lists are general-purpose containers that can hold mixed object types, while arrays are generally designed for homogeneous typed data.

[Back to Questions](#questions)
