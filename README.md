# 🧮 Simple Calculator

A Python program implementing a basic calculator with the ability to perform addition, subtraction, multiplication, division, and exponentiation. The program prompts users to input two numbers and choose an operation. It then displays the result and allows users to continue calculations or start a new one.

## Operations

- Addition (+)
- Subtraction (-)
- Multiplication (*)
- Division (/)
- Exponentiation (**)

## Usage

1. Enter the first number.
2. Choose an operation from the available options.
3. Enter the second number.
4. View the result.
5. Decide to continue with the result or start a new calculation.

## Example

```python
from art import logo

# 
from art import logo


def add(n1, n2):
    return n1 + n2


def subtract(n1, n2):
    return n1 - n2


def multiply(n1, n2):
    return n1 * n2


def divide(n1, n2):
    return n1 / n2


def power(n1, n2):
    return n1**n2


operations = {
    "+": add,
    "-": subtract,
    "*": multiply,
    "/": divide,
    "**": power,
}


def calculator():
    print(logo)

    num1 = float(input("What's the first number?: "))
    for symbol in operations:
        print(symbol)
    should_continue = True

    while should_continue:
        operation_symbol = input("Pick an operation: ")
        num2 = float(input("What's the next number?: "))
        calculation_function = operations[operation_symbol]
        answer = calculation_function(num1, num2)

        print(f"{num1} {operation_symbol} {num2} = {answer}")

        if input(
            f"Type 'y' to continue calculating with {answer}, or type 'n' to start a new calculation: "
            == "y"
        ):
            num1 = answer
        else:
            should_continue = False
            calculator()


calculator()


calculator()
