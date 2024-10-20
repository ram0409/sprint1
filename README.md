# Order Service API

## Overview

The **Order Service API** is a RESTful web service built using Spring Boot that allows you to manage customer orders. The API provides functionality to perform CRUD (Create, Read, Update, Delete) operations on orders, including retrieving all orders, fetching a specific order by its ID, creating new orders, updating existing orders, and deleting orders.

## Features

- **Get all orders**: Retrieve a list of all orders.
- **Get order by ID**: Retrieve a specific order by its ID.
- **Create a new order**: Add a new order to the system.
- **Update an order**: Update details of an existing order.
- **Delete an order**: Remove an order from the system.

## Technologies Used

- Java
- Spring Boot
- Spring Data JPA (for database interaction)
- H2 (in-memory database, can be replaced with any other relational database)
- Maven (for project management and build)
- REST API design principles

## Prerequisites

- Java Development Kit (JDK) 8 or later
- Maven 3.6+
- Any IDE (e.g., IntelliJ IDEA, Eclipse) for running the project

## Setup and Running the Application

1. **Clone the repository**:
   ```bash
   git clone https://github.com/ram0409/order-service.git
   cd order-service
   ```

2. **Build the project**:
   ```bash
   mvn clean install
   ```

3. **Run the application**:
   ```bash
   mvn spring-boot:run
   ```

4. **Access the API**:
   The application will run on `http://localhost:8080`. Use any API client like Postman or curl to interact with the endpoints.

## API Endpoints

### Get All Orders

- **URL**: `/orders`
- **Method**: `GET`
- **Response**: List of orders
- **Example**:
  ```bash
  curl -X GET http://localhost:8080/orders
  ```

### Get Order by ID

- **URL**: `/orders/{id}`
- **Method**: `GET`
- **Response**: The order with the given ID
- **Example**:
  ```bash
  curl -X GET http://localhost:8080/orders/1
  ```

### Create a New Order

- **URL**: `/orders`
- **Method**: `POST`
- **Request Body**: JSON object representing the order
- **Response**: The created order
- **Example**:
  ```bash
  curl -X POST http://localhost:8080/orders \
  -H 'Content-Type: application/json' \
  -d '{"customerName":"John Doe", "product":"Laptop", "quantity":1}'
  ```

### Update an Order

- **URL**: `/orders/{id}`
- **Method**: `PUT`
- **Request Body**: JSON object with updated order details
- **Response**: The updated order
- **Example**:
  ```bash
  curl -X PUT http://localhost:8080/orders/1 \
  -H 'Content-Type: application/json' \
  -d '{"customerName":"Jane Doe", "product":"Tablet", "quantity":2}'
  ```

### Delete an Order

- **URL**: `/orders/{id}`
- **Method**: `DELETE`
- **Response**: `200 OK` on success
- **Example**:
  ```bash
  curl -X DELETE http://localhost:8080/orders/1
  ```

