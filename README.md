# Assignment_3_-Armstrong_Numbers-
📘 Extended Description: Armstrong Number Checker
This notebook contains a Python script that checks whether a user-inputted number is an Armstrong number. An Armstrong number (also known as a narcissistic number) is a number that is equal to the sum of its own digits each raised to the power of the number of digits. For example, 9474 is an Armstrong number because:

9^4 + 4^4 + 7^4 + 4^4 = 9474

🔧 Code Improvements and Rationale
The original version of the code was functional but lacked clarity and modern Python practices. The updated version introduces the following enhancements:

✅ 1. Descriptive Variable Naming
Replaced generic names like a, b, c with meaningful identifiers: number, digit, total, power, num.

This improves readability and makes the code self-documenting.

🧠 2. Simplified Logic
Used number.isdigit() instead of isdigit() == True for cleaner syntax.

Replaced manual digit summation loop with a generator expression inside sum():

python
total = sum(int(digit) ** power for digit in number)
🧵 3. Modern String Formatting
Switched from .format() to f-strings for more concise and readable output:

python
print(f"{num} is an Armstrong number.")
🧱 4. Robust Input Validation
Checks for:

Negative numbers using startswith("-")

Decimal or comma input (locale-aware)

Non-numeric characters

Ensures only valid positive integers are processed.

🌍 5. Internationalization Awareness
Recognizes both "." and "," as decimal separators to accommodate different regional formats.

📦 6. Notebook Compatibility
The code is embedded in a valid Jupyter Notebook (nbformat 4.4) with proper metadata, ensuring compatibility with GitHub rendering and interactive environments.
