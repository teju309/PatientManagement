# Patient Management System – Microservices Architecture

This project is a **production-grade microservices system** built step by step with **Spring Boot, gRPC, Kafka, Docker, API Gateway, Authentication, Testing, and AWS CloudFormation (IaC)**.  
It demonstrates how to design and deploy scalable, secure, and event-driven systems.

---

## 📚 Table of Contents
- [Introduction](#introduction)
- [Architecture](#architecture)
- [Tech Stack](#tech-stack)
- [Services](#services)
  
---

## 🚀 Introduction
This repository contains a **full-stack microservices project** that simulates a patient management workflow.  
It covers REST APIs, gRPC communication, Kafka event streaming, authentication with JWT, integration testing, and deployment to AWS (via LocalStack & CloudFormation).

---

## 🏗️ Architecture
The system consists of the following services:

- **Patient Service** – Core service for managing patients (CRUD operations).
- **Billing Service** – gRPC-based service for handling billing logic.
- **Analytics Service** – Consumes Kafka patient events for analytics.
- **Auth Service** – JWT-based authentication and authorization.
- **API Gateway** – Single entry point with request routing, filtering, and token validation.

All services are containerized with **Docker**, orchestrated with **ECS**, and integrated with **MSK (Kafka)**.

---

## ⚙️ Tech Stack
- **Backend:** Java, Spring Boot, gRPC
- **Data Layer:** PostgreSQL, JPA/Hibernate, In-Memory DB (for testing)
- **Event Streaming:** Apache Kafka (MSK on AWS)
- **Authentication:** Spring Security, JWT
- **Infrastructure:** Docker, AWS LocalStack, CloudFormation, ECS, VPC
- **Testing:** JUnit, Integration Testing
- **CI/CD Ready:** Dockerized builds and IaC deployment scripts

---

## 🧩 Services
1. **Patient Service**
   - REST APIs for patient management
   - gRPC client to Billing Service
   - Kafka producer for patient events

2. **Billing Service**
   - gRPC server handling billing requests

3. **Analytics Service**
   - Kafka consumer for patient events
   - Generates insights

4. **Auth Service**
   - User management
   - JWT authentication and validation

5. **API Gateway**
   - Routes requests to services
   - Applies JWT validation filter
   - Serves OpenAPI docs via gateway

---
