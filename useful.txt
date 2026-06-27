def calculator():
    print("Basic Calculator")
    print("Enter two numbers and choose an operation.")

    try:
        num1 = float(input("First number: "))
        num2 = float(input("Second number: "))
    except ValueError:
        print("Invalid input. Please enter numeric values.")
        return

    print("\nOperations:")
    print("1. Add")
    print("2. Subtract")
    print("3. Multiply")
    print("4. Divide")

    operation = input("Choose operation (1/2/3/4): ")

    if operation == "1":
        result = num1 + num2
        op_name = "Addition"
    elif operation == "2":
        result = num1 - num2
        op_name = "Subtraction"
    elif operation == "3":
        result = num1 * num2
        op_name = "Multiplication"
    elif operation == "4":
        if num2 == 0:
            print("Error: Cannot divide by zero.")
            return
        result = num1 / num2
        op_name = "Division"
    else:
        print("Invalid operation selection.")
        return

    print(f"\n{op_name} result: {result}")


if __name__ == "__main__":
    calculator()
