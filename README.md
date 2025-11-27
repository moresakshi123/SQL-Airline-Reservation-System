# SQL-Airline-Reservation-System(Indigo)
Designed an Airline Reservation System using SQL with tables for flights, customers, bookings, and payments, along with queries for searching, reserving, and managing reservations.

# SQL Project: Airline Reservation System(2022-24 Indigo Airlines)
## 📌 Project Overview
This SQL project focuses on designing and analyzing an *Airline Reservation System* database.  
The goal is to manage flight schedules, passengers, bookings, payments, and reservations through efficient SQL queries.

The project demonstrates:
- Database creation
- Table design with relationships
- Insert operations
- Querying real-world airline scenarios

## 🧰 Tools & Technologies Used
- MySQL / SQL Server / MySQL Workbench
- SQL Workbench / VS Code
- CSV/Excel datasets (if used)

## 🗂 Files Included
- Airline Reservation System (ppt)
- ER Diagram
- README.md – Documentation

---

## 📂 Database Structure

### ✔ *Main Tables*
- *Passengers* – Stores passenger details  
- *Employees* – Information on 
- *Airports* – List of airports operating ,flights, routes, timings  
- *Reservations* – Booking details  
- *Review* – Comments,Rating

---

## 🧮 SQL Concepts Used
- Database creation & table design  
- PRIMARY KEY & FOREIGN KEY  
- JOINS (INNER, LEFT, RIGHT)  
- GROUP BY / HAVING  
- Subqueries  
- Views  
- Constraints (NOT NULL, UNIQUE)  
- Aggregate functions (COUNT, SUM, AVG)

---

## 📝 Sample SQL Queries

### ▶ 1. List all flights between two cities
SELECT flight_id, airline_name, departure_time, arrival_time 
FROM flights
WHERE source = 'Mumbai' AND destination = 'Delhi';

▶2. Find total number of passengers booked on each flight

SELECT flight_id, COUNT(passenger_id) AS total_passengers
FROM reservations
GROUP BY flight_id;

▶ 3. Get revenue generated per flight

SELECT r.flight_id, SUM(p.amount) AS total_revenue
FROM payments p
JOIN reservations r ON p.reservation_id = r.reservation_id
GROUP BY r.flight_id;

▶ 4. Show all upcoming flights scheduled today

SELECT flight_id, airline_name, departure_time
FROM flights
WHERE departure_date = CURDATE();



📈 Findings / Insights

Popular travel routes

High-demand travel hours

Airline with maximum bookings

Revenue comparison across flights

Passenger booking patterns



---

🧠 Skills Demonstrated

Designing a relational database

Writing optimized SQL queries

Applying normalization

Solving real-world business problems

Analytical thinking and data interpretation



---

📝 Conclusion

The Airline Reservation System SQL Project provides a complete end-to-end solution for managing flight data, passenger records, reservations, and payments. It demonstrates efficient use of SQL for real-world applications such as booking systems, travel analytics, and airline operations.


