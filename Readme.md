# Loopr Python Assignment

This repository contains the backend code for the Looper application. It provides a set of API endpoints for user registration, login, product management, coupon management, and shopping cart functionality.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

To run this project, you need to have the following software installed on your system:

- Python (version 3.8 or above)
- pip (Python package installer)

### Installation

Follow these steps to set up the project:

1. Clone the repository to your local machine:

   ```
   git clone https://github.com/arvi18/loopr-python.git
   ```

2. Change to the project directory:

   ```
   cd loopr-python
   ```

3. Install the required dependencies:

   ```
   pip install -r requirements.txt
   ```

4. Start the server:

   ```
   python main.py
   ```

   The server will run on `http://localhost:8000`.

## API Endpoints

### Register

- **Endpoint:** `/register`
- **Method:** POST
- **Description:** Register a new user.
- **Request Body:**
  ```json
  {
    "username": "username",
    "password": "password"
  }
  ```

### Login

- **Endpoint:** `/login`
- **Method:** POST
- **Description:** Authenticate a user.
- **Request Body:**
  ```json
  {
    "username": "username",
    "password": "password"
  }
  ```

### Add Product

- **Endpoint:** `/add_product`
- **Method:** POST
- **Description:** Add a new product.
- **Request Body:**
  ```json
  {
    "image": "URL",
    "name": "",
    "price": 0,
    "quantity": 0
  }
  ```

### List all Products

- **Endpoint:** `/get_products`
- **Method:** GET
- **Description:** Get a list of all products.

### Add Coupon

- **Endpoint:** `/add_coupon`
- **Method:** POST
- **Description:** Add a new coupon.
- **Request Body:**
  ```json
  {
    "code": "",
    "discount": 0,
    "discount_type": "percentage", // or "amount"
    "description": ""
  }
  ```

### List all Coupons

- **Endpoint:** `/get_coupons`
- **Method:** GET
- **Description:** Get a list of all coupons.

### Add a Product to Cart

- **Endpoint:** `/add_to_cart?productId=1`
- **Method:** POST
- **Description:** Add a product to the shopping cart.

### Update Product Quantity in the Cart

- **Endpoint:** `/update_cart?productId=1&quantity=50`
- **Method:** PUT
- **Description:** Update the quantity of a product in the shopping cart.

### Delete Product from Cart

- **Endpoint:** `/delete_from_cart?productId=1`
- **Method:** DELETE
- **Description:** Remove a product from the shopping cart.

### Get Cart

- **Endpoint:** `/get_cart`
- **Method:** GET
- **Description:** Retrieve the shopping cart contents, including the list of products and total price. To apply a coupon code for a discount, include the `coupon` query parameter in the URL, e.g., `/get_cart?coupon=FREE`. The response will include the discounted price if a valid coupon code is provided.

## Links

```
- Deployed app: [Replit](https://replit.com/@arviiii/loopr-python)
- Postman Documentation: [Postman](https://documenter.getpostman.com/view/17461415/2s93sW9vko)

```
