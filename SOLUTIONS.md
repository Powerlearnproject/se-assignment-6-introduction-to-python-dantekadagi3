Question 1.
Python is a high-level, interpreted programming language known for its simplicity and readability. Created by Guido van Rossum and first released in 1991, Python has become one of the most popular programming languages due to its versatility and ease of use.

### Key Features of Python

1. **Readability and Simplicity**:
   - Python’s syntax is designed to be easy to read and write. It uses indentation to define code blocks, making the code more readable and reducing the likelihood of errors.
   - Example:
     ```python
     def greet(name):
         print(f"Hello, {name}!")
     ```

2. **Interpreted Language**:
   - Python code is executed line-by-line, which makes debugging easier and code execution more flexible.
   - Example:
     ```python
     print("This will be executed immediately.")
     ```

3. **Dynamic Typing**:
   - Variables in Python are dynamically typed, meaning you don’t need to declare their type explicitly.
   - Example:
     ```python
     age = 25
     age = "twenty-five"  # This is valid in Python
     ```

4. **Extensive Standard Library**:
   - Python comes with a comprehensive standard library that includes modules and packages for a wide variety of tasks, such as file I/O, system calls, and even web services.
   - Example:
     ```python
     import math
     print(math.sqrt(16))  # Output: 4.0
     ```

5. **Cross-Platform Compatibility**:
   - Python runs on various operating systems, including Windows, macOS, and Linux, making it a versatile choice for cross-platform development.
   - Example:
     ```python
     import os
     print(os.name)  # Outputs the name of the operating system
     ```

6. **Large Community and Ecosystem**:
   - Python has a large and active community, contributing to a rich ecosystem of third-party packages and frameworks.
   - Example: `numpy` for numerical computing, `pandas` for data manipulation, `requests` for HTTP requests, etc.

### Use Cases Where Python is Particularly Effective

1. **Web Development**:
   - Python is widely used in web development with frameworks such as Django and Flask.
   - Example:
     ```python
     from flask import Flask
     app = Flask(__name__)

     @app.route('/')
     def home():
         return "Hello, World!"

     if __name__ == '__main__':
         app.run(debug=True)
     ```

2. **Data Science and Machine Learning**:
   - Python is a preferred language in data science due to libraries like `pandas`, `numpy`, `scikit-learn`, and `TensorFlow`.
   - Example:
     ```python
     import pandas as pd

     data = pd.read_csv('data.csv')
     print(data.head())
     ```

3. **Automation and Scripting**:
   - Python is often used for scripting to automate repetitive tasks such as file manipulation, web scraping, and data processing.
   - Example:
     ```python
     import os

     for filename in os.listdir('.'):
         if filename.endswith('.txt'):
             print(filename)
     ```

4. **Scientific Computing**:
   - Python is used in scientific research for simulations, data analysis, and visualization.
   - Example:
     ```python
     import numpy as np

     array = np.array([1, 2, 3, 4])
     print(np.mean(array))  # Output: 2.5
     ```

5. **Game Development**:
   - Python is used in game development with libraries like Pygame.
   - Example:
     ```python
     import pygame

     pygame.init()
     screen = pygame.display.set_mode((640, 480))
     pygame.display.set_caption('Simple Game')
     running = True

     while running:
         for event in pygame.event.get():
             if event.type == pygame.QUIT:
                 running = False

     pygame.quit()
     ```

6. **Artificial Intelligence**:
   - Python is extensively used in AI development, with frameworks like TensorFlow, Keras, and PyTorch.
   - Example:
     ```python
     import tensorflow as tf

     model = tf.keras.models.Sequential([
         tf.keras.layers.Dense(128, activation='relu'),
         tf.keras.layers.Dense(10, activation='softmax')
     ])
     ```

Question 2
### Installing Python on Linux (Ubuntu 22.04 LTS)

#### Step 1: Update the Package List

Before installing any new software, it’s a good practice to update the package list to ensure you get the latest versions available.

```bash
sudo apt update
```

#### Step 2: Install Python

Ubuntu 22.04 LTS comes with Python 3 pre-installed, but it’s advisable to ensure you have the latest version.

1. **Install Python 3:**

   ```bash
   sudo apt install python3
   ```

2. **Install Python Package Manager (pip):**

   ```bash
   sudo apt install python3-pip
   ```

#### Step 3: Verify the Installation

To check if Python and pip are installed correctly, you can use the following commands:

1. **Verify Python installation:**

   ```bash
   python3 --version
   ```

   This should output something like `Python 3.x.x`, indicating the installed Python version.

2. **Verify pip installation:**

   ```bash
   pip3 --version
   ```

   This should output the version of pip installed, such as `pip 21.x.x from ...`.

#### Step 4: Set Up a Virtual Environment

Virtual environments are useful for creating isolated Python environments for different projects, preventing conflicts between dependencies.

1. **Install `venv` module:**

   The `venv` module is included in the Python standard library for Python 3.3 and above. Ensure it’s installed with:

   ```bash
   sudo apt install python3-venv
   ```

2. **Create a Virtual Environment:**

   Navigate to your project directory or create a new one:

   ```bash
   mkdir my_project
   cd my_project
   ```

   Then create a virtual environment:

   ```bash
   python3 -m venv myenv
   ```

   Here, `myenv` is the name of the virtual environment. You can name it anything you like.

3. **Activate the Virtual Environment:**

   To start using the virtual environment, you need to activate it:

   ```bash
   source myenv/bin/activate
   ```

   Once activated, your command prompt will change to indicate that you are now working inside the virtual environment.

4. **Deactivate the Virtual Environment:**

   When you are done working in the virtual environment, you can deactivate it by simply running:

   ```bash
   deactivate
   ```

#### Summary of Commands

```bash
# Update package list
sudo apt update

# Install Python 3
sudo apt install python3

# Install pip
sudo apt install python3-pip

# Verify installations
python3 --version
pip3 --version

# Install venv module
sudo apt install python3-venv

# Create and activate a virtual environment
mkdir my_project
cd my_project
python3 -m venv myenv
source myenv/bin/activate

# Deactivate the virtual environment
deactivate
```

By following these steps, you’ll have Python installed and a virtual environment set up on Ubuntu 22.04 LTS, ready for your development work.


Question 3
Basic python syntax that prints "Hello World"

print("Hello, World!")

Explanation of Basic Syntax Elements
print Function:

The print() function is a built-in Python function that outputs text to the console.
The text to be printed is passed as an argument to the print() function.
Strings:

The text "Hello, World!" is a string, which is a sequence of characters enclosed in quotation marks (either single ' or double " quotes).
In this example, double quotes are used to enclose the string.
Parentheses:

The print function call includes parentheses () to enclose its arguments.
This syntax is required for function calls in Python, indicating what data the function should process.
Function Call:

print("Hello, World!") is a function call, where print is the function name, and ("Hello, World!") is the argument passed to the function.
Functions in Python are invoked using their name followed by parentheses containing any necessary arguments.


Question 4
### Basic Data Types in Python

1. **Integers (int)**:
   - Whole numbers, positive or negative, without a decimal point.
   - Example: `5`, `-10`

2. **Floating-Point Numbers (float)**:
   - Numbers with a decimal point or in exponential (scientific) notation.
   - Example: `3.14`, `-2.5`, `2e10`

3. **Strings (str)**:
   - A sequence of characters enclosed in single, double, or triple quotes.
   - Example: `"hello"`, `'world'`, `"""This is a string"""`

4. **Booleans (bool)**:
   - Represents one of two values: `True` or `False`.
   - Example: `True`, `False`

5. **Lists (list)**:
   - Ordered, mutable collection of items enclosed in square brackets.
   - Example: `[1, 2, 3]`, `["apple", "banana", "cherry"]`

6. **Tuples (tuple)**:
   - Ordered, immutable collection of items enclosed in parentheses.
   - Example: `(1, 2, 3)`, `("apple", "banana", "cherry")`

7. **Dictionaries (dict)**:
   - Unordered, mutable collection of key-value pairs enclosed in curly braces.
   - Example: `{"name": "Alice", "age": 30}`, `{"key1": "value1", "key2": "value2"}`

8. **Sets (set)**:
   - Unordered collection of unique items enclosed in curly braces.
   - Example: `{1, 2, 3}`, `{"apple", "banana", "cherry"}`

### Script Demonstrating Variables of Different Data Types

```python
# Integers
age = 25
print("Age:", age)

# Floating-Point Numbers
height = 5.9
print("Height:", height)

# Strings
name = "Alice"
print("Name:", name)

# Booleans
is_student = True
print("Is Student:", is_student)

# Lists
fruits = ["apple", "banana", "cherry"]
print("Fruits:", fruits)

# Tuples
coordinates = (10.0, 20.0)
print("Coordinates:", coordinates)

# Dictionaries
person = {"name": "Bob", "age": 30}
print("Person:", person)

# Sets
unique_numbers = {1, 2, 3, 4, 5}
print("Unique Numbers:", unique_numbers)
```

### Explanation

1. **Integers (int)**:
   - `age = 25`: A variable `age` is created and assigned the integer value `25`.

2. **Floating-Point Numbers (float)**:
   - `height = 5.9`: A variable `height` is created and assigned the float value `5.9`.

3. **Strings (str)**:
   - `name = "Alice"`: A variable `name` is created and assigned the string value `"Alice"`.

4. **Booleans (bool)**:
   - `is_student = True`: A variable `is_student` is created and assigned the boolean value `True`.

5. **Lists (list)**:
   - `fruits = ["apple", "banana", "cherry"]`: A variable `fruits` is created and assigned a list of strings.

6. **Tuples (tuple)**:
   - `coordinates = (10.0, 20.0)`: A variable `coordinates` is created and assigned a tuple containing two float values.

7. **Dictionaries (dict)**:
   - `person = {"name": "Bob", "age": 30}`: A variable `person` is created and assigned a dictionary with keys `"name"` and `"age"`.

8. **Sets (set)**:
   - `unique_numbers = {1, 2, 3, 4, 5}`: A variable `unique_numbers` is created and assigned a set of unique integers.

This script demonstrates how to create and use variables of different data types in Python. Each variable is printed to the console to show its value.


Question 5
### Conditional Statements

Conditional statements in Python are used to execute code based on certain conditions. The most common conditional statement is the `if-else` statement.

#### `if-else` Statement

The `if-else` statement evaluates a condition (an expression that returns `True` or `False`) and executes code blocks based on the result of the evaluation.

##### Syntax:

```python
if condition:
    # Code block to execute if condition is True
else:
    # Code block to execute if condition is False
```

##### Example:

```python
age = 20

if age >= 18:
    print("You are an adult.")
else:
    print("You are a minor.")
```

In this example, the condition `age >= 18` is evaluated. If the condition is `True`, the message "You are an adult." is printed. Otherwise, the message "You are a minor." is printed.

### Loops

Loops in Python are used to execute a block of code repeatedly as long as a condition is met. The most common loops are the `for` loop and the `while` loop.

#### `for` Loop

The `for` loop is used to iterate over a sequence (such as a list, tuple, dictionary, set, or string) and execute a block of code for each item in the sequence.

##### Syntax:

```python
for item in sequence:
    # Code block to execute for each item
```

##### Example:

```python
fruits = ["apple", "banana", "cherry"]

for fruit in fruits:
    print(fruit)
```

In this example, the `for` loop iterates over each item in the `fruits` list and prints each fruit.

### Combined Example

Here’s an example that combines an `if-else` statement and a `for` loop:

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

for number in numbers:
    if number % 2 == 0:
        print(f"{number} is even")
    else:
        print(f"{number} is odd")
```

#### Explanation:

1. **List of Numbers**:
   - A list `numbers` is created containing integers from 1 to 10.

2. **`for` Loop**:
   - The `for` loop iterates over each number in the `numbers` list.

3. **`if-else` Statement**:
   - Inside the loop, an `if-else` statement checks whether the current number is even or odd using the modulo operator `%`.
   - If `number % 2 == 0` (the remainder when `number` is divided by 2 is zero), the number is even, and the corresponding message is printed.
   - Otherwise, the number is odd, and the corresponding message is printed.

### Output:

```
1 is odd
2 is even
3 is odd
4 is even
5 is odd
6 is even
7 is odd
8 is even
9 is odd
10 is even
```

This example demonstrates the use of both conditional statements and loops in Python to evaluate conditions and iterate over sequences.


Question 6
### Functions in Python

Functions in Python are blocks of reusable code that perform a specific task. They are useful for:

- **Modularity**: Breaking down complex problems into smaller, manageable pieces.
- **Reusability**: Allowing code to be reused in different parts of a program without rewriting it.
- **Readability**: Making code easier to understand by encapsulating logic within well-named functions.

#### Defining a Function

A function is defined using the `def` keyword, followed by the function name and parentheses `()` that may contain parameters.

##### Syntax:

```python
def function_name(parameters):
    # Code block (function body)
    return result
```

- `function_name`: The name of the function.
- `parameters`: The values passed to the function (optional).
- `return`: The statement used to return a value from the function (optional).

### Example: Function to Return the Sum of Two Arguments

Here's a Python function that takes two arguments and returns their sum:

```python
def add_numbers(a, b):
    """Return the sum of two numbers."""
    return a + b
```

#### Explanation:

- `def add_numbers(a, b)`: Defines a function named `add_numbers` that takes two parameters, `a` and `b`.
- `return a + b`: Returns the sum of `a` and `b`.

#### Calling the Function

To use the function, you call it by its name and pass the required arguments:

```python
# Example of calling the add_numbers function
result = add_numbers(5, 3)
print("The sum is:", result)
```

#### Explanation:

- `add_numbers(5, 3)`: Calls the `add_numbers` function with arguments `5` and `3`.
- The result of the function call (the sum of 5 and 3) is assigned to the variable `result`.
- `print("The sum is:", result)`: Prints the result.

### Full Example

Here’s the complete code:

```python
def add_numbers(a, b):
    """Return the sum of two numbers."""
    return a + b

# Example of calling the add_numbers function
result = add_numbers(5, 3)
print("The sum is:", result)
```

### Output:

```
The sum is: 8
```

This example demonstrates how to define a function, call it with arguments, and use its return value. Functions help organize code, making it more modular, reusable, and readable.


Question 7
### Differences Between Lists and Dictionaries in Python

1. **Structure**:
   - **Lists**: Ordered collection of items, which can be of any data type. Lists are indexed by integers.
   - **Dictionaries**: Unordered collection of key-value pairs. Each key must be unique and is used to access the corresponding value.

2. **Syntax**:
   - **Lists**: Created using square brackets `[]`.
   - **Dictionaries**: Created using curly braces `{}` with key-value pairs separated by colons `:`.

3. **Accessing Elements**:
   - **Lists**: Elements are accessed using their index (starting from 0).
   - **Dictionaries**: Elements are accessed using their keys.

4. **Mutability**:
   - Both lists and dictionaries are mutable, meaning their contents can be changed.

### Script Demonstrating Basic Operations on Lists and Dictionaries

#### Creating a List of Numbers

```python
# Create a list of numbers
numbers = [1, 2, 3, 4, 5]
print("List of numbers:", numbers)
```

#### Basic Operations on Lists

1. **Accessing Elements**:
   ```python
   print("First element:", numbers[0])
   print("Last element:", numbers[-1])
   ```

2. **Adding Elements**:
   ```python
   numbers.append(6)
   print("After appending 6:", numbers)
   ```

3. **Removing Elements**:
   ```python
   numbers.remove(3)
   print("After removing 3:", numbers)
   ```

4. **Slicing**:
   ```python
   print("Sliced list (first three elements):", numbers[:3])
   ```

#### Creating a Dictionary with Key-Value Pairs

```python
# Create a dictionary with key-value pairs
person = {
    "name": "Alice",
    "age": 30,
    "city": "New York"
}
print("Dictionary:", person)
```

#### Basic Operations on Dictionaries

1. **Accessing Elements**:
   ```python
   print("Name:", person["name"])
   print("Age:", person["age"])
   ```

2. **Adding or Updating Elements**:
   ```python
   person["email"] = "alice@example.com"
   print("After adding email:", person)
   ```

3. **Removing Elements**:
   ```python
   del person["age"]
   print("After removing age:", person)
   ```

4. **Iterating Through Keys and Values**:
   ```python
   print("Keys and values in the dictionary:")
   for key, value in person.items():
       print(f"{key}: {value}")
   ```

### Full Script

Here is the complete script with all the operations:

```python
# List operations
numbers = [1, 2, 3, 4, 5]
print("List of numbers:", numbers)

# Accessing elements
print("First element:", numbers[0])
print("Last element:", numbers[-1])

# Adding elements
numbers.append(6)
print("After appending 6:", numbers)

# Removing elements
numbers.remove(3)
print("After removing 3:", numbers)

# Slicing
print("Sliced list (first three elements):", numbers[:3])

# Dictionary operations
person = {
    "name": "Alice",
    "age": 30,
    "city": "New York"
}
print("Dictionary:", person)

# Accessing elements
print("Name:", person["name"])
print("Age:", person["age"])

# Adding or updating elements
person["email"] = "alice@example.com"
print("After adding email:", person)

# Removing elements
del person["age"]
print("After removing age:", person)

# Iterating through keys and values
print("Keys and values in the dictionary:")
for key, value in person.items():
    print(f"{key}: {value}")
```

### Explanation

- **List Operations**:
  - **Creating a list**: `numbers` is initialized with `[1, 2, 3, 4, 5]`.
  - **Accessing elements**: The first and last elements are accessed using indices.
  - **Adding elements**: `append(6)` adds `6` to the end of the list.
  - **Removing elements**: `remove(3)` removes the first occurrence of `3` from the list.
  - **Slicing**: `[:3]` gets the first three elements of the list.

- **Dictionary Operations**:
  - **Creating a dictionary**: `person` is initialized with key-value pairs for name, age, and city.
  - **Accessing elements**: Values are accessed using their keys.
  - **Adding/updating elements**: Adding a new key-value pair for email.
  - **Removing elements**: Deleting the key-value pair for age.
  - **Iterating**: Looping through the dictionary to print each key-value pair.

This script demonstrates basic operations for both lists and dictionaries, highlighting their differences and typical use cases.

Question 8
### Exception Handling in Python

Exception handling in Python allows you to manage and respond to errors that occur during program execution. It prevents the program from crashing and enables you to handle unexpected conditions gracefully. The key components of exception handling are the `try`, `except`, and `finally` blocks.

#### Components:

1. **`try` Block**:
   - Contains the code that might raise an exception.
   
2. **`except` Block**:
   - Contains the code that executes if an exception occurs in the `try` block.
   - You can specify the type of exception to catch or use a general `except` block to catch any exception.
   
3. **`finally` Block**:
   - Contains the code that will always execute, regardless of whether an exception was raised or not.
   - Often used for cleanup actions (e.g., closing files or releasing resources).

### Example of Exception Handling

Here’s an example of how to use `try`, `except`, and `finally` blocks to handle errors in a Python script:

```python
def divide_numbers(a, b):
    try:
        # Try to perform division
        result = a / b
    except ZeroDivisionError as e:
        # Handle division by zero error
        print("Error: Cannot divide by zero.")
        print("Exception message:", e)
        result = None
    except TypeError as e:
        # Handle type error (if non-numeric types are passed)
        print("Error: Invalid input types. Both arguments must be numbers.")
        print("Exception message:", e)
        result = None
    else:
        # If no exception occurs
        print("Division successful.")
    finally:
        # Always execute this block
        print("Execution of finally block.")
    
    return result

# Example calls
print("Result:", divide_numbers(10, 2))    # Should print the result of 10 / 2
print("Result:", divide_numbers(10, 0))    # Should handle division by zero
print("Result:", divide_numbers(10, 'a'))  # Should handle type error
```

### Explanation

1. **`try` Block**:
   - The division operation `result = a / b` is placed inside the `try` block because it may raise exceptions (e.g., `ZeroDivisionError` or `TypeError`).

2. **`except` Blocks**:
   - **`except ZeroDivisionError as e`**: Catches and handles the division by zero error, printing an appropriate message and setting `result` to `None`.
   - **`except TypeError as e`**: Catches and handles the type error (e.g., if non-numeric types are passed), printing an appropriate message and setting `result` to `None`.

3. **`else` Block**:
   - The `else` block executes if no exceptions are raised in the `try` block. It prints a success message.

4. **`finally` Block**:
   - The `finally` block executes regardless of whether an exception occurred or not. It prints a message indicating the execution of the block, useful for cleanup operations.

### Output

```
Division successful.
Execution of finally block.
Result: 5.0
Error: Cannot divide by zero.
Exception message: division by zero
Execution of finally block.
Result: None
Error: Invalid input types. Both arguments must be numbers.
Exception message: unsupported operand type(s) for /: 'int' and 'str'
Execution of finally block.
Result: None
```

This example demonstrates how to handle different types of exceptions using `try`, `except`, and `finally` blocks, ensuring that the program continues to run smoothly even when errors occur.


Question 9
### Modules and Packages in Python

#### Modules

A module in Python is a file containing Python code (functions, classes, variables) that can be imported and used in other Python scripts. Modules help organize and reuse code across multiple programs.

##### Creating a Module

To create a module, you simply save a Python script with a `.py` extension. For example, `mymodule.py` could be a module containing some functions:

```python
# mymodule.py
def greet(name):
    return f"Hello, {name}!"
```

##### Importing a Module

You can import and use a module in another script using the `import` statement:

```python
# script.py
import mymodule

message = mymodule.greet("Alice")
print(message)  # Output: Hello, Alice!
```

#### Packages

A package is a way of organizing related modules into a directory hierarchy. A package is a directory containing a special `__init__.py` file (which can be empty) and can include multiple modules and sub-packages.

##### Creating a Package

Here’s an example structure of a package named `mypackage`:

```
mypackage/
    __init__.py
    module1.py
    module2.py
```

##### Importing from a Package

You can import modules from a package using the dot notation:

```python
# script.py
from mypackage import module1, module2

result1 = module1.some_function()
result2 = module2.another_function()
```

### Example Using the `math` Module

The `math` module is a standard Python module providing mathematical functions.

##### Importing the `math` Module

You can import the entire `math` module or specific functions from it:

```python
import math
# or
from math import sqrt, pi
```

##### Using the `math` Module

Here’s an example script demonstrating the use of the `math` module:

```python
import math

# Calculate the square root of a number
number = 16
sqrt_number = math.sqrt(number)
print(f"The square root of {number} is {sqrt_number}")

# Calculate the sine of an angle (in radians)
angle = math.pi / 2  # 90 degrees
sine_value = math.sin(angle)
print(f"The sine of {angle} radians is {sine_value}")

# Using constants from the math module
print(f"The value of pi is {math.pi}")
print(f"The value of e is {math.e}")

# Using other functions from the math module
factorial_5 = math.factorial(5)
print(f"The factorial of 5 is {factorial_5}")
```

### Explanation

1. **Importing the `math` Module**:
   - `import math`: Imports the entire `math` module.

2. **Using `math.sqrt`**:
   - `math.sqrt(number)`: Calculates the square root of `number`.

3. **Using `math.sin`**:
   - `math.sin(angle)`: Calculates the sine of `angle` (in radians).

4. **Using Constants**:
   - `math.pi`: The mathematical constant π (pi).
   - `math.e`: The mathematical constant e (Euler's number).

5. **Using `math.factorial`**:
   - `math.factorial(5)`: Calculates the factorial of 5.

### Output

```
The square root of 16 is 4.0
The sine of 1.5707963267948966 radians is 1.0
The value of pi is 3.141592653589793
The value of e is 2.718281828459045
The factorial of 5 is 120
```

This example demonstrates how to import and use the `math` module, showcasing various mathematical functions and constants available in the module. Modules and packages are essential for organizing and reusing code, making Python programming more modular and maintainable.


Question 10
### Reading from Files in Python

To read from files in Python, you can use the `open()` function along with methods like `read()`, `readline()`, or `readlines()`.

#### Example: Reading the Content of a File

Let's assume we have a file named `example.txt` with the following content:

```
Hello, this is line 1.
This is line 2.
And this is line 3.
```

Here's a script that reads the content of the file and prints it to the console:

```python
# Reading from a file
file_path = 'example.txt'

try:
    with open(file_path, 'r') as file:
        content = file.read()
        print(content)
except FileNotFoundError:
    print(f"Error: The file '{file_path}' was not found.")
except IOError as e:
    print(f"Error: Could not read the file '{file_path}'.")
    print(f"Exception message: {e}")
```

#### Explanation

- **Opening a File**: `open(file_path, 'r')` opens the file `example.txt` in read mode (`'r'`).
- **Reading the Content**: `file.read()` reads the entire content of the file as a string and assigns it to the variable `content`.
- **Printing the Content**: `print(content)` prints the content to the console.

### Writing to Files in Python

To write to files in Python, you can use the `open()` function with modes like `'w'` (write) or `'a'` (append).

#### Example: Writing a List of Strings to a File

Let's write a list of strings to a file named `output.txt`:

```python
# Writing to a file
output_file_path = 'output.txt'
lines_to_write = [
    "This is line 1.",
    "And this is line 2.",
    "Finally, this is line 3."
]

try:
    with open(output_file_path, 'w') as file:
        for line in lines_to_write:
            file.write(line + '\n')
    print(f"Successfully wrote {len(lines_to_write)} lines to '{output_file_path}'.")
except IOError as e:
    print(f"Error: Could not write to the file '{output_file_path}'.")
    print(f"Exception message: {e}")
```

#### Explanation

- **Opening a File for Writing**: `open(output_file_path, 'w')` opens the file `output.txt` in write mode (`'w'`).
- **Writing to the File**: `file.write(line + '\n')` writes each line from `lines_to_write` to the file, adding a newline character `\n` after each line.
- **Success Message**: `print(f"Successfully wrote {len(lines_to_write)} lines to '{output_file_path}'.")` prints a success message after writing.

### Full Scripts

Here are the complete scripts for reading from a file and writing to a file:

#### Reading from a File

```python
# Reading from a file
file_path = 'example.txt'

try:
    with open(file_path, 'r') as file:
        content = file.read()
        print(content)
except FileNotFoundError:
    print(f"Error: The file '{file_path}' was not found.")
except IOError as e:
    print(f"Error: Could not read the file '{file_path}'.")
    print(f"Exception message: {e}")
```

#### Writing to a File

```python
# Writing to a file
output_file_path = 'output.txt'
lines_to_write = [
    "This is line 1.",
    "And this is line 2.",
    "Finally, this is line 3."
]

try:
    with open(output_file_path, 'w') as file:
        for line in lines_to_write:
            file.write(line + '\n')
    print(f"Successfully wrote {len(lines_to_write)} lines to '{output_file_path}'.")
except IOError as e:
    print(f"Error: Could not write to the file '{output_file_path}'.")
    print(f"Exception message: {e}")
```

### Output

Assuming `example.txt` contains the given content and `output.txt` is written successfully, the output would be:

```
Hello, this is line 1.
This is line 2.
And this is line 3.

Successfully wrote 3 lines to 'output.txt'.
```

These scripts demonstrate how to read from and write to files in Python, handling different scenarios such as file not found or permission errors. Adjust the file paths and content according to your specific use case.