# Basic-Calculator
Basic Calculator Description 
# Task 1: Basic Calculator
# Name: Manikandan 
# Domain: Python Developer - Alfido Tech Internship
# Description: A simple calculator that performs addition, subtraction, multiplication, and division.

# Function definitions
def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        return "Error! Division by zero is not possible."
    else:
        return x / y

# Program start
print("======== BASIC CALCULATOR ========")
print("Operations:")
print("1. Addition (+)")
print("2. Subtraction (-)")
print("3. Multiplication (*)")
print("4. Division (/)")
print("Type 'q' to quit.")

while True:
    choice = input("\nEnter your choice (1/2/3/4 or q): ")

    if choice.lower() == 'q':
        print("Exiting the calculator. Thank you!")
        break

    # Get user input
    try:
        num1 = float(input("Enter first number: "))
        num2 = float(input("Enter second number: "))
    except ValueError:
        print("❌ Invalid input! Please enter numbers only.")
        continue

    # Perform the selected operation
    if choice == '1':
        print(f"Result: {num1} + {num2} = {add(num1, num2)}")
    elif choice == '2':
        print(f"Result: {num1} - {num2} = {subtract(num1, num2)}")
    elif choice == '3':
        print(f"Result: {num1} * {num2} = {multiply(num1, num2)}")
    elif choice == '4':
        print(f"Result: {num1} / {num2} = {divide(num1, num2)}")
    else:
        print("⚠️ Invalid choice! Please select 1, 2, 3, 4, or 'q' to quit.")
