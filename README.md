# late-show-api-challenge

## Late Show API

A Flask RESTful API managing a Late Night TV show system with episodes, guests, appearances, and user authentication.

## Project Overview

This API includes:

- PostgreSQL database  
- JWT token-based authentication  
- MVC architecture  
- CRUD for episodes, guests, appearances  
- Protected routes for sensitive actions  
- Tested with Postman / Thunder Client  

---

## Setup Instructions

### Prerequisites

- Python 3.8+  
- PostgreSQL installed and running  
- Pipenv for dependency management  

### Database Setup

Create the PostgreSQL database:

```sql
CREATE DATABASE late_show_db;

Set environment variables (optional, or update server/config.py):

bash
Copy
Edit
export DATABASE_URL="postgresql://<username>:<password>@localhost:5432/late_show_db"
export SECRET_KEY="your-secret-key"
export JWT_SECRET_KEY="your-jwt-secret"

Install Dependencies
bash
Copy
Edit
pipenv install
pipenv shell


Running the Application
Initialize and migrate the database:

bash
Copy
Edit
export FLASK_APP=server/app.py
flask db init
flask db migrate -m "initial migration"
flask db upgrade
Seed the database:

bash
Copy
Edit
python server/seed.py
Run the app:

bash
Copy
Edit
flask run
The app runs at: http://127.0.0.1:5000/

Authentication Flow
Register: POST /auth/register
Payload example:

json
Copy
Edit
{
  "username": "tyra",
  "password": "Wakera2006"
}
Response: Confirmation message.

Login: POST /auth/login
Payload example:

json
Copy
Edit
{
  "username": "tyra",
  "password": "Wakera2006"
}
Response: JWT access token.

License
MIT License

GitHub Repository
https://github.com/3Tyra/late-show-api-challenge