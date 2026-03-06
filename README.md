Quiz Application – Microservices Architecture

A Spring Boot Microservices-based Quiz Application that allows users to generate quizzes from stored questions and evaluate results. The system is built using Spring Boot, Spring Cloud, and Microservices architecture for scalability and modularity.

This project demonstrates how multiple services communicate using Service Discovery and API Gateway.

🚀 Features

Create and manage questions

Generate quizzes from question database

Submit quiz answers

Evaluate quiz results

Microservices communication

Centralized API Gateway

Service Discovery using Eureka

🏗️ Microservices Architecture

The project contains the following services:

1️⃣ Service Registry (Eureka Server)

Registers all microservices

Helps services discover each other

📁 Folder: service-registry

2️⃣ API Gateway

Single entry point for all client requests

Routes requests to appropriate microservices

📁 Folder: api-gateway

3️⃣ Question Service

Manages all question-related operations.

Functions:

Add questions

Get questions by category

Retrieve random questions for quiz

📁 Folder: question-service

4️⃣ Quiz Service

Handles quiz generation and evaluation.

Functions:

Create quiz

Fetch quiz questions

Submit answers

Calculate score

📁 Folder: quiz-service

🛠️ Technologies Used

Java 17

Spring Boot

Spring Cloud

Spring Data JPA

MySQL

Eureka Service Discovery

Spring Cloud Gateway

Maven

Git & GitHub

📂 Project Structure
quiz-app-microservices
│
├── service-registry        # Eureka Server
├── api-gateway             # API Gateway
├── question-service        # Question Management Service
├── quiz-service            # Quiz Management Service
├── question-table-data.sql # Sample question database
⚙️ How to Run the Project
1️⃣ Clone the repository
git clone https://github.com/your-username/quiz-microservices-app.git
cd quiz-microservices-app
2️⃣ Start Services in Order

Start services in this sequence:

1️⃣ Service Registry

cd service-registry
mvn spring-boot:run

2️⃣ API Gateway

cd api-gateway
mvn spring-boot:run

3️⃣ Question Service

cd question-service
mvn spring-boot:run

4️⃣ Quiz Service

cd quiz-service
mvn spring-boot:run
🌐 Eureka Dashboard

After starting services, open:

http://localhost:8761

You will see all registered services.

🔗 API Endpoints
Question Service

Add Question

POST /question/add

Get Questions by Category

GET /question/category/{category}
Quiz Service

Create Quiz

POST /quiz/create

Get Quiz Questions

GET /quiz/get/{quizId}

Submit Quiz

POST /quiz/submit/{quizId}
📊 Database Setup

Create database:

CREATE DATABASE quiz_app;

Import sample questions

Use the file:

question-table-data.sql
📷 Architecture Diagram

Client → API Gateway → Microservices
↓
Service Registry (Eureka)

🎯 Learning Outcomes

This project demonstrates:

Microservices Architecture

Service Discovery using Eureka

API Gateway Routing

Inter-service communication

REST API development with Spring Boot

👨‍💻 Author

Piyush Choudhary
B.Tech CSE – Vignan's Foundation for Science, Technology and Research
