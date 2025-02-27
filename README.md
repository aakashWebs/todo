# Django Todo App

A simple todo app built with Django.

## Setup

### Prerequisites
- Docker
- Docker Compose

### Running the Application

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. Build the Docker containers:
   ```bash
   docker-compose build
   ```

3. Run the application:
   ```bash
   docker-compose up
   ```

4. Access the application at `http://localhost:8000`.

### Environment Variables
You can set the following environment variables in the `docker-compose.yml` file:
- `DATABASE_NAME`: Name of the PostgreSQL database.
- `DATABASE_USER`: PostgreSQL user.
- `DATABASE_PASSWORD`: Password for the PostgreSQL user.
- `DATABASE_HOST`: Host for the PostgreSQL database (default is `db`).
- `DATABASE_PORT`: Port for the PostgreSQL database (default is `5432`).

### Migrations
To apply migrations, you can run:
```bash
docker-compose run web python manage.py migrate
```

### Static Files
To collect static files, run:
```bash
docker-compose run web python manage.py collectstatic
