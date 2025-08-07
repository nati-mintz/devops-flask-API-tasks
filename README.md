#  Simple Task API with Flask

This is a simpel Python REST API built with Flask that allows users to manage a list of tasks using HTTP methods: `GET` and `POST`.

## Project Overview

This application was built as part of a DevOps mini-project. It demonstrates how to build and containerize a Flask-based REST API and run it inside a Docker container.

The API supports:
- `GET /tasks` – Fetch all tasks.
- `POST /tasks` – Add a new task to the list.

##  Tech Stack

- Python 3.11
- Flask 3.1
- Docker

##  How to Run Locally (Without Docker)

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/your-repo.git
   cd your-repo

2. **Create virtual environment**
   ```bash
   python3 -m venv venv
   source venv/bin/activate

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt

4. **Run the app**
   ```bash
   python app.py
   
**Visit the API at: http://localhost:5000/tasks**

## Running with Docker
1. **build the Docker image**
    ```bash
   docker build -t flask-task-api .

2. **Run the container**
    ```bash
    docker run -d -p 5000:5000 flask-task-api

**The API will be available at: http://localhost:5000/tasks**

## Usage Examples (with curl)
### Add a new task
 ```bash
curl -X POST http://localhost:5000/tasks \
     -H "Content-Type: application/json" \
     -d '{"title": "Learn Flask"}'
```

### Get all taskes
  ```bash
  curl http://localhost:5000/tasks





