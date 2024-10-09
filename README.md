# CS764: Task Management System
> Benzon Carlitos Salazar (salazarbc24@uww.edu)

## Project Overview:
- **Objective**: A task management web application where users can create, edit, and manage tasks. Tasks are stored in a 
MySQL database, and Python is used to manage backend logic, including APIs, user authentication, and database interactions.
  
## Key Components:
1. **Google Cloud Services**:
  - **Cloud SQL**: Host a MySQL database for storing task data (task name, due date, status, etc.).
  - **Google App Engine or Cloud Run**: Deploy a Python-based backend (e.g., Flask or Django) to handle API requests, 
  user authentication, and business logic.
  - **Cloud IAM**: For managing authentication and authorization.

2. **Backend**:
  - **Python (Flask/Django)**: Handle API endpoints for CRUD (Create, Read, Update, Delete) operations on tasks, 
  authentication, and user management.
  - Use **SQLAlchemy** or **PyMySQL** to interact with MySQL.

3. **Frontend**:
  - A web interface using **HTML/CSS/JavaScript** (possibly a front-end framework like React or Vue.js) for users to 
  interact with the system.

## Features:
- **User Authentication**: Register/login users.
- **CRUD Functionality**: Create, update, and delete tasks. Mark tasks as complete or set deadlines.
- **Task Categorization**: Users can group tasks by projects or categories.

## Project Structure:

```
task_manager_gcp/
│
├── backend/
│   ├── app/
│   │   ├── __init__.py        # Initialization for Flask/Django app
│   │   ├── models.py          # SQLAlchemy models for database entities
│   │   ├── routes/
│   │   │   ├── __init__.py    # Initialization for routes
│   │   │   ├── auth.py        # Authentication routes (login, register)
│   │   │   ├── tasks.py       # Task-related API endpoints
│   │   └── utils/
│   │       ├── __init__.py    # Initialization for utilities
│   │       ├── db.py          # Database connection and ORM setup
│   │       └── auth.py        # Authentication utilities (JWT, etc.)
│   ├── config.py              # Configuration settings (Google Cloud, database, etc.)
│   └── main.py                # Main entry point for the backend application
│
├── frontend/
│   ├── public/
│   │   ├── index.html         # Main HTML file
│   │   ├── css/
│   │   │   └── styles.css     # Stylesheet
│   │   └── js/
│   │       └── main.js        # JavaScript logic for frontend
│   ├── src/
│   │   ├── components/        # Reusable components (if using React/Vue)
│   │   ├── pages/             # Page-specific components
│   │   └── App.js             # Main React/Vue component
│   └── package.json           # Dependencies for frontend framework
│
├── migrations/
│   └── ...                    # Database migration files (if using Flask-Migrate/Django)
│
├── tests/
│   ├── test_auth.py           # Tests for authentication
│   ├── test_tasks.py          # Tests for task management features
│   └── ...
│
├── Dockerfile                 # Dockerfile for containerizing the application
├── docker-compose.yml         # Docker Compose file for multi-container setup (backend, frontend, database)
├── requirements.txt           # Python dependencies
├── .env                       # Environment variables (secret keys, DB credentials, etc.)
└── README.md                  # Project overview and setup instructions
```
