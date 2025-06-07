# Microservice Spring Security Program 🚀

![Microservices](https://img.shields.io/badge/Microservices-Enabled-brightgreen) ![Java](https://img.shields.io/badge/Java-11-orange) ![Spring Boot](https://img.shields.io/badge/Spring%20Boot-2.5.4-blue) ![Spring Security](https://img.shields.io/badge/Spring%20Security-5.5.2-lightgrey)

Welcome to the **Microservice Spring Security Program**! This repository contains a complete microservices-based Java application that showcases secure communication between services. We utilize Spring Boot, Spring Security, and JWT-based authentication to ensure that our services are robust and secure.

## Table of Contents

1. [Overview](#overview)
2. [Technologies Used](#technologies-used)
3. [Features](#features)
4. [Architecture](#architecture)
5. [Setup and Installation](#setup-and-installation)
6. [Usage](#usage)
7. [API Endpoints](#api-endpoints)
8. [Testing](#testing)
9. [Contributing](#contributing)
10. [License](#license)
11. [Releases](#releases)

## Overview

This application is designed to demonstrate the power of microservices architecture. Each service is modularized, which allows for easier management and scaling. We implement role-based access control to manage user permissions effectively. The system also includes service discovery, which enhances scalability and reliability.

## Technologies Used

- **Java**: The primary programming language used for backend development.
- **Spring Boot**: A framework that simplifies the development of Java applications.
- **Spring Security**: Provides security features to protect our application.
- **JWT (JSON Web Tokens)**: Used for secure communication and authentication.
- **Eureka**: Service discovery for managing microservices.
- **MySQL**: Database for storing application data.
- **Postman**: Tool for testing APIs.
- **Maven**: Dependency management and build tool.
- **RESTful API**: Standard for building APIs.

## Features

- **Secure Communication**: All services communicate securely using JWT for authentication.
- **Role-Based Access Control**: Users have different access levels based on their roles.
- **Modular Architecture**: Each service is a separate module, making it easy to manage and scale.
- **Service Discovery**: Eureka enables services to find and communicate with each other.
- **RESTful APIs**: All services expose RESTful APIs for easy integration.
- **Database Integration**: MySQL is used for persistent data storage.

## Architecture

The architecture of this application is designed to support microservices. Below is a simple diagram illustrating the architecture:

```
+------------------+        +------------------+
|   API Gateway    | <----> |   Service A      |
+------------------+        +------------------+
|                  | <----> |   Service B      |
+------------------+        +------------------+
|                  | <----> |   Service C      |
+------------------+        +------------------+
|                  | <----> |   Eureka Server   |
+------------------+        +------------------+
```

- **API Gateway**: Routes requests to the appropriate service.
- **Service A, B, C**: Individual microservices handling different functionalities.
- **Eureka Server**: Manages service registration and discovery.

## Setup and Installation

To set up the application locally, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/viking19/Microservice_Spring-Security_Program.git
   cd Microservice_Spring-Security_Program
   ```

2. **Install Dependencies**:
   Make sure you have Maven installed. Run the following command to install dependencies:
   ```bash
   mvn clean install
   ```

3. **Set Up MySQL**:
   - Create a new MySQL database.
   - Update the `application.properties` file with your database credentials.

4. **Run the Application**:
   You can run each service individually using:
   ```bash
   mvn spring-boot:run
   ```

## Usage

Once the application is running, you can access the API Gateway to route requests to the respective services. Use Postman to test the endpoints. Ensure you include the JWT token in the headers for secure access.

## API Endpoints

Here are some key API endpoints you can use:

- **User Registration**: 
  ```
  POST /api/auth/register
  ```

- **User Login**: 
  ```
  POST /api/auth/login
  ```

- **Get User Details**: 
  ```
  GET /api/user/details
  ```

- **Service A Endpoint**: 
  ```
  GET /api/serviceA/data
  ```

- **Service B Endpoint**: 
  ```
  GET /api/serviceB/data
  ```

Make sure to include the JWT token in the headers for authenticated requests.

## Testing

You can use Postman to test the API endpoints. Create a collection for the various endpoints and include sample requests for easy testing. 

### Sample Postman Collection

To make testing easier, you can download the Postman collection from the [Releases section](https://github.com/viking19/Microservice_Spring-Security_Program/releases). This collection includes predefined requests for each API endpoint.

## Contributing

We welcome contributions to improve this project. If you have suggestions or find bugs, please open an issue or submit a pull request. 

### Steps to Contribute:

1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Releases

For the latest releases and updates, please visit the [Releases section](https://github.com/viking19/Microservice_Spring-Security_Program/releases). You can download and execute the latest files from there.

---

Thank you for checking out the **Microservice Spring Security Program**! We hope you find this application useful and informative. If you have any questions, feel free to reach out or create an issue in the repository.