# Coding Challenge: Advanced Currency Converter

## Challenge Overview
Develop a robust currency converter application. This challenge involves handling user input, performing arithmetic operations, reading exchange rates from a JSON file, and implementing comprehensive error handling.

## Tasks

### Task 1: Input the Amount and Currencies
- Implement a function `get_amount()` to accept user input for the amount of money to convert.
  - The function should validate that the input is a positive number. If not, display an error message and re-prompt the user.
- Implement a function `get_currencies()` to accept user input for the source and target currencies.
  - The function should validate that the currency codes are valid (e.g., USD, EUR, GBP, JPY). If not, display an error message and re-prompt the user.
  - Currency codes should be case-insensitive.

### Task 2: Read Exchange Rates from JSON File
- Create a JSON file named `exchange_rates.json` with exchange rates.
  - The JSON file should contain a nested structure as shown in the example.
- Implement a function `load_exchange_rates(filename)` to read the exchange rates from the JSON file.
  - Handle potential `FileNotFoundError` if the file does not exist.
  - Handle potential `JSONDecodeError` if the file is not a valid JSON.
  - If an error occurs, display an appropriate error message and exit the program gracefully.

### Task 3: Perform the Conversion
- Implement a function `convert_currency(amount, source_currency, target_currency, exchange_rates)` to convert the amount from the source currency to the target currency using the exchange rates from the JSON file.
  - Handle potential `KeyError` if the source or target currency is not found in the exchange rates.
  - If an error occurs, display an appropriate error message and return `None`.
  - Implement cross-rate conversion (e.g., if a direct rate from A to C is not available, convert from A to B and then B to C).

### Task 4: Display the Result
- Implement a function `display_result(amount, source_currency, target_currency, converted_amount)` to display the converted amount.
  - The output should be formatted to two decimal places.
  - Display the result in a clear and user-friendly format.

### Task 5: Error Handling
- Implement comprehensive error handling for all possible scenarios, including:
  - Invalid user input (non-numeric amount, invalid currency codes)
  - File not found (`exchange_rates.json`)
  - Invalid JSON format
  - Missing exchange rates
  - Division by zero (if an exchange rate is zero, which is unlikely but should be handled)
- Display informative error messages to the user.

### Task 6: Logging
- Implement basic logging to record any errors or exceptions that occur during the program execution.
  - Use the `logging` module in Python.
  - Log errors to a file named `currency_converter.log`.

## Example Interaction:

```
Welcome to the Advanced Currency Converter
Enter the amount: abc
Invalid amount. Please enter a positive number.
Enter the amount: -100
Invalid amount. Please enter a positive number.
Enter the amount: 100
Enter the source currency (e.g., USD, EUR, GBP, JPY): usdd
Invalid currency code. Please enter a valid currency code.
Enter the source currency (e.g., USD, EUR, GBP, JPY): USD
Enter the target currency (e.g., USD, EUR, GBP, JPY): EUR
Converted amount: 100 USD = 85.00 EUR
```

## Example JSON File (`exchange_rates.json`):
```json
{
  "USD": {
    "EUR": 0.85,
    "GBP": 0.75,
    "JPY": 110.0,
    "INR": 74.0
  },
  "EUR": {
    "USD": 1.18,
    "GBP": 0.88,
    "JPY": 129.0,
    "INR": 87.0
  },
  "GBP": {
    "USD": 1.33,
    "EUR": 1.14,
    "JPY": 145.0,
    "INR": 99.0
  },
  "JPY": {
    "USD": 0.0091,
    "EUR": 0.0078,
    "GBP": 0.0069,
    "INR": 0.68
  },
  "INR": {
    "USD": 0.0135,
    "EUR": 0.0115,
    "GBP": 0.0101,
    "JPY": 1.47
  }
}
```

## Submission Guidelines:
- Ensure your code is well-documented and follows best practices.
- Use GitHub Copilot to assist in the development process.
- Include comprehensive error handling and logging.
- Write Unit Tests
- Provide clear instructions on how to run the application.