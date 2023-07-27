def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        return "Cannot divide by zero"
    return x / y

def calculator():
    print("Basic Calculator App")
    print("Available operations: +, -, *, /")
    while True:
        operator = input("Enter operator (+, -, *, /) or 'exit' to quit: ")

        if operator.lower() == 'exit':
            break

        if operator not in ('+', '-', '*', '/'):
            print("Invalid operator. Please try again.")
            continue

        num1 = float(input("Enter the first number: "))
        num2 = float(input("Enter the second number: "))

        if operator == '+':
            result = add(num1, num2)
        elif operator == '-':
            result = subtract(num1, num2)
        elif operator == '*':
            result = multiply(num1, num2)
        else:
            result = divide(num1, num2)

        print(f"Result: {result}\n")

if __name__ == "__main__":
    calculator()