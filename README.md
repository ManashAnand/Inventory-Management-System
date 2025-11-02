# 🧾 Inventory Management System (Node.js + Kafka)

## 📘 Overview
This project is a beginner-friendly Proof of Concept (POC) for an **Inventory Management System**, built using **Node.js**, **Kafka**, and **MySQL**.  
It demonstrates how to design scalable, event-driven systems with asynchronous communication and modular microservices.

The main goal is to understand service separation, data flow, and backend system design before implementation.

---

## 🚀 Features
- **Microservices Architecture** — Independent services for Product and Order management.  
- **RESTful APIs** — Built with Express.js for efficient communication between services.  
- **Database Integration** — Persistent storage using MySQL with Sequelize ORM.  
- **Asynchronous Messaging** — Real-time event updates using Apache Kafka.  
- **Containerization** — Each service containerized with Docker for easy deployment and scalability.  
- **Design-First Approach** — Planned data flow and sequence diagrams before coding for better system design.

---

## 🧩 System Workflow
1. **Order Placement** — Users place orders containing one or more products.  
2. **Stock Verification** — Product Service checks product availability in real-time.  
3. **Event Publishing** — Order Service emits Kafka events (`order_placed`, `out_of_stock`).  
4. **Inventory Update** — Product Service listens to Kafka topics and updates stock asynchronously.  
5. **Order Status Update** — Users receive order confirmations and stock updates immediately.

---

## 🧠 Key Components

### 🧾 Order Service
- Handles incoming order requests.  
- Publishes events to Kafka after successful or failed order placement.  
- Ensures data integrity between order and product services.

### 📦 Product Service
- Manages inventory and product data.  
- Listens to Kafka events to handle stock changes.  
- Syncs product availability dynamically across services.

### ⚙️ Kafka Integration
- Enables asynchronous, fault-tolerant message passing.  
- Improves scalability and decouples services for independent scaling.  

---

## 🧰 Technologies Used
**Backend:** Node.js, Express.js, Kafka, Sequelize  
**Database:** MySQL  
**Containerization:** Docker  
**Tools:** Postman (API Testing), Docker Compose (Orchestration)

---

## 🧱 Architecture Diagram
Below is the high-level architecture representing event flow and service communication.

![Architecture Diagram]<img width="1100" height="624" alt="image" src="https://github.com/user-attachments/assets/1e505f00-e889-4a15-9c5a-bcc4e1520a59" />


---

## 🧵 Sequence Diagram
This sequence diagram shows the step-by-step communication between microservices through Kafka events.

![Sequence Diagram]

<img width="1100" height="760" alt="image" src="https://github.com/user-attachments/assets/a3eb28ac-3740-42d6-bc4b-d5afd7615cfe" />
---

## 🎯 Project Goals
- Understand microservice architecture and modular service design.  
- Learn asynchronous communication using Kafka.  
- Practice event-driven programming and fault-tolerant systems.  
- Improve backend design and documentation before coding.

---

## 🧩 Folder Structure
