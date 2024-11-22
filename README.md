def calculator():
    print("Welcome to the Calculator!")
    print("Select an operation:")
    print("1. Addition (+)")
    print("2. Subtraction (-)")
    print("3. Multiplication (*)")
    print("4. Division (/)")

    while True:
        # Take input from the user
        choice = input("Enter the number corresponding to the operation (1/2/3/4): ")

        # Check if the input is valid
        if choice in ['1', '2', '3', '4']:
            try:
                # Take two numbers as input
                num1 = float(input("Enter the first number: "))
                num2 = float(input("Enter the second number: "))

                # Perform the chosen operation
                if choice == '1':
                    print(f"The result is: {num1 + num2}")
                elif choice == '2':
                    print(f"The result is: {num1 - num2}")
                elif choice == '3':
                    print(f"The result is: {num1 * num2}")
                elif choice == '4':
                    if num2 != 0:
                        print(f"The result is: {num1 / num2}")
                    else:
                        print("Error: Division by zero is not allowed.")
            except ValueError:
                print("Invalid input. Please enter numeric values.")
        else:
            print("Invalid choice. Please select a valid operation.")

        # Ask if the user wants to perform another calculation
        again = input("Do you want to perform another calculation? (yes/no): ").strip().lower()
        if again != 'yes':
            print("Goodbye!")
            break

