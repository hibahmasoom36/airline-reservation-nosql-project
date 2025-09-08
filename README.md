# Airline Reservation System — NoSQL Project

## 📌 Overview
This project was completed as part of **DSE6210: Big Data SQL and NoSQL**.  
It explores how an airline reservation system can be modeled using **NoSQL (MongoDB)** compared to a traditional **relational database (PostgreSQL)**, and discusses tradeoffs between flexibility, scalability, and consistency.

## 🎯 Objectives
- Represent airline reservation data in **JSON document format**.  
- Compare relational and document-oriented models for the same system.  
- Evaluate the advantages and disadvantages of MongoDB in this use case.  
- Propose a **hybrid solution** that balances scalability with transactional reliability.  

## 🗂️ Deliverables
- **JSON Model (`json-model.json`)** — airline reservation captured in a single NoSQL-style document.  
- **Final Project Paper (`final-project-paper.pdf`)** — written analysis on RDBMS vs. MongoDB tradeoffs.  

## 🛠️ Key Insights
- MongoDB reduces join complexity and enables **faster queries** for read-heavy workloads.  
- Schema-less design allows for **flexible evolution** as flight and reservation data changes.  
- Horizontal scaling via **sharding** supports high volumes of bookings and real-time updates.  
- Drawbacks: potential **data redundancy** and weaker **transactional guarantees** compared to RDBMS.  
- A **hybrid model** — MongoDB for flexible data and PostgreSQL for strict transactions — provides an optimal balance for large-scale airline systems.  

## 📊 JSON Data Example
The reservation data includes:
- Flight details (number, airline, aircraft type, schedule).  
- Multi-leg itinerary.  
- Passenger and contact details.  
- Reservation status, ticket type, travel class.  
- Payment status and amount.  

```json
{
    "flight_number": "FL123",
    "airline_code": "FA",
    "aircraft_type": "Jet",
    "origin": {
        "airport_code": "A1",
        "airport_name": "Alpha Airport",
        "location": "City A"
    },
    "destination": {
        "airport_code": "B2",
        "airport_name": "Beta Airport",
        "location": "City B"
    },
    "departure_date_time": "2024-12-01T08:00:00Z",
    "arrival_date_time": "2024-12-01T11:00:00Z",
    "reservations": [
        {
            "reservation_id": 1,
            "passenger": {
                "passenger_id": 101,
                "first_name": "Alice",
                "last_name": "Smith"
            },
            "reservation_status": "confirmed",
            "travel_class": "economy",
            "payment": {
                "status": "paid",
                "amount": 200.00
            }
        }
    ]
}

```
## 📂 Repo Structure
/README.md

/json-model.json

/final-project-paper.pdf

## 🔮 Next Steps
- Expand the **JSON schema** with complex itineraries and loyalty program data.  
- Test MongoDB Atlas queries against **Postgres joins** to measure tradeoffs.  
- Prototype a **hybrid design**: MongoDB for flexibility + PostgreSQL for transactions. 
