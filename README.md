# MyTODO

A simple Flask todo application with SQLite storage. Add, view, update, and delete todo items through a Bootstrap-based web interface.

## Features

- Create todos with a title and description
- View all saved todos
- Update existing todos
- Delete todos
- SQLite database storage
- Runs locally or on Render with Gunicorn

## Tech Stack

- Python
- Flask
- Flask-SQLAlchemy
- SQLite
- Bootstrap 5
- Gunicorn

## Live Demo

https://todo-app-flask-1qky.onrender.com

## Run Locally

### 1. Clone the repository

```powershell
git clone https://github.com/kshitizsrf/todo-app-flask.git
cd todo-app-flask
```

### 2. Create and activate a virtual environment

```powershell
py -3.12 -m venv .venv
.\.venv\Scripts\Activate.ps1
```

### 3. Install dependencies

```powershell
python -m pip install -r requirements.txt
```

### 4. Start the application

```powershell
python app.py
```

Open http://127.0.0.1:8000/ in your browser.

## Deploy on Render

Create a new **Web Service** on [Render](https://render.com) and connect this GitHub repository.

Use these settings:

- **Build command:** `pip install -r requirements.txt`
- **Start command:** `gunicorn app:app`
- **Environment:** `Python 3`

Render will provide a public `onrender.com` URL after deployment.

## Project Structure

```text
.
├── app.py
├── requirements.txt
├── Procfile
├── instance/
│   └── todo.db
├── static/
│   ├── css/style.css
│   └── js/ksh.js
└── templates/
    ├── body.html
    ├── navbar.html
    └── update.html
```

## Database Note

The app uses SQLite through Flask-SQLAlchemy. On hosting platforms such as Render, the local filesystem may be reset during redeployments or service restarts. For durable production data, use a managed PostgreSQL database and configure the database URL through an environment variable.
