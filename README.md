# Airline Reservation System — NoSQL Project

## 📌 Overview
This project compares relational (PostgreSQL) vs. NoSQL (MongoDB) approaches for modeling and scaling an airline reservation system.

## 🎯 Objectives
- Represent airline reservation data in JSON document format.  
- Analyze the strengths and weaknesses of MongoDB vs. PostgreSQL.  
- Discuss tradeoffs and propose a hybrid solution for scalability + consistency.  

## 🗂️ Deliverables
- **JSON Model (`json-model.json`)** — a single document capturing flight, passenger, reservation, and payment data.  
- **Final Project Paper (`final-project-paper.pdf`)** — analysis of MongoDB features, limitations, and hybrid strategies.  

## 🛠️ Key Insights
- MongoDB reduces join complexity and supports flexible schema evolution.  
- Schema-less design enables rapid scaling via sharding.  
- Challenges include **redundancy** and **transactional consistency**.  
- A **hybrid model** (MongoDB + RDBMS) provides the best balance for airline systems. 
