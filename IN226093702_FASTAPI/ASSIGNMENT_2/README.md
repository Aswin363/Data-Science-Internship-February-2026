# FastAPI Internship – Assignment 2

## Overview

This project was completed as part of the **February 2026 FastAPI Internship Program**.
The objective of this assignment was to implement and test multiple **FastAPI endpoints**, apply **query parameters**, perform **Pydantic validation**, and implement **business logic for product management and order processing**.

All endpoints were tested using **Swagger UI (`/docs`)**, and screenshots were captured as proof of execution.

---

# Technologies Used

* Python
* FastAPI
* Uvicorn
* Pydantic
* Swagger UI

---

# How to Run the Project

## 1. Create Virtual Environment

```bash
python -m venv venv
```

## 2. Activate Virtual Environment

Windows:

```bash
venv\Scripts\activate
```

## 3. Install Required Libraries

```bash
pip install fastapi uvicorn
```

## 4. Run the Server

```bash
uvicorn main:app --reload
```

## 5. Open Swagger UI

Open the browser and go to:

```
http://127.0.0.1:8000/docs
```

All endpoints can be tested from Swagger UI.

---

# Implemented API Endpoints

## Q1 – Filter Products by Minimum Price

Endpoint:

```
GET /products/filter
```

Features:

* Filter products using `min_price`
* Works together with other filters like `max_price`

Example:

```
/products/filter?min_price=400
```

---

## Q2 – Get Product Price

Endpoint:

```
GET /products/{product_id}/price
```

Returns only:

* Product name
* Product price

If the product ID does not exist:

```
{"error": "Product not found"}
```

---

## Q3 – Customer Feedback API

Endpoint:

```
POST /feedback
```

Uses **Pydantic validation**.

Fields:

* customer_name (min 2 characters)
* product_id (>0)
* rating (1–5)
* comment (optional)

Example response:

```
{
 "message": "Feedback submitted successfully"
}
```

---

## Q4 – Product Summary Dashboard

Endpoint:

```
GET /products/summary
```

Returns:

* total_products
* in_stock_count
* out_of_stock_count
* most_expensive product
* cheapest product
* list of categories

---

## Q5 – Bulk Order Processing

Endpoint:

```
POST /orders/bulk
```

Features:

* Accepts multiple items
* Validates stock availability
* Calculates subtotal and grand total
* Returns confirmed and failed orders separately

Example output:

```
{
 "company": "TechCorp",
 "confirmed": [...],
 "failed": [...],
 "grand_total": 1497
}
```

---

# Bonus Feature – Order Status Tracker

## Place Order

```
POST /orders
```

Orders are created with status **pending**.

## Get Order by ID

```
GET /orders/{order_id}
```

Returns order details.

## Confirm Order

```
PATCH /orders/{order_id}/confirm
```

Updates order status from **pending → confirmed**.

---

# Project Folder Structure

```
FASTAPI_ASSIGNMENT
│
└── ASSIGNMENT_2
    │
    ├── main.py
    ├── README.md
    │
    ├── Q1_MinPrice_Output.png
    ├── Q1_Combined_Filter_Output.png
    │
    ├── Q2_ProductPrice_Output.png
    ├── Q2_ProductNotFound_Output.png
    │
    ├── Q3_Feedback_Error_Output.png
    ├── Q3_Feedback_Success_Output.png
    │
    ├── Q4_ProductSummary_Output.png
    │
    ├── Q5_BulkOrder_Output.png
    │
    ├── Bonus_OrderPlaced_Pending_Output.png
    ├── Bonus_OrderConfirm_Output.png
    │
    └── Swagger_AllEndpoints_Test_Output.png
```

---

# Testing

All endpoints were tested successfully in **Swagger UI**.
Screenshots of each task output were captured as required by the assignment submission guidelines.

---

# Author

**FastAPI Internship – Assignment 2**
February 2026 Internship Program
Innomatics Research Labs

