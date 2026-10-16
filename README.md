# FinTech Backend API

Production-ready FastAPI initial boilerplate with standard modular architecture, SQLite/PostgreSQL database support via SQLAlchemy, Pydantic settings management, OAuth2 JWT security helpers, and integration testing with Pytest.

---

## 📁 Project Structure

```text
FinTech_Backend/
├── app/
│   ├── main.py                  # FastAPI app entrypoint & middleware
│   ├── core/
│   │   ├── config.py            # Pydantic Settings (.env auto-load)
│   │   ├── database.py          # SQLAlchemy engine & session dependency
│   │   └── security.py          # Password hashing & JWT helpers
│   ├── api/
│   │   └── v1/
│   │       ├── api.py           # V1 Router bundle
│   │       └── endpoints/
│   │           ├── health.py    # Health check endpoint
│   │           ├── auth.py      # Registration & Login endpoints
│   │           └── users.py     # User management endpoints
│   ├── models/                  # SQLAlchemy ORM Models
│   │   └── user.py
│   ├── schemas/                 # Pydantic validation schemas
│   │   └── user.py
│   └── crud/                    # Database CRUD operations
│       └── crud_user.py
├── tests/                       # Pytest test suite
│   ├── conftest.py
│   └── test_health.py
├── .env.example                 # Environment variables template
├── .gitignore
├── README.md
└── requirements.txt
```

---

## 🚀 Quick Start Guide

### 1. Setup Virtual Environment

On Windows PowerShell:
```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

### 2. Install Dependencies

```powershell
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
```

### 3. Run Development Server

```powershell
.\.venv\Scripts\python.exe -m uvicorn app.main:app --reload
```

Server will run at `http://127.0.0.1:8000`

---

## 📚 API Documentation

Once the server is running, explore interactive API documentation at:
- **Swagger UI**: [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)
- **ReDoc**: [http://127.0.0.1:8000/redoc](http://127.0.0.1:8000/redoc)

---

## 🧪 Running Tests

Execute the automated test suite with pytest:

```powershell
.\.venv\Scripts\python.exe -m pytest
```
