**Spring Boot E-Commerce REST API**

A backend REST API for a simple E-Commerce system built using Spring Boot, Spring Data JPA, and MySQL.
This project demonstrates how to design and build a modular backend with layered architecture using modern Java frameworks.

**🚀 Features**
User Registration
User Login
Product Management
Add Products
View All Products
Update Product Stock
Delete Products
REST API based architecture
MySQL database integration using JPA

**🧱 Project Architecture**
The application follows a layered architecture:
Controller → Service → Repository → Database

Example flow:
HTTP Request → Controller → Service Logic → Repository (JPA) → MySQL

This structure keeps the application modular, maintainable, and scalable.

🛠️ Tech Stack

Java 17
Spring Boot
Spring Data JPA
MySQL
Maven
REST API

**📂 Project Structure**
src/main/java/com/ecommerce
│
├── controller
│   ├── UserController.java
│   └── ProductController.java
│
├── service
│   ├── UserService.java
│   └── ProductService.java
│
├── repository
│   ├── UserRepository.java
│   └── ProductRepository.java
│
├── model
│   ├── User.java
│   └── Product.java
│
└── EcommerceApplication.java
Postman (for API testing)

**⚙️ Setup & Installation**
1. Clone the repository
git clone https://github.com/YOUR_USERNAME/springboot-ecommerce-api.git
2. Open the project
Open the project in VS Code or IntelliJ IDEA.
3. Configure Database
Edit:
src/main/resources/application.properties
Example configuration:
spring.datasource.url=jdbc:mysql://localhost:3306/ecommerce
spring.datasource.username=root
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
server.port=8081
4. Run the application
./mvnw spring-boot:run
Application will start at:
http://localhost:8081

**📡 API Endpoints**
User APIs
**Register User**
POST /users/register
Example request:
{
"name": "Meena",
"email": "meena@gmail.com",
"password": "123"
}
**Login User**
POST /users/login?email=meena@gmail.com&password=123

**Product APIs**
Add Product
POST /products/add
Example request:
{
"name": "Laptop",
"price": 55000,
"stock": 10
}
Get All Products
GET /products/all
Update Product Stock
PUT /products/updateStock/{id}?stock=20
Delete Product
DELETE /products/delete/{id}

**🧪 API Testing**
All APIs were tested using Postman.
Steps:

1.Start the Spring Boot application
2.Open Postman
3.Send requests to http://localhost:8081
4.Use JSON body for POST requests
