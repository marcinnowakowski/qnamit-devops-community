# Medical inquiry devops

This is devops project for medical inquiry project set.

## Django Docker Project

This project demonstrates how to containerize a Django application using Docker. It uses Docker Compose for orchestration and SQLite as the database.

---

### Features

- **Django Backend**: A simple Django application containerized for ease of deployment.
- **SQLite Database**: Lightweight and included with Django by default, perfect for development.
- **Docker Compose**: Simplifies the management of Docker containers.

---

### Directory Structure

```plaintext
project/
├── backend/              # Django application
│   ├── Dockerfile        # Dockerfile for Django
│   ├── manage.py
│   ├── requirements.txt  # Python dependencies
│   ├── app/              # Django app folder
├── docker-compose.yml    # For orchestrating services
└── .env                  # Environment variables
```

---

### Getting Started

#### Prerequisites

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

#### Setup

##### 1. Clone the Repository

```bash
git clone <repository-url>
cd project
```

##### 2. Define Environment Variables

Create a `.env` file in the root directory:

```plaintext
DEBUG=1
SECRET_KEY=your_django_secret_key
```

##### 3. Build and Start the Django Service

```bash
docker-compose up --build
```

##### 4. Apply Migrations

Run the following command in a new terminal:

```bash
docker exec -it django python manage.py migrate
```

##### 5. Create a Superuser

```bash
docker exec -it django python manage.py createsuperuser
```

##### 6. Access the App

- Open your browser and visit: [http://localhost:8000](http://localhost:8000)
