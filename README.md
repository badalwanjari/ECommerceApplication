# E-Commerce Backend with Spring Boot & JWT Authentication
## Overview
This project is a fully functional backend for an e-commerce platform, developed using Spring Boot. It features secure user authentication using JSON Web Tokens (JWT) and provides a comprehensive set of RESTful APIs to manage products, categories, carts, orders, and user profiles.

## Features
- ___JWT Authentication:___ Secure login and registration with token-based authentication.
- ___User Management:___ APIs for user registration, login, and profile management.
- ___Product Management:___ CRUD operations for products and categories.
- ___Cart Management:___ APIs for adding/removing products, updating quantities, and viewing cart details.
- ___Order Processing:___ Order creation, payment integration, and order status management.

## Technologies Used
- _Spring Boot:_ Core framework for building the application.
- _Spring Security:_ For implementing JWT-based authentication and authorization.
- _Hibernate/JPA:_ For database interactions.
- _MySQL:_ Database to store all the e-commerce data.
- _Maven:_ Build and dependency management tool.
- _Swagger:_ API documentation and testing.

## API Endpoints

### Authentication
- POST /api/login - User login.
- POST /api/register - User registration.
### User Management
- GET /api/public/users/{emailId}/orders - Get orders for a user.
- GET /api/public/users/{emailId}/carts/{cartId} - Get user's cart details.
- POST /api/public/users/{emailId}/carts/{cartId}/payments/{paymentMethod}/order - Process payment and create an order.
### Product Management
- GET /api/public/categories - Get all categories.
- GET /api/public/categories/{categoryId}/products - Get products by category.
- GET /api/public/products/keyword/{keyword} - Search products by keyword.
- POST /api/admin/categories - Add a new category.
- PUT /api/admin/categories/{categoryId} - Update category details.
- DELETE /api/admin/categories/{categoryId} - Delete a category.
### Cart Management
- POST /api/public/carts/{cartId}/product/{productId} - Add a product to the cart.
- PUT /api/public/carts/{cartId}/products/{productId}/quantity/{quantity} - Update product quantity in the cart.
- DELETE /api/public/carts/{cartId}/products/{productId} - Remove a product from the cart.
### Order Management
- GET /api/admin/orders - Get all orders (Admin).
- PUT /api/admin/users/{emailId}/orders/{orderId}/orderStatus/{orderStatus} - Update order status (Admin).
- GET /api/public/users/{emailId}/orders/{orderId} - Get order details for a user.

## Installation
- Clone the Repository:
```sh
git clone https://github.com/yourusername/ecommerce-backend.git
cd ecommerce-backend
Set Up MySQL Database: Create a MySQL database and update the application.properties file with your database credentials.
```

- Build the Project:
```sh
mvn clean install
```

- Run the Application:
```sh
mvn spring-boot:run
```

Access the API Documentation: Visit [http://localhost:8080/swagger-ui/index.html](http://localhost:8080/swagger-ui/index.html) to view and test the APIs.

## Project Structure
- /src/main/java - Contains the Java source code, organized by packages.
- /src/main/resources - Contains application properties and other resources.
- /target - Contains the compiled output of the project.
  
## Future Enhancements
- _Payment Gateway Integration:_ Enhance the payment process with real-world payment gateway integration.
- _Role-Based Access Control:_ Implement role-based permissions to distinguish between admin and regular users.
- _Caching:_ Introduce caching mechanisms to improve performance for frequently accessed data.
- _Email notifications_
