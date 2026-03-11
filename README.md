# Spring Boot E-Commerce REST API

A backend REST API for a simple E-Commerce system built using **Spring Boot**, **Spring Data JPA**, and **MySQL**.
This project demonstrates how to design and build a layered backend architecture using controllers, services, repositories, and entities.

---

## Tech Stack

* Java 17
* Spring Boot
* Spring Web
* Spring Data JPA
* MySQL
* Maven
* REST APIs
* Postman (for API testing)

---

## Project Features

### User Module

* User registration
* User login
* Stores user information in MySQL database

### Product Module

* Add new product
* View all products
* Update product stock
* Delete product

### Database Integration

* MySQL database connectivity
* ORM using Spring Data JPA
* Automatic table mapping using entities

---

## Project Structure

src/main/java/com/ecommerce

controller → REST API endpoints
service → business logic
repository → database access layer
model → entity classes
EcommerceApplication.java → Spring Boot main class

Example structure:

com.ecommerce
├── controller

│   ├── UserController.java

│   └── ProductController.java

├── service

│   ├── UserService.java

│   └── ProductService.java

├── repository

│   ├── UserRepository.java

│   └── ProductRepository.java

├── model

│   ├── User.java

│   └── Product.java

└── EcommerceApplication.java

---

## Database Configuration

Update the file:

src/main/resources/application.properties

```
spring.datasource.url=jdbc:mysql://localhost:3306/ecommerce
spring.datasource.username=root
spring.datasource.password=YOUR_PASSWORD

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

server.port=8081
```

---

## Running the Application

Clone the repository

```
git clone https://github.com/Sravani-1309/springboot-ecommerce-api.git
```

Navigate to project folder

```
cd springboot-ecommerce-api
```

Run the application

```
./mvnw spring-boot:run
```

The server will start at

```
http://localhost:8081
```

---

## API Endpoints

### User APIs

Register User

POST

```
/users/register
```

Body

```
{
"name":"Meena",
"email":"meena@gmail.com",
"password":"123"
}
```

Login User

POST

```
/users/login?email=meena@gmail.com&password=123
```

---

### Product APIs

Add Product

POST

```
/products/add
```

Body

```
{
"name":"Laptop",
"price":55000,
"stock":10
}
```

Get All Products

GET

```
/products/all
```

Update Product Stock

PUT

```
/products/updateStock/{id}?stock=20
```

Delete Product

DELETE

```
/products/delete/{id}
```

---

## Testing APIs

All APIs were tested using **Postman**.

Example workflow:

1. Start Spring Boot application
2. Open Postman
3. Send HTTP requests to the endpoints
4. Verify responses and database changes
