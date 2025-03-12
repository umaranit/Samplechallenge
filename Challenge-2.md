

# Coding Challenge: Simple E-commerce Product Search

## Challenge Overview

Develop a simple e-commerce product search application. This challenge involves reading product data from a JSON file, implementing a search function, and displaying the search results.

## Tasks

### Task 1: Product Data Structure

-   Define a `Product` class with the following attributes:
    -   `product_id` (string): Unique identifier for the product.
    -   `name` (string): Name of the product.
    -   `description` (string): Detailed description of the product.
    -   `price` (float): Price of the product.
    -   `category` (string): Category the product belongs to (e.g., "Electronics", "Books", "Clothing").
    -   `image_url` (string, optional): URL to an image of the product.

### Task 2: Read Product Data from JSON File

-   Create a JSON file named `products.json` containing an array of product objects.
-   Implement a function `load_products(filename)` to read the product data from the JSON file and return a list of `Product` objects.
    -   Handle potential `FileNotFoundError` if the file does not exist.
    -   Handle potential `JSONDecodeError` if the file is not a valid JSON.

### Task 3: Implement Search Functionality

-   Implement a function `search_products(products, query)` that searches for products based on a given query string.
    -   The search should be case-insensitive.
    -   The search should check if the query string is present in the `name` or `description` of the product.
    -   The function should return a list of `Product` objects that match the search query.

### Task 4: Display Search Results

-   Implement a function `display_products(products)` that displays the product information in a user-friendly format.
    -   Display the `name`, `price`, and a short snippet of the `description` for each product.
    -   If no products are found, display a message indicating that no results were found.

### Task 5: User Interaction

-   Implement a main function that:
    -   Loads the product data from `products.json`.
    -   Prompts the user to enter a search query.
    -   Calls the `search_products` function to find matching products.
    -   Calls the `display_products` function to display the search results.
    -   Allows the user to perform multiple searches until they choose to exit.

## Example Interaction

```
Welcome to the Product Search Application!

Enter your search query (or type 'exit' to quit): laptop
Search results:
--------------------
Name: Laptop Pro 15
Price: 1299.99
Description: Powerful laptop with a 15-inch display...

Name: UltraBook
Price: 999.00
Description: Lightweight and portable ultrabook...
--------------------

Enter your search query (or type 'exit' to quit): book
Search results:
--------------------
Name: The Hitchhiker's Guide to the Galaxy
Price: 12.50
Description: A humorous science fiction book...
--------------------

Enter your search query (or type 'exit' to quit): exit
Thank you for using the Product Search Application!
```

## Example JSON File (`products.json`)

```json
[
  {
    "product_id": "P001",
    "name": "Laptop Pro 15",
    "description": "Powerful laptop with a 15-inch display, 16GB RAM, and 512GB SSD.",
    "price": 1299.99,
    "category": "Electronics",
    "image_url": "https://example.com/laptop.jpg"
  },
  {
    "product_id": "P002",
    "name": "Wireless Mouse",
    "description": "Ergonomic wireless mouse with high precision.",
    "price": 25.00,
    "category": "Electronics"
  },
  {
    "product_id": "B001",
    "name": "The Hitchhiker's Guide to the Galaxy",
    "description": "A humorous science fiction book by Douglas Adams.",
    "price": 12.50,
    "category": "Books",
    "image_url": "https://example.com/hitchhikers.jpg"
  },
  {
    "product_id": "P003",
    "name": "UltraBook",
    "description": "Lightweight and portable ultrabook with a long battery life.",
    "price": 999.00,
    "category": "Electronics"
  }
]
```

## Detailed Requirements

-   **Error Handling: ** Implement error handling for file operations and invalid data.
-   **Case-Insensitive Search: ** The search should be case-insensitive.
-   **Partial Match: ** The search should return products that contain the query in their name or description (not an exact match).
-   **User Interface: ** The user interface should be clear and easy to use.
-   **Code Quality: ** Ensure your code is well-documented and follows best practices.
-   **Modularity: ** Break down the problem into smaller, manageable functions.
-   **Comments: ** Add comments to explain the purpose of each function and complex logic.
