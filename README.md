# Microservices Hands-On Session

## Overview
This project sets up a **Spring Boot microservices architecture** using **Eureka for service discovery** and **API Gateway for routing**.

## Prerequisites
- Java 17+ installed
- Maven installed

## Steps to Run

### 1. Start Eureka Server
```sh
cd eureka-server
mvn spring-boot:run
```

### 2. Start API Gateway
```sh
cd api-gateway
mvn spring-boot:run
```

### 3. Start Microservices
```sh
cd service-a
mvn spring-boot:run

cd service-b
mvn spring-boot:run
```

### 4. Test Microservices via API Gateway

- **Service A:** `http://localhost:8080/service-a/message`  
- **Service B:** `http://localhost:8080/service-b/message`  

You should see responses:  
- `"Hello from Service A"`  
- `"Hello from Service B"`  

## Next Steps
- Extend this setup with authentication (OAuth2, JWT).
- Add a database connection using PostgreSQL or MySQL.
- Implement resilience patterns like Circuit Breaker.
