# nimaptest Nimap Clients & Projects API

A Django REST Framework (DRF) project that manages Clients and their Projects, with PostgreSQL as the database.

🚀 Features

Create, list, update, and delete Clients

Assign Projects to Clients

Link Projects with existing Users

Retrieve Client details with their Projects

Retrieve all Projects assigned to the logged-in user

Token-based authentication for secured APIs

🛠️ Tech Stack

Backend: Django 5, Django REST Framework

Database: PostgreSQL

Authentication: Token-based (DRF Auth Token)

Tools: Git, Postman

📌 API Endpoints
Clients

GET /clients/ → List all clients

POST /clients/ → Create a new client

GET /clients/:id/ → Get client details with projects

PUT/PATCH /clients/:id/ → Update client details

DELETE /clients/:id/ → Delete a client

Projects

POST /clients/:id/projects/ → Create a new project under a client

GET /projects/ → List all projects assigned to logged-in user

🗄️ Example
Create a new Client

Request:

POST /clients/
{
  "client_name": "Company A"
}


Response:

{
  "id": 3,
  "client_name": "Company A",
  "created_at": "2025-09-14T11:03:55.931739+05:30",
  "created_by": "Rohit"
}

⚙️ Setup Instructions

Clone the repo

git clone https://github.com/ajayanilgogane/nimaptest.git
cd nimaptest


Create virtual environment & install dependencies

python -m venv venv
venv\Scripts\activate   # Windows
source venv/bin/activate # Linux/Mac

pip install -r requirements.txt


Configure PostgreSQL in settings.py

Apply migrations

python manage.py migrate


Create a superuser

python manage.py createsuperuser


Run server

python manage.py runserver


✍️ Author: Ajay Anil Gogane
