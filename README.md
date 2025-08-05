# ecommerce-api

A portfolio project for an E-commerce backend API using **FastAPI**, following **Clean Architecture** principles.

This project supports:

- User management
- Product listing
- Order handling
- JWT-based authentication

---

## 🔧 Technologies Used

- **FastAPI** – for building RESTful APIs
- **SQLite** – lightweight local database
- **Pydantic** – for data validation and schemas
- **PyJWT** – for handling authentication
- **Pytest** – for unit testing
- **Postman** – for manual API testing

---

## 📁 Project Structure


- `app/auth/` – JWT-based auth system  
- `app/routes/` – API endpoints for users, products, orders  
- `app/schemas/` – Pydantic data models  
- `app/services/` – business logic  
- `tests/` – test files using Pytest

---

## 🔐 Authentication

The API uses **JWT tokens** to protect routes.  
There are two user roles:

- **User**
- **Admin**

Access to certain endpoints requires a valid JWT token sent as a `Bearer` token in headers.

---

## 🚀 Endpoints Overview

| Endpoint       | Description              | Auth Required |
|----------------|--------------------------|---------------|
| `/users/`      | Get all users            | ✅ Yes         |
| `/products/`   | Get all products         | ❌ No          |
| `/orders/`     | Get all orders           | ❌ No          |

---

## ✅ Running the Project

1. Install dependencies:

    pip install fastapi uvicorn python-jose[cryptography] pytest

2. Run the app:

    uvicorn main:app --reload

3. Run tests:

    pytest

---

## 📬 Postman Collection

A ready-to-use Postman collection is provided, including sample tokens to test protected routes.

---

## 📄 License

This project is open-source and free to use under the MIT license.
