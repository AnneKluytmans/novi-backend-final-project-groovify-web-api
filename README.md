# Groovify - Web API for Vinylshops

## About The Project

**Groovify** is a RESTFUL web API designed to support vinyl stores in efficiently managing their daily operations.
The API is built to optimize workflows for both customers and store employees. It enables customers to browse
collections, place orders and view their order details, while empowering employees to handle inventory and
process orders with ease.

  <br>

<img src="src/main/resources/assets/groovifyLogo.png" alt="Groovify Logo" width="300"/> 

## Table of contents

- [Tech Stack](#tech-stack)
- [Key Features](#key-features)
- [API Endpoints](#api-endpoints)
- [Prerequisites](#prerequisites)
- [How To Run](#how-to-run)
- [Credits](#credits)
- [Licence](#licence)
- [Author](#author)


## Tech Stack
- **Java 17+**
- **Spring Boot 3.4.1** (REST API, Spring Web)
- **Spring Security** (JWT Authentication)
- **Hibernate / JPA** (Entity management)
- **Maven**
- **PasswordEncoder (BCrypt)** for secure password storage
- **PostgreSQL**
- **Swagger** and **Postman** (API documentation)

## Key Features

### 🎵 Product Management
- Customers can **browse the full vinyl collection** with powerful filters (title, artist, genre, year) and sorting options.
- Employees can **add, edit, and remove records** to keep the catalog up-to-date.
- Album cover **upload and download support** makes the catalog visually appealing and intuitive.
- Stock levels are always visible, ensuring popular records never run out unexpectedly.

### 🛒 Order Management
- Customers can **add records to their cart** and place orders with preferred shipping and payment options.
- Automatic **invoice generation** after successful payment for seamless administration.
- Employees can **search, track, and update order statuses** (e.g. *Processing*, *Shipped*), keeping customers informed and orders flowing smoothly.

### 👥 User Management
- Customers can **create accounts**, manage personal data, and view their **order history**.
- Employees can **access customer data** when needed for support or order processing.
- Administrators can **manage accounts**, including blocking or deactivating users if necessary.

### 🔐 Authentication & Authorization
- **Secure login** with JWT-based authentication.
- **Password reset** functionality
- Automatic **role assignment** (USER, EMPLOYEE, ADMIN) during registration.
- **Role-based access control** ensures each user only has access to the right actions and data.

### 🧪 Testing
- Comprehensive **unit tests** for core logic in services.
- **Integration test** covering the ArtistController.


## API Endpoints

### 📦 Postman Collection
A Postman collection is provided for testing and exploring the Groovify API. You can find it in the project resources:
`src/main/resources/postman.json`
You can import this file into Postman to test all available endpoints, including authentication, vinyl management, and order workflows.

### Swagger
Visit http://localhost:8080/swagger-ui.html to explore the API endpoints.

## Prerequisites
Before running the Spring Boot Web API, ensure you have the following installed:

- Java Development Kit (JDK): Corretto 21 ([Download](https://aws.amazon.com/corretto/))
- Maven: Version 4.0.0 ([Download](https://maven.apache.org/download.cgi))
- PostgreSQL: Latest version ([Download](https://www.postgresql.org/download/))
- IntelliJ IDEA or any other IDE supporting Java and Spring Boot ([Download](https://www.jetbrains.com/idea/download/))
- Postman: For API testing ([Download](https://www.postman.com/downloads/))

## How To Run
Follow these steps to set up and run the Spring Boot Web API.

1. Clone the repository or open the project in your IDE (IntelliJ IDEA)

2. Set Up Environment Variables
   Create a `.env` file in the root directory of the project and add the following:
    ```dotenv
    DB_URL=your_database_url
    DB_USERNAME=your_username
    DB_PASSWORD=your_password
    ```
   Alternatively, you can copy the provided `.env.example`file:
    ```
    cp .env.example .env
    ```

3.  Configure the PostgreSQL Database
    - Create a PostgreSQL database
    - Fill the `.env` file with your database credentials to configure the database connection
    
4. Build the Project
   Use Maven to build the project:
    ```
    mvn clean install
    ```
5. Run the Application
   Start the Spring Boot application with the following command:
    ```
    mvn spring-boot:run
    ```
6. The server will start at: `http://localhost:8080`

7. API Documentation and Testing
   - Swagger UI: Visit http://localhost:8080/swagger-ui.html to explore API endpoints.
   - Postman: Import the provided Postman collection for testing API requests.


## Acknowledgements
> "This assignment was developed for the Backend Java module in the NOVI Software Development program."

## License
> "This repository is intended for educational purposes only. You are welcome to use the code for learning, but not for commercial use."

## Author
> "This project was developed by [Anne Kluytmans](https://github.com/AnneKluytmans), a Software Development student at [NOVI](https://www.novi.nl/)."