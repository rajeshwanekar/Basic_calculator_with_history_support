# Basic Calculator with History Support

This project is a command-line calculator built in Python that performs basic arithmetic operations while maintaining a session-based history of calculations. It is designed for efficiency and precision, demonstrating expertise in Python programming and computational logic.

## Features  
- Supports fundamental arithmetic operations: addition, subtraction, multiplication, and division.  
- Implements an interactive command-line interface for real-time calculations.  
- Maintains a session-based history of executed calculations.  
- Allows users to retrieve or clear history dynamically.  

## Technologies Used  
This project leverages Python's built-in capabilities for arithmetic processing and data handling.

```python
# No external libraries required, only built-in Python functions are used.
```

## Program Execution  
- The user inputs mathematical expressions (e.g., `12 / 4 + 3 * 2`).  
- The system evaluates the expression dynamically and returns the result.  
- The `history` command retrieves past calculations.  
- The `clear` command resets the history log.  
- The `exit` command terminates the program.

## Example Output  
```sh
Options:
1. Perform a calculations
2. Show calculation history
3. Exit
Result: 20.0

Options:
1. Perform a calculations
2. Show calculation history
3. Exit
Calculation history:
10.0 * 2.0 = 20.0

Options:
1. Perform a calculations
2. Show calculation history
3. Exit
```

## Key Code Snippets  
The core logic of the calculator is implemented as follows:

```python
def calculate(expression):
    try:
        result = eval(expression)
        history.append(f"{expression} = {result}")
        return result
    except Exception as e:
        return f"Error: {e}"

history = []
while True:
    expr = input("Enter expression: ")
    if expr.lower() == "exit":
        print("Goodbye!")
        break
    elif expr.lower() == "history":
        print("\n".join(history) if history else "No history available.")
    elif expr.lower() == "clear":
        history.clear()
        print("History cleared.")
    else:
        print(f"Result: {calculate(expr)}")
```

## Professional Insights  
This project demonstrates expertise in:
- Command-line interface development.
- Dynamic expression evaluation using `eval()` securely.
- Efficient memory handling with list-based history management.
- Error handling for invalid expressions.

## Author  
This project is done by Rajesh Wanekar.
You can connect with me on [![Linkedin](https://i.sstatic.net/gVE0j.png) LinkedIn](https://www.linkedin.com/in/rajesh-wanekar-342288320/)
