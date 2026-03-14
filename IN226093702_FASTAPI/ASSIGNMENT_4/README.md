# 🛒 FastAPI Shopping Cart System

A RESTful **Shopping Cart API** built using **FastAPI**.
This project simulates a basic e-commerce cart workflow where users can add products, update quantities, remove items, and checkout orders.

The system was implemented as part of a **Python Backend Development Internship Assignment**.

---

# Features

* Add products to cart
* Update quantity of existing cart items
* View cart with subtotal and grand total
* Remove items from cart
* Checkout cart and create orders
* View order history
* Error handling for invalid products and out-of-stock items
* Proper handling of checkout with empty cart

---

# 🛠️ Tech Stack

* **Python**
* **FastAPI**
* **Uvicorn**
* **Swagger UI (API Testing)**

---

# 📂 Project Structure

```
project-folder
│
├── main.py
├── README.md
└── screenshots
    ├── Q1_add_mouse.png
    ├── Q1_add_notebook.png
    ├── Q2_cart_total.png
    ├── Q3_invalid_product.png
    ├── Q3_out_of_stock.png
    ├── Q4_cart_updated.png
    ├── Q5_remove_notebook.png
    ├── Q5_checkout.png
    ├── Q6_customer1_checkout.png
    ├── Q6_customer2_checkout.png
    ├── Q6_total_orders.png
    ├── BONUS_cart_empty.png
    └── manual_calculation.png
```

---

# ⚙️ Installation & Run

### 1️⃣ Install dependencies

```bash
pip install fastapi uvicorn
```

### 2️⃣ Run the server

```bash
uvicorn main:app --reload
```

### 3️⃣ Open API Docs

```
http://127.0.0.1:8000/docs
```

---

# 📡 API Endpoints

| Method | Endpoint             | Description           |
| ------ | -------------------- | --------------------- |
| POST   | `/cart/add`          | Add product to cart   |
| GET    | `/cart`              | View cart             |
| DELETE | `/cart/{product_id}` | Remove item from cart |
| POST   | `/cart/checkout`     | Checkout cart         |
| GET    | `/orders`            | View all orders       |

---

# 🧾 Assignment Tasks Implementation

## Q1 – Add Products to Cart

Added products:

* Wireless Mouse (ID:1)
* Notebook (ID:2)

Subtotal calculation:

```
Wireless Mouse → 499 × 2 = 998
Notebook → 99 × 1 = 99
```

---

## Q2 – View Cart

Cart response:

```
item_count = 2
grand_total = 1097
```

Calculation:

```
998 + 99 = 1097
```

---

## Q3 – Error Handling

Invalid product:

```
product_id = 99
Response → 404 Product not found
```

Out of stock product:

```
product_id = 3
Response → 400 USB Hub is out of stock
```

---

## Q4 – Update Existing Item

Adding Wireless Mouse again updates quantity.

```
499 × 3 = 1497
```

Updated cart total:

```
1497 + 99 = 1596
```

---

## Q5 – Remove Item and Checkout

Notebook removed:

```
DELETE /cart/2
```

Remaining cart:

```
Wireless Mouse → 499 × 3 = 1497
```

Checkout created order:

```
grand_total = 1497
```

Cart becomes empty after checkout.

---

## Q6 – Full Cart Flow (2 Customers)

### Customer 1

Products:

```
Wireless Mouse → 499
Pen Set → 49 × 3 = 147
```

Total:

```
499 + 147 = 646
```

Orders created:

* Wireless Mouse
* Pen Set

---

### Customer 2

Products:

```
Wireless Mouse → 499
```

Order created:

* Wireless Mouse

Final orders list:

```
Total Orders = 3
```

---

# ⭐ Bonus Task

Checkout with empty cart:

```
POST /cart/checkout
```

Response:

```
400 Bad Request
Cart is empty — add items first
```

No order is created.

---

# 🧮 Manual Calculation Verification

All subtotals and grand totals were verified manually.

Example:

```
Wireless Mouse → 499 × 2 = 998
Notebook → 99 × 1 = 99

Grand Total = 998 + 99 = 1097
```

The API response matches the manual calculations.

---

# 📷 Screenshots

All API responses and flows are captured in the **screenshots folder** for verification.

---

# 👨‍💻 Author

**Aswin Sahu**

Python Backend Development Intern
MCA Student

---

# ✅ Assignment Completion Checklist

✔ Add products to cart
✔ View cart totals
✔ Error handling implemented
✔ Cart update logic implemented
✔ Remove item + checkout flow
✔ Multi-customer cart flow
✔ Manual verification of totals
✔ Bonus task completed

---

# 📌 Conclusion

This project demonstrates the implementation of a **complete shopping cart workflow using FastAPI**, including CRUD operations, validation, error handling, and order processing.

The API was successfully tested using **Swagger UI**, and all calculations were verified manually.
