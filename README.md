# 🍔 Burger App: Document Database API (Phase 1 of NoSQL Series)

## 📌 Project Overview
This repository is the first phase of a larger Data Engineering and Backend portfolio series demonstrating **Polyglot Persistence**. 

This specific project focuses on **Document-based NoSQL Databases** using **MongoDB** integrated with **FastAPI**. It serves as the core Data Store API to manage flexible, hierarchical data like burger menus, complex ingredients, and pricing, while enforcing strict application-level data validation.

## 🗺️ The Polyglot Data Ecosystem Roadmap
To build a highly scalable Burger Recommendation System, the architecture is divided into the following phases:
1. 🟢 **Phase 1: Document DB** (This Repo - MongoDB + FastAPI for core catalog and menus).
2. ⏳ **Phase 2: Key-Value DB** (Redis for shopping carts and sessions).
3. ⏳ **Phase 3: Wide-Column DB** (Cassandra for user activity tracking).
4. ⏳ **Phase 4: Graph DB** (Neo4j for AI recommendation engine).
5. ⏳ **Phase 5: The Integrator** (Orchestrating the databases together).

## 🏗️ Project Architecture (Modular Design)
The code is structured into a modular Python application following software engineering best practices:
* `database.py`: Handles secure connection, timeouts, and authentication with MongoDB using `.env`.
* `models.py`: Defines strict data validation schemas using Pydantic (Application-Level Validation) to ensure data integrity before insertion.
* `main.py`: The FastAPI application acting as the controller, defining the endpoints (Routing) to handle client requests and execute MQL operations.

## 🛠️ Tech Stack
* **Database:** MongoDB (Local / Atlas)
* **Framework:** FastAPI
* **Language:** Python 3
* **Libraries:** `pymongo`, `pydantic`, `uvicorn`, `python-dotenv`

## 🚀 Setup & Installation
1. Clone the repository:
   ```bash
   git clone [https://github.com/hazemmagdy12/fastapi-mongodb-burger-api.git](https://github.com/hazemmagdy12/fastapi-mongodb-burger-api.git)
   cd fastapi-mongodb-burger-api

  python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
pip install fastapi uvicorn pymongo python-dotenv pydantic

MONGO_URI="mongodb://127.0.0.1:27017/"

uvicorn main:app --reload
[http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)
