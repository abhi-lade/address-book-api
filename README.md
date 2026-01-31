# Address Book API

A RESTful Address Book API built using *FastAPI* and *SQLite*.  
This project allows users to manage address records and search nearby addresses using geographic coordinates.

---

## 🚀 Features

- Create a new address
- Update an existing address
- Delete an address
- Fetch all addresses
- Find addresses within a given distance (in KM)
- Input validation for latitude & longitude
- Interactive API documentation using Swagger UI

---

## 🛠 Tech Stack

- *Python 3*
- *FastAPI*
- *SQLAlchemy (ORM)*
- *SQLite*
- *Pydantic*
- *Uvicorn*

---

## 📁 Project Structure
```
Aaddress_book_api/
│
├── main.py
├── database.py
├── models.py
├── schemas.py
├── crud.py
├── utils.py
├── requirements.txt
└── README.md
```

---

📄 File-by-File Explanation (Interview Friendly)

main.py

Entry point of the application

Initializes FastAPI

Defines all API routes

Handles dependency injection for database sessions

Creates database tables on startup


👉 This file controls request flow.


---

database.py

Configures SQLite database

Creates SQLAlchemy engine

Manages database sessions

Defines Base for ORM models


👉 Central place for DB connection management.


---

models.py

Defines SQLAlchemy ORM models

Represents database tables as Python classes

Example: Address table with id, name, latitude, longitude


👉 Handles database structure.


---

schemas.py

Defines Pydantic schemas

Used for:

Request validation

Response serialization


Enforces latitude & longitude constraints


👉 Ensures data validation and API safety.


---

crud.py

Contains all business logic

Handles Create, Read, Update, Delete operations

Keeps main.py clean and readable


👉 Follows separation of concerns.


---

utils.py

Stores helper functions

Implements Haversine formula

Calculates distance between two coordinates


👉 Reusable utility logic.


---

requirements.txt

Lists all project dependencies

Used to recreate environment easily


👉 Supports reproducibility.