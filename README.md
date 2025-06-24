Late Show API  

A Flask-based REST API for managing a database of late show guests, built with SQLAlchemy and Alembic for migrations.

Features
RESTful API endpoints for managing resources
Database migrations with Alembic via Flask-Migrate
Seed scripts for populating the database
Modular structure for controllers and models
Project Structure
server/
  app.py            # Main Flask app
  config.py         # Configuration settings
  seed.py           # Database seeding script
  controllers/      # API route handlers
  models/           # SQLAlchemy models
migrations/         # Alembic migration scripts
instance/
  late_show.db      # SQLite database (local)
extensions.py       # Custom Flask extensions
requirements.txt    # Python dependencies
Setup
Clone the repository

git clone <repo-url>
cd late-show-api-challenge
Create and activate a virtual environment

python3 -m venv env
source env/bin/activate
Install dependencies

pip install -r requirements.txt
Set environment variables

export FLASK_APP=server/app.py
export FLASK_ENV=development
Initialize the database

flask db init
flask db migrate -m "Initial migration"
flask db upgrade
Seed the database (optional)

python server/seed.py
Run the server

flask run
Database Migrations
Create migration repository:
flask db init
Generate migration:
flask db migrate -m "Message"
Apply migrations:
flask db upgrade
Downgrade:
flask db downgrade