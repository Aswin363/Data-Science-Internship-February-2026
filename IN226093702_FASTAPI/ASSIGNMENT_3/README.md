
# FastAPI Product Management API

This project is a Product Management API developed using FastAPI.
The API provides basic CRUD operations for managing products along with additional features such as product audit and bulk discount functionality.

---

Project Overview

The application manages a list of products and provides endpoints to perform the following operations:

Create new products
Retrieve product details
Update product information
Delete products
Generate product audit reports
Apply bulk discounts to product categories

The API is tested and documented using the FastAPI interactive documentation interface.

---

Technologies Used

Python
FastAPI
Pydantic
Uvicorn

---

API Endpoints

1. Get All Products

Endpoint
GET /products

Description
Returns the list of all products along with the total count.

---

2. Add Product

Endpoint
POST /products

Description
Adds a new product to the product list. If a product with the same name already exists, the API returns a 400 error.

Example Request

{
"name": "Laptop Stand",
"price": 1299,
"category": "Electronics",
"in_stock": true
}

---

3. Get Product by ID

Endpoint
GET /products/{product_id}

Description
Returns the details of a specific product based on its ID.

---

4. Update Product

Endpoint
PUT /products/{product_id}

Description
Updates the product price or stock status.

Example

/products/3?price=649&in_stock=true

---

5. Delete Product

Endpoint
DELETE /products/{product_id}

Description
Removes the product from the system and returns a confirmation message.

---

Product Audit

Endpoint
GET /products/audit

Description
This endpoint provides a summary report of the product inventory including:

Total number of products
Number of products currently in stock
Names of products that are out of stock
Total stock value
Most expensive product

Example Response

{
"total_products": 5,
"in_stock_count": 5,
"out_of_stock_names": [],
"total_stock_value": 25950,
"most_expensive": {
"name": "Laptop Stand",
"price": 1299
}
}

---

Bonus Feature

Bulk Discount

Endpoint
PUT /products/discount

Description
Applies a percentage discount to all products within a specific category.

Example Request

/products/discount?category=Electronics&discount_percent=10

Example Response

{
"message": "10% discount applied to Electronics",
"updated_count": 4
}

---

How to Run the Project

Step 1: Install dependencies

pip install fastapi uvicorn

Step 2: Run the server

uvicorn main:app --reload

Step 3: Open API documentation

http://127.0.0.1:8000/docs

---

Project Files

main.py – Contains all FastAPI endpoints and application logic
README.md – Project documentation
Screenshots – Contains API execution screenshots for assignment submission

---

Author

FastAPI Internship Assignment Submission
