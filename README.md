# errand-api
Simple Errand Request API built with Spring Boot
What I Built
A RESTful web service with two endpoints:
POST /errands – create a new errand (title and description)
GET /errands – retrieve all errands
Each errand is stored in an H2 in‑memory database.
Validation ensures the title cannot be empty (using @Valid and @NotBlank).
Proper HTTP status codes are returned:
201 Created for successful creation
200 OK for listing
400 Bad Request when validation fails
Global error handling returns user‑friendly field error messages.
The code is organised with DTOs, Entity, Repository, and Controller layers.
Lombok reduces boilerplate (getters/setters/constructors).
How to Run It
Prerequisites
Java 17 or 21 installed
Maven (or use the included Maven wrapper)
What I Would Improve (If I Had More Time)
Add Unit and Integration Tests
Write tests for the controller (@WebMvcTest) and repository (@DataJpaTest) to ensure reliability.
Implement Update and Delete Endpoints
Add PUT /errands/{id} and DELETE /errands/{id} for full CRUD functionality.
Pagination and Sorting
For the GET /errands endpoint, add pagination (e.g., ?page=0&size=10) to handle large lists.
Use a Persistent Database
Replace H2 with PostgreSQL or MySQL for production readiness, and add migration tools (Flyway/Liquibase).
Add API Documentation
Integrate SpringDoc OpenAPI (Swagger) to generate interactive API docs.
Enhance Validation
Add more constraints (e.g., description length, custom validation rules).
Logging and Monitoring

Include structured logging and health endpoints (Spring Boot Actuator).
