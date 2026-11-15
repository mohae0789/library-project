# 📚 Library Management System \- Microservices Architecture

> **Faculty of Computers & Artificial Intelligence \- Software Engineering-2 Project**  
> **Capital University**

---

## 📋 Overview

A complete **Library Management System** built using a **Spring Boot Microservices Architecture**. The system implements real-world business rules, role-based access control, service discovery, API routing, aspect-oriented programming (AOP), and containerization using Docker.

---

## 🏗️ System Architecture & Services

The project is divided into the following components and microservices:

| Service / Component | Description | Default Port | Swagger UI / Dashboard Link |
| :---- | :---- | :---: | :---- |
| **Eureka Server** | Service discovery and registration center | `8761` | `http://localhost:8761` |
| **API Gateway** | Single entry point for all client requests (`lb://`) | `8080` | \- |
| **Members Service** | User management, authentication (JWT), and roles | `8081` | `http://localhost:8081/swagger-ui.html` |
| **Books Service** | Book catalog, categories, and inventory management | `8082` | `http://localhost:8082/swagger-ui.html` |
| **Loans Service** | Book borrowing/returning and business rules validation | `8083` | `http://localhost:8083/swagger-ui.html` |
| **Fines Service** | Late return penalties calculation and AOP logging | `8084` | `http://localhost:8084/swagger-ui.html` |
| **Frontend App** | Web client (HTML/CSS/JS) communicating via Gateway | `3000` / `5500` | \- |

---

## 🛠️ Tech Stack

* **Backend:** Java 17+, Spring Boot 3+, Spring Cloud (Eureka, API Gateway, OpenFeign)  
* **Security:** Spring Security, JWT (JSON Web Tokens), BCrypt Password Encoding  
* **Database:** MySQL / PostgreSQL (Database-per-service pattern) with Spring Data JPA  
* **AOP & Docs:** Spring AOP, Springdoc OpenAPI (Swagger UI), Postman Collection  
* **Frontend:** HTML5, CSS3, JavaScript  
* **DevOps & Deployment:** Docker, Docker Compose, Git & GitHub

---

## 📁 Repository Structure

```
my-library-project/
├── frontend/               # Web interface (HTML, CSS, JS)
├── eureka-server/          # Service Registry (Eureka)
├── api-gateway/            # Spring Cloud Gateway
├── members-service/        # Users & Security Microservice
├── books-service/          # Books Inventory Microservice
├── loans-service/          # Borrowing & Business Rules Microservice
├── fines-service/          # Penalties & AOP Microservice
├── docs/                   # SRS, UML Diagrams, OCL Constraints, Postman JSON
├── docker-compose.yml      # Multi-container Docker orchestration
└── README.md               # Project documentation
```

---

## 🚀 How to Run the Project

### Prerequisites

* Java 17 or higher  
* Maven or Gradle  
* Docker & Docker Compose installed

### Running via Docker Compose (Recommended)

1. Clone the repository:

```sh
git clone https://github.com/your-username/library-microservices-project.git
cd library-microservices-project
```

2. Build and start all services and databases:

```sh
docker compose up --build -d
```

3. Verify that all microservices are registered on the **Eureka Dashboard**:  
   * Open `http://localhost:8761` in your browser.

---

## 📄 Documentation & Testing

* **SRS & Diagrams:** Located in the `/docs` folder (Use Case, ERD, Class, Sequence, Activity, and Architecture diagrams).  
* **API Testing:** Import `docs/postman-collection.json` into Postman. Make sure to configure the `baseUrl` (`http://localhost:8080`) and `token` variables.

---

## 👥 Team Members & Roles

* **Team Number:** \[Insert Team Number\]  
1. **\[Member 1 Name\]** \- ID: `[ID]` \- *Documentation, SRS, Diagrams & OCL*  
2. **\[Member 2 Name\]** \- ID: `[ID]` \- *Infrastructure (Eureka Server & API Gateway)*  
3. **\[Member 3 Name\]** \- ID: `[ID]` \- *Members Service & Spring Security (JWT)*  
4. **\[Member 4 Name\]** \- ID: `[ID]` \- *Books Service & Swagger Documentation*  
5. **\[Member 5 Name\]** \- ID: `[ID]` \- *Loans Service, Business Rules & OpenFeign*  
6. **\[Member 6 Name\]** \- ID: `[ID]` \- *Fines Service, Spring AOP, Docker & Frontend*