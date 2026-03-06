# HBnB Project – Initial Setup

## Overview

HBnB is a simplified backend application inspired by Airbnb.
The goal of this project is to design a **modular backend architecture** using **Flask**, while applying important software design principles such as **layered architecture** and the **Facade design pattern**.

At this stage of the project, the focus is on setting up a **clean project structure**, implementing an **in-memory repository**, and preparing the application for future expansion.

The application is divided into three main layers:

* **Presentation Layer** – Handles API endpoints and client communication.
* **Business Logic Layer** – Contains the core logic of the application.
* **Persistence Layer** – Responsible for storing and retrieving data.

Currently, the project uses an **in-memory repository**, which will later be replaced with a **database solution using SQLAlchemy**.

---

## Project Structure

```
hbnb/
├── app/
│   ├── __init__.py
│   ├── api/
│   │   ├── __init__.py
│   │   ├── v1/
│   │       ├── __init__.py
│   │       ├── users.py
│   │       ├── places.py
│   │       ├── reviews.py
│   │       ├── amenities.py
│   ├── models/
│   │   ├── __init__.py
│   │   ├── user.py
│   │   ├── place.py
│   │   ├── review.py
│   │   ├── amenity.py
│   ├── services/
│   │   ├── __init__.py
│   │   ├── facade.py
│   ├── persistence/
│       ├── __init__.py
│       ├── repository.py
├── run.py
├── config.py
├── requirements.txt
└── README.md
```

---

## Directory and File Description

### app/

Contains the main application code.

### api/

Handles the **API endpoints** that clients interact with.

### api/v1/

Contains version 1 of the API routes for:

* Users
* Places
* Reviews
* Amenities

### models/

Contains the **business logic classes** that represent core entities of the system such as:

* User
* Place
* Review
* Amenity

### services/

Implements the **Facade pattern**, which simplifies communication between the API layer and the persistence layer.

### persistence/

Contains the **repository implementation** used to store and manage application data.

Currently, the project uses an **InMemoryRepository**, which stores objects in memory using a Python dictionary.

In later stages, this will be replaced with a **database-backed repository using SQLAlchemy**.

### run.py

Entry point of the application.
It creates and runs the Flask application.

### config.py

Handles application configuration such as:

* Secret keys
* Debug mode
* Environment settings

### requirements.txt

Lists the Python dependencies required for the project.

---

## Installation

Clone the repository and navigate to the project directory:

```
git clone <repository_url>
cd hbnb
```

Install the required dependencies:

```
pip install -r requirements.txt
```

---

## Running the Application

To start the Flask application, run:

```
python3 run.py
```

The server will start at:

```
http://127.0.0.1:5000
```

Since the API endpoints are not implemented yet, you may see a **404 response**, which is expected at this stage.

---

## Current Implementation

At this stage, the project includes:

* Project structure setup
* Flask application initialization
* In-memory repository implementation
* Facade pattern structure
* Basic configuration setup

API endpoints and database integration will be implemented in later tasks.

---

## Technologies Used

* Python
* Flask
* Flask-RESTX

---

## Future Improvements

In the next stages of the project, the following features will be added:

* Complete API endpoints
* Data validation
* Database integration with SQLAlchemy
* Authentication and authorization
* Full CRUD operations for all entities

