# Student Result Management System
=====================================

## Overview
-----------

The Student Result Management System is a Flask-based web application designed to manage student results. The system allows students to log in, view their results, and provides administrators with the ability to upload new results. The application utilizes a SQLite database to store student information and results.

## Features
------------

* **Student Login**: Students can log in to the system using their unique credentials.
* **Result Upload**: Administrators can upload new results for students.
* **Result Viewing**: Students can view their uploaded results.
* **SQLite Database**: The system uses a SQLite database to store student information and results.
* **REST API**: The system provides a REST API for interacting with the application programmatically.

## Installation
------------

To install the Student Result Management System, follow these steps:

1. **Clone the repository**: `git clone https://github.com/your-username/student-result-management-system.git`
2. **Install dependencies**: `pip install -r requirements.txt`
3. **Create the database**: `python create_db.py`
4. **Run the application**: `python app.py`

## Usage
-----

1. **Start the application**: `python app.py`
2. **Open a web browser**: Navigate to `http://localhost:5000` to access the application.
3. **Log in**: Students can log in using their unique credentials.
4. **Upload results**: Administrators can upload new results for students.
5. **View results**: Students can view their uploaded results.

## API Endpoints
--------------

The following API endpoints are available:

### Student Endpoints

* **GET /students**: Retrieve a list of all students.
* **GET /students/<int:student_id>**: Retrieve a specific student by ID.
* **POST /students**: Create a new student.
* **PUT /students/<int:student_id>**: Update a specific student.
* **DELETE /students/<int:student_id>**: Delete a specific student.

### Result Endpoints

* **GET /results**: Retrieve a list of all results.
* **GET /results/<int:result_id>**: Retrieve a specific result by ID.
* **POST /results**: Create a new result.
* **PUT /results/<int:result_id>**: Update a specific result.
* **DELETE /results/<int:result_id>**: Delete a specific result.

### Login Endpoints

* **POST /login**: Log in to the application.
* **GET /logout**: Log out of the application.

### Example API Usage

```bash
# Retrieve a list of all students
curl http://localhost:5000/students

# Create a new student
curl -X POST -H "Content-Type: application/json" -d '{"name": "John Doe", "email": "john@example.com"}' http://localhost:5000/students

# Upload a new result
curl -X POST -H "Content-Type: application/json" -d '{"student_id": 1, "result": 90}' http://localhost:5000/results
```

Note: Replace `http://localhost:5000` with the actual URL of your application.