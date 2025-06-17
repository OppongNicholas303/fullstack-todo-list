

# Full-Stack Todo List Application

This repository hosts a full-stack Todo List application designed to allow users to create, manage, and organize their tasks efficiently. The application features a React-based frontend and a Node.js backend, utilizing MongoDB for data persistence.

## Technologies Used

- **Frontend**: React, Material-UI
- **Backend**: Node.js, Express
- **Database**: MongoDB
- **Other Tools**: Vite, React Toastify, Lucide Icons

## Project Structure

The project is divided into two main parts:
- **Frontend**: Located in the `frontend/` directory with its own [README](frontend/README.md).
- **Backend**: Located in the `backend/` directory with its own [README](backend/README.md).

## Features

- Create, view, update, and delete todo items.
- Organize tasks with tags/categories.
- Responsive user interface adaptable to different screen sizes.
- Real-time updates without page reloads.

## Contributing

Contributions are welcome! See the specific README files in the `frontend/` and `backend/` directories for more details on contributing.

## Live Demo

<h4 align="left">Live Preview is available at https://fullstack-todolist-1.onrender.com/</h4>

## Snapshots

<img src="./Frontend/src/assets/home-snapshot.png" alt="home page"/>

## Containerized Setup

### Prerequisites
- Docker and Docker Compose installed on your machine.

### Building and Running the Containers
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. Build and start the containers:
   ```bash
   docker-compose up --build
   ```

3. Access the application:
   - Frontend: http://localhost:80
   - Backend API: http://localhost:3000

### Stopping the Containers
```bash
docker-compose down
```

## Network and Security Configurations
- **Frontend:** Served on port 80 using Nginx.
- **Backend:** Exposed on port 3000.
- **Database (MongoDB):** Exposed on port 27017.
- **Environment Variables:** Database connection string is set in the `docker-compose.yml` file.

## Troubleshooting Guide
- **Container Not Starting:** Check logs using `docker-compose logs`.
- **Database Connection Issues:** Ensure MongoDB is running and the connection string is correct.
- **Frontend Not Accessible:** Verify Nginx configuration and check if the frontend build was successful.

## Testing Script
To verify that all services are running correctly, execute the following commands:

```bash
# Test Frontend
curl http://localhost:80

# Test Backend
curl http://localhost:3000/api/todos

# Test Database Connection
docker exec -it <mongo-container-id> mongo --eval "db.adminCommand('ping')"
```

## Self-Review: Meeting Assessment Requirements

### Dockerfile(s) for Each Component
- **Frontend:** Multi-stage build with Node.js and Nginx for efficient static file serving.
- **Backend:** Node.js setup with proper port exposure.
- **Database:** Official MongoDB image with secure configuration.

### Docker Compose File
- Orchestrates all three services (frontend, backend, database) with proper networking, volumes, and environment variables.

### Documentation
- **Setup Instructions:** Clear, step-by-step guide for building, running, and stopping containers.
- **Network & Security:** Detailed explanation of ports, environment variables, and security settings.
- **Troubleshooting Guide:** Common issues and solutions provided.

### Container Testing Script
- Commands to verify frontend, backend, and database connectivity.

### Conclusion
The current setup fully meets the requirements of the Cloud Engineering Pathway Assessment, providing a secure, efficient, and well-documented containerized application.

