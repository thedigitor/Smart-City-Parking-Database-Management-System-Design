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

## Database Entities & Attributes
The Smart City Parking Management System database is built around 8 core entities. Each entity was designed to capture a distinct real-world concept in the parking workflow: from the customer registering through to payment and membership benefits.

1. Customer: Individual using parking services 
2. Vehicle: Vehicle owned by a customer 
3. ParkingLot: Physical parking location 
4. ParkingSpace: Individual parking space inside a lot 
5. ParkingSession: One instance of parking (entry → exit) 
6. MembershipPlan: Subscription plans offered 
7. Payment: Payment made for a parking session 
8. CustomerMembership: Links customers to membership plans

These entities represent the full parking lifecycle from registration to payment and membership benefits.

## Entity Relationships & Cardinalities
The following table describes every relationship in the database, including cardinality, the foreign key column, and the business rule it enforces.

|Relationship  | Type | Business Rule|
|--------|------|------|
|Customer → Vehicle  | One-to-Many (1:M)  |   One customer can own many vehicles; every vehicle must have an owner|
|ParkingLot → ParkingSpace |  One-to-Many (1:M)   |  One lot contains many spaces; every space belongs to exactly one lot|
|Customer → ParkingSession | One-to-Many (1:M) |  One customer can have many sessions; every session must link to a customer|
|Vehicle → ParkingSession |   One-to-Many (1:M) |  One vehicle can appear in many sessions; every session must identify the vehicle|
|ParkingSpace → ParkingSession  |  One-to-Many (1:M)  | One space can be used in many sessions (at different times)|
|Customer → MembershipPlan |  One-to-Many (1:M) |  A customer can subscribe to different plans; a plan must belong to one customer|
|ParkingSession → Payment| One-to-Many (1:M)  |One session can have one or more payment records|
|Customer → CustomerMembership  | One-to-Many (1:M)  | One customer can hold multiple memberships over time|
|MembershipPlan → CustomerMembership  |  One-to-Many (1:M) |  One plan can be subscribed to by many customers|
