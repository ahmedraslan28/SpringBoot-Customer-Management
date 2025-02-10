# Customer Management Application

A simple CRUD application built with **Spring Boot**, **PostgreSQL**, and **React.js**. This application allows users to register and log in. Every customer can manage other customer accounts, including adding new customers and updating existing ones. The project is containerized using **Docker** and deployed on **AWS Elastic Beanstalk**.

## Features

- **User Authentication**: Register and log in securely.
- **Customer Management**: Create, update, and manage customer accounts.
- **Exception Handling**: Robust error handling with various exception types.
- **Database Migrations**: Managed using **Flyway**.
- **Testing**:
  - **Unit Testing** for all components.
  - **Integration Testing** using **Testcontainers**, **Mockito**, and **TestNG**.
- **CI/CD**:
  - Automated workflows using **GitHub Actions**.
  - Deployment as a Docker container on **AWS Elastic Beanstalk**.

## Technologies Used

### Backend:
- **Spring Boot** (Java)
- **PostgreSQL**
- **Flyway** (Database migrations)
- **JUnit**, **Mockito**, **Testcontainers**, **TestNG** (Testing)

### Frontend:
- **React.js**

### DevOps & Deployment:
- **Docker** (Containerization)
- **AWS Elastic Beanstalk** (Deployment)
- **GitHub Actions** (CI/CD automation)

## Setup Instructions

### Prerequisites
- **Docker** installed
- **Java 17+**
- **Node.js 18+**
- **PostgreSQL** installed (if running locally)

### Running Locally

1. Clone the repository:
   ```sh
   git clone https://github.com/your-username/customer-management-app.git
   cd customer-management-app
   ```

2. Set up the backend:
   ```sh
   cd backend
   mvn clean install
   mvn spring-boot:run
   ```

3. Set up the frontend:
   ```sh
   cd frontend
   npm install
   npm start
   ```

### Running with Docker

1. Build and start the containers:
   ```sh
   docker compose up --build -d
   ```

2. The backend will be available at: `http://localhost:8081`
3. The frontend will be available at: `http://localhost:3000`

### Running Tests

- **Unit Tests**:
  ```sh
  mvn test
  ```
- **Integration Tests**:
  ```sh
  mvn verify
  ```

## Deployment

### CI/CD with GitHub Actions

1. The GitHub Actions workflow automates building, testing, and deploying the app.
2. On each push, the workflow:
   - Runs unit and integration tests
   - Builds the Docker image
   - Deploys the app to AWS Elastic Beanstalk

