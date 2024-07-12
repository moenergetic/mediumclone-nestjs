## Prerequisites

Make sure you have the following installed on your machine:

- Docker
- Docker Compose
- Node.js (v14 or higher)
- npm (v6 or higher)
- PostgreSQL (used in Docker)

## Getting Started

### Clone the Repository

```bash
git clone <repository_url>
cd <repository_name>
```

### Docker Compose

To set up and run the project using Docker Compose, use the following command:

```bash
docker-compose up --build
```

This command will build and start the Docker containers defined in the `docker-compose.yml` file.

### Install Dependencies & Running Migrations

To install the project dependencies, run:

```bash
npm install
```

To run the database migrations, use the following command:

```bash

npm run migration:run
```

This command will execute all pending migrations and update your database schema.

### Starting the Development Server

To start the development server, use the following command:

```bash
npm run start:dev
```

This command will start the NestJS application in development mode with hot-reload enabled.

## Additional Commands

### Stopping the Containers

To stop the Docker containers, use:

```bash
docker-compose down
```

### Viewing Logs

To view the logs of the running containers, use:

```bash
docker-compose logs -f
```

To access the database

```bash
docker ps ## copy the CONTAINER ID
docker exec -it <CONTAINER ID> psql -U user -d mydatabase
```

## Testing API Endpoints

You will find all the necessary requests in the `req.http` file. This file can be used with tools like VS Code's REST Client extension to easily test the API endpoints.

To use the `req.http` file, follow these steps:

1. Open the `req.http` file in your code editor.
2. Install the REST Client extension if you are using VS Code.
3. Execute the requests directly from the file to interact with the API.
