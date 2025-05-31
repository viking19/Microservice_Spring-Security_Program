📖 About the Project:
⏩This project showcases a real-world implementation of a secure microservice architecture using Java Spring Boot. It includes multiple services communicating with each other via REST APIs and secured using JWT tokens. Authentication and authorization are handled centrally, ensuring each service is protected against unauthorized access.


🔧 Core Modules:
⏩authservice – Manages user login, registration, and JWT token generation.
⏩microservice-1 – A protected microservice that handles domain-specific logic and requires valid tokens for access.
⏩api-gateway – Central gateway routing all API requests, also responsible for token validation before passing to microservices.
⏩service-registry-eureka – A Eureka-based service registry for discovering microservices dynamically.


🚀 Key Features:
☑️Spring Boot microservice structure
☑️JWT-based login and authentication
☑️Role-based access control
☑️API Gateway using Spring Cloud Gateway
☑️Eureka Service Registry
☑️RESTful APIs with secure endpoints
☑️Maven-based build for all modules
☑️Environment ready for deployment or Dockerization


📚 Tech Stack / Topics:
✅Java 8+
✅Spring Boot
✅Spring Security
✅Spring Cloud Gateway
✅Spring Cloud Eureka
✅JWT (JSON Web Token)
✅REST APIs
✅Maven
✅Microservices Architecture


⚙️ Database Configuration
Ensure your MySQL server is running and configured properly. Example application.properties in 'authservice':

properties:-
spring.datasource.url=jdbc:mysql://localhost:3306/db name.
spring.datasource.username=root
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL5InnoDBDialect

📢Replace yourpassword with your actual MySQL root password.


🔐 Authentication Flow
✅User registers or logs in via authservice.
✅A JWT token is generated and returned.
✅Token is passed in the header for subsequent requests to secured endpoints (like microservice-1).
✅api-gateway intercepts and validates the token before routing to microservices.


📫 How to Test Using Postman
✅Register User: POST http://localhost:8081/auth/register
✅Login User: POST http://localhost:8081/auth/login → Receives JWT token
✅Access Secure Endpoint:
✅GET http://localhost:8082/data (Requires Bearer Token in Header)
✅Add Header: Authorization: Bearer <your-token>


🧪 Run Instructions
✅Start MySQL server and create required database.
✅Start service-registry-eureka first.
✅Start authservice, then microservice-1, and finally api-gateway.
✅Test APIs using Postman as described above.


📁 Folder Structure
Copy
Edit
Microservice_Spring-security_Program/
│
├── api-gateway
├── authservice
├── microservice-1
└── service-registry-eureka


📜 License
☑️This project is for learning and demonstration purposes.
