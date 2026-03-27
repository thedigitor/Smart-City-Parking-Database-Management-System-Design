# Smart City Parking Database Management System Design
## Improving Operational Efficiency in CityPark’s Current Manual Parking System with a Scalable Data Solution
### SQL Database Design Project Report
## Project Overview
The Smart City Parking Database Management System was designed to solve inefficiencies in CityPark’s current manual parking system. The existing paper-based approach made it difficult to track parking availability, calculate fees accurately, and analyze customer behavior.

This project introduces a structured relational database system that automates parking operations, improves data accuracy, and enables better decision-making.

|Attribute  |  Detail |
|------|--------|
|Project Title  |  Smart City Parking Database Management System|
|Database Type |  Relational Database (SQL)|
|Normalization Level  |  Third Normal Form (3NF)|
|Total Entities |   8 Core Entities|
|Total Relationships  |9 Foreign Key Relationships|
|Deliverables  |   ERD, DDL Scripts, DML Scripts, Business Rules, Use Cases|

## Business Context
Before any database design was undertaken, a thorough review of CityPark's business requirements was conducted
### Problem Statement
CityPark faced five critical operational challenges with its paper-based system:
* No real-time visibility into available parking spaces across city lots
* Inability to track customer parking history and duration
* Manual fee calculation leading to billing errors and revenue leakage
* No infrastructure to support repeat-customer recognition or membership programs
* No data for identifying high-demand lots to optimize operations

This database design directly addresses each of these pain points through structured data modeling, automated calculations, and well-defined relationships between entities.

### Objectives
The database management system was designed to:
* Store and manage customer and vehicle data
* Track parking sessions from entry to exit
* Automatically calculate parking fees
* Support membership plans with discounts
* Provide structured data for reporting and analytics
