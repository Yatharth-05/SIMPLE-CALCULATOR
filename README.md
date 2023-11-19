# SIMPLE-CALCULATOR
Prompt the user to input 2 numbers and an operation choice.

def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        return "Error! Division by zero is not allowed."
    return x / y

print("Simple Calculator")
print("Operations:")
print("1. Addition")
print("2. Subtraction")
print("3. Multiplication")
print("4. Division")

# Input from the user
choice = input("Enter operation (A/S/M/D): ")

num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))

result = 0

if choice == 'A':
    result = add(num1, num2)
    operation = '+'
elif choice == 'S':
    result = subtract(num1, num2)
    operation = '-'
elif choice == 'M':
    result = multiply(num1, num2)
    operation = '*'
elif choice == 'D':
    result = divide(num1, num2)
    operation = '/'

if isinstance(result, str):
    print(result)
else:
    print(f"{num1} {operation} {num2} = {result}")
