# -Basic-Python-Calculator
creating a basic Python command-line calculator.  Basic mathematical operations like addition, subtraction, multiplication, and division should be able to be carried out by the calculator. It ought to request input from the user, compute the outcome, and show it.







def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        return "Error! Division by zero."
    else:
        return x / y

def calculator():
    while True:
        print("\nChoose operation:")
        print("1. Addition")
        print("2. Subtraction")
        print("3. Multiplication")
        print("4. Division")
        print("5. Exit")

        choice = input("Enter choice (1/2/3/4/5): ")

        if choice == '5':
            print("Exiting the calculator. Goodbye!")
            break

        if choice in ('1', '2', '3', '4'):
            num1 = input("Enter first number: ")
            num2 = input("Enter second number: ")

            try:
                num1 = float(num1)
                num2 = float(num2)
            except ValueError:
                print("Invalid input! Please enter numeric values.")
                continue

            if choice == '1':
                print("Result:", add(num1, num2))
            elif choice == '2':
                print("Result:", subtract(num1, num2))
            elif choice == '3':
                print("Result:", multiply(num1, num2))
            elif choice == '4':
                print("Result:", divide(num1, num2))
        else:
            print("Invalid input! Please enter a valid choice (1/2/3/4).")

if __name__ == "__main__":
    calculator()