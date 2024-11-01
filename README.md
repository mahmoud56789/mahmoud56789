import math

def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y != 0:
        return x / y
    else:
        return "Error! Division by zero."

def square_root(x):
    return math.sqrt(x)

def power(x, y):
    return math.pow(x, y)

def logarithm(x, base=10):
    return math.log(x, base)

def scientific_calculator():
    print("Select operation:")
    print("1. Add")
    print("2. Subtract")
    print("3. Multiply")
    print("4. Divide")
    print("5. Square Root")
    print("6. Power")
    print("7. Logarithm")

    while True:
        choice = input("Enter choice(1/2/3/4/5/6/7): ")

        if choice in ['1', '2', '3', '4']:
            num1 = float(input("Enter first number: "))
            num2 = float(input("Enter second number: "))

            if choice == '1':
                print(f"{num1} + {num2} = {add(num1, num2)}")
            elif choice == '2':
                print(f"{num1} - {num2} = {subtract(num1, num2)}")
            elif choice == '3':
                print(f"{num1} * {num2} = {multiply(num1, num2)}")
            elif choice == '4':
                print(f"{num1} / {num2} = {divide(num1, num2)}")
        elif choice == '5':
            num = float(input("Enter number: "))
            print(f"Square root of {num} = {square_root(num)}")
        elif choice == '6':
            base = float(input("Enter base: "))
            exp = float(input("Enter exponent: "))
            print(f"{base} ^ {exp} = {power(base, exp)}")
        elif choice == '7':
            num = float(input("Enter number: "))
            base = input("Enter base (default is 10): ")
            if base == "":
                base = 10
            else:
                base = float(base)
            print(f"log_{base}({num}) = {logarithm(num, base)}")
        else:
            print("Invalid Input")
        next_calculation = input("Do you want to make another calculation? (yes/no): ")
        if next_calculation.lower() != 'yes':
            break

if __name__ == "__main__":
    scientific_calculator()
