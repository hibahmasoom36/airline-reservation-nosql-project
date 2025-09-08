# Airline Reservation System — NoSQL Project

## 📌 Overview
This project explores how an airline reservation system can be modeled using **NoSQL (MongoDB)** compared to a traditional **relational database (PostgreSQL)**. It was completed as part of **DSE6210: Big Data SQL and NoSQL**.

## 🎯 Objectives
- Represent airline reservation data in **JSON document format**.  
- Compare relational and document-oriented models for the same system.  
- Evaluate MongoDB’s advantages and disadvantages in this context.  
- Propose a **hybrid approach** balancing scalability and transactional reliability.  

## 🗂️ Deliverables
- `json-model.json` → Airline reservation captured in a single NoSQL-style document.  
- `final-project-paper.pdf` → Analysis of RDBMS vs. MongoDB tradeoffs.  

## 🛠️ Key Insights
- MongoDB reduces join complexity and improves read performance.  
- Schema-less design supports flexible schema evolution.  
- Sharding enables **horizontal scaling** for high booking volumes.  
- Challenges: potential redundancy and weaker **transactional guarantees** compared to RDBMS.  
- A **hybrid model** (MongoDB + PostgreSQL) provides the best of both worlds.  

## 📊 Example: JSON Snippet
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
