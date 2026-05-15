# Airline-Reservation-Management-System-db-basic


## Overview

The Airline Reservation Management System is a professional relational database project developed using SQL and MySQL. The system is designed to manage and simulate real-world airline operations including passenger management, airport administration, aircraft records, flight scheduling, booking and reservation handling, ticket generation, payment processing, boarding pass management, baggage tracking, and employee flight crew assignments.

This project follows Third Normal Form (3NF) normalization principles to reduce data redundancy, maintain relational integrity, improve consistency, and support scalable database operations.

---

# Features

- Passenger Management
- Airport Management
- Aircraft Management
- Flight Scheduling System
- Booking and Reservation Management
- Ticket Generation
- Boarding Pass Management
- Payment Tracking
- Baggage Management
- Employee and Flight Crew Management
- Revenue and Reporting Queries
- Realistic Large Sample Data
- Advanced SQL Queries and Joins
- 3NF Normalized Database Structure

---

# Technologies Used

- MySQL
- SQL
- Relational Database Management System (RDBMS)

---

# Database Structure

The project contains the following tables:

| Table Name | Description |
|------------|-------------|
| Passenger | Stores passenger information |
| Airport | Stores airport details |
| Aircraft | Stores aircraft information |
| Flight | Stores airline flight details |
| Flight_Schedule | Stores flight schedules and timing |
| Booking | Stores booking and reservation records |
| Payment | Stores payment transaction details |
| Ticket | Stores issued ticket information |
| Boarding_Pass | Stores boarding pass records |
| Baggage | Stores baggage details |
| Employee | Stores airline employee information |
| Flight_Crew | Assigns employees to flights |

---

# Database Relationships

- One passenger can have multiple bookings.
- One flight can have multiple schedules.
- One booking can contain payment and ticket information.
- One ticket can generate a boarding pass.
- One booking can contain baggage details.
- One flight can have multiple crew members.
- Flights are connected with airports and aircrafts through foreign key relationships.

---

# Third Normal Form (3NF)

This project is designed according to Third Normal Form (3NF) standards:

- No repeating groups
- No partial dependencies
- No transitive dependencies
- Proper use of primary and foreign keys
- Reduced data redundancy
- Improved consistency and scalability

---

# Project Modules

## 1. Passenger Module
Manages passenger registration and personal information.

## 2. Airport Module
Stores airport names, airport codes, cities, and countries.

## 3. Aircraft Module
Maintains aircraft models, manufacturers, and seating capacity.

## 4. Flight Module
Handles flight details including airline information and flight routes.

## 5. Flight Schedule Module
Stores departure and arrival timings, dates, and flight status.

## 6. Booking Module
Handles reservations, seat allocation, booking class, and booking status.

## 7. Payment Module
Tracks payment methods, payment status, and transaction records.

## 8. Ticketing Module
Generates and manages airline tickets.

## 9. Boarding Pass Module
Stores gate information and boarding status.

## 10. Baggage Module
Manages cabin and checked baggage along with extra baggage fees.

## 11. Employee & Flight Crew Module
Assigns airline staff and crew members to flights.

---

# Advanced SQL Queries Included

The project includes several advanced SQL queries such as:

- Passenger Booking Details
- Flight Route Information
- Total Revenue Calculation
- Passenger Payment Reports
- Flight Crew Information
- Baggage Charges Report
- Available Seats Tracking
- Boarding Status Monitoring
- Flight Status Updates
- Booking Cancellation

These queries demonstrate the practical implementation of joins, aggregate functions, filtering, updates, and relational data retrieval.

---

# Large Sample Data

The database includes extensive realistic sample datasets for:

- Passengers
- Airports
- Aircrafts
- Flights
- Flight Schedules
- Bookings
- Payments
- Tickets
- Boarding Passes
- Baggage
- Employees
- Flight Crew Assignments

This data helps simulate a real-world airline reservation environment for academic and learning purposes.

---

# Installation & Setup

## Step 1: Create Database

Run the following SQL commands:

```sql
CREATE DATABASE Airline_Reservation_System;
USE Airline_Reservation_System;
```

---

## Step 2: Execute Table Creation Queries

Run all `CREATE TABLE` statements to generate the database schema.

---

## Step 3: Insert Sample Data

Run all `INSERT INTO` statements to populate the database with realistic airline records.

---

## Step 4: Execute Queries

Run the provided SQL queries for:

- Reporting
- Revenue analysis
- Booking information
- Flight management
- Passenger tracking
- Operational analysis

---

# Example SQL Query

## Passenger Booking Details

```sql
SELECT
    P.First_Name,
    P.Last_Name,
    F.Flight_Number,
    B.Seat_Number,
    B.Booking_Class,
    B.Booking_Status
FROM Booking B
JOIN Passenger P
ON B.Passenger_ID = P.Passenger_ID
JOIN Flight_Schedule FS
ON B.Schedule_ID = FS.Schedule_ID
JOIN Flight F
ON FS.Flight_ID = F.Flight_ID;
```

---

# Future Enhancements

Possible future improvements include:

- Online Seat Selection System
- Web-Based User Interface
- Admin Dashboard
- Passenger Authentication System
- Mobile Application Integration
- Real-Time Flight Tracking
- Multi-Airline Support
- Cloud Database Deployment
- AI-Based Ticket Price Prediction

---

# Educational Objectives

This project demonstrates:

- SQL Database Design
- Relational Database Modeling
- Database Normalization
- Foreign Key Relationships
- Advanced SQL Query Writing
- Data Integrity Management
- Real-World Airline Management System Design

---

# Project Structure

```text
Airline-Reservation-System/
│
├── database_schema.sql
├── insert_large_data.sql
├── advanced_queries.sql
├── README.md
│
└── screenshots/
```

---

# Author

**Hasnain Chohan**  
Software Development Student

---

# License

This project is developed for educational, academic, and learning purposes.

---
