# Simple-Calculator
def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y==0:
        return "invalid operation"
    else:
        return x / y

print("Select operation.")
print("add for addition")
print("sub for subtraction")
print("mul for multiplication")
print("div for division")

while True:
    choice = input("Enter choice (add/sub/mul/div): ")

    if choice in ('add', 'sub', 'mul', 'div'):
        num1 = float(input("Enter first number: "))
        num2 = float(input("Enter second number: "))

        if choice == 'add':
            print(num1, "+", num2, "=", add(num1, num2))
        elif choice == 'sub':
            print(num1, "-", num2, "=", subtract(num1, num2))
        elif choice == 'mul':
            print(num1, "*", num2, "=", multiply(num1, num2))
        elif choice == 'div':
            print(num1, "/", num2, "=", divide(num1, num2))

        next_calculation = input("Next calculation? (yes/no): ")
        if next_calculation.lower() != "yes":
            break
    else:
        print("Invalid Operation") 
