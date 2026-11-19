# Day 10 – Calculator

## Project Overview

This project is a command-line calculator built using Python. It performs four basic mathematical operations: addition, subtraction, multiplication, and division.

The calculator uses separate functions for each mathematical operation and stores these functions inside a dictionary. Based on the operation selected by the user, the program calls the corresponding function and displays the result.

It also allows users to continue calculating with the previous result or restart the calculator to perform a new calculation.

This project is part of my **100 Days of Python** learning journey.

## Features

- **Addition (+):** Adds two numbers.
- **Subtraction (-):** Subtracts the second number from the first number.
- **Multiplication (*):** Multiplies two numbers.
- **Division (/):** Divides the first number by the second number.
- **Continuous Calculation:** Allows users to use the previous result for the next calculation.
- **New Calculation:** Allows users to restart the calculator.
- **Function-Based Operations:** Each mathematical operation is handled by a separate function.

## How the Program Works

### 1. Importing the Calculator Logo

The program imports the logo from a separate Python file named `art.py`.

```python
import art

print(art.logo)
```

This keeps the logo separate from the main calculator logic.

### 2. Creating Mathematical Functions

Four separate functions are created to perform mathematical operations.

```python
def add(n1, n2):
    return n1 + n2

def subtract(n1, n2):
    return n1 - n2

def multiply(n1, n2):
    return n1 * n2

def divide(n1, n2):
    return n1 / n2
```

Each function accepts two numbers and returns the calculated result.

### 3. Storing Functions in a Dictionary

The calculator uses a dictionary to connect operation symbols with their corresponding functions.

```python
operations = {
    "+": add,
    "-": subtract,
    "*": multiply,
    "/": divide
}
```

For example, when the user selects `+`, the program accesses the `add` function from the dictionary.

### 4. Taking User Input

The program asks the user to enter the first number, select an operation, and enter the next number.

The inputs are converted into floating-point numbers using `float()`.

### 5. Performing the Calculation

The selected function is called using the operation symbol.

```python
answer = operations[operation_symbol](num1, num2)
```

The dictionary retrieves the corresponding function, passes both numbers to it, and stores the returned result in `answer`.

### 6. Continuing the Calculation

After displaying the result, the calculator asks the user whether they want to continue.

- If the user enters `y`, the previous result becomes the first number for the next calculation.
- Otherwise, the current calculator function stops its loop and starts a new calculator using recursion.

## Example Output

```text
What is the first number?: 10

+
-
*
/
Pick an operation: +
What is the next number?: 5

10.0 + 5.0 = 15.0

Type 'y' to continue calculating with 15.0,
or type 'n' to start a new calculation: y

+
-
*
/
Pick an operation: *
What is the next number?: 2

15.0 * 2.0 = 30.0
```

## Python Concepts Used

| Concept | How It Is Used |
|---|---|
| Functions | Separate functions for mathematical operations |
| Parameters | Passing two numbers to each operation |
| Return Statement | Returning calculation results |
| Dictionaries | Mapping operation symbols to functions |
| Functions as Values | Storing and accessing functions through a dictionary |
| While Loop | Repeating calculations |
| For Loop | Displaying available operation symbols |
| If-Else Conditions | Deciding whether to continue or restart |
| User Input | Taking numbers and operation choices |
| Type Conversion | Converting input into floating-point numbers |
| Recursion | Calling the calculator function again to start a new calculation |
| Modules | Importing the logo from `art.py` |

## Project Structure

```text
Day-10-Calculator/
│
├── main.py       # Main calculator program
├── art.py        # Calculator logo
└── README.md     # Project documentation
```

## How to Run the Project

**Prerequisites:**
- Python 3 installed on your system.
- A code editor such as VS Code or PyCharm.

**Steps:**

1. Clone the repository:

```bash
git clone YOUR_REPOSITORY_URL
```

2. Navigate to the project folder:

```bash
cd Day-10-Calculator
```

3. Run the Python program:

```bash
python main.py
```

## What I Learned

While building this calculator, I learned how to:

- Organize a program using separate functions.
- Store functions as dictionary values.
- Access and call functions dynamically using dictionary keys.
- Use loops to repeat calculations.
- Use recursion to restart a program.
- Reuse the previous calculation result in the next operation.
- Organize code across multiple Python files.

## Learning Journey

**100 Days of Python – Day 10**

This project helped me understand how functions and dictionaries can work together to build a simple interactive application.