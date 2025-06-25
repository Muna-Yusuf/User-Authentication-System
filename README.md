# 🔐 Auth API

This is a simple Django REST API for user registration, login with JWT, and protected profile access.

## Endpoints:

- `POST /api/register/` – Create a new user account.
- `POST /api/login/` – Log in and receive a JWT token.
- `GET /api/profile/` – Protected: View user profile.
- `GET /swagger/` – Swagger API docs.

---

## Getting Started:

1. Clone this repository:
    ```bash
    git clone https://github.com/Muna-Yusuf/User-Authentication-System.git
    cd User-Authentication-System
    ```
2. Create and activate a virtual environment:
    ```bash
    python -m venv venv  
    source venv/bin/activate
    ```
3. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```
4. Run migrations:
    ```bash
    python manage.py migrate
    ```
5. Start the server:
    ```bash
    python manage.py runserver
    ```

---

## How to Use:

- Register a user:
```bash
POST http://localhost:8000/api/register/
```
    - ```json
         {
            "username": "ali",
            "email": "ali@example.com",
            "password": "yourpassword123*"
        }
    ```
- Login and get token:
```bash
POST http://localhost:8000/api/login/
```
    - ```json 
        {
            "email": "ali@example.com",
            "password": "yourpassword123*"
        }   
    ```
- Use the token to access profile:
```bash
GET http://localhost:8000/api/profile/
Authorization: Bearer <your_token>
```

---

## Testing with Bruno or Postman:

1. Open Bruno or Postman.

2. Create requests for the 3 main endpoints.

3. Register a user, log in, and copy the token.

4. Use the token to authorize the profile request.


---

Made using Django, JWT, and Swagger UI.