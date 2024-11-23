# FitPro Gym SQL Project

![Project Image Placeholder](https://github.com/sureka2003/Fitpro/blob/main/Fitpro_logo.png) 


Welcome to my first SQL project, where I perform an in-depth analysis of real-time data from **FitPro Gym**. Utilizing a dataset of **10,000 visit records**, this project examines gym membership trends and customer visit patterns to address critical business questions. The insights generated aim to help the fitness center gain a deeper understanding of its customer base better , enabling data-driven strategies to enhance service delivery and operational efficiency.

## Table of Contents
- [Introduction](#introduction)
- [Project Structure](#project-structure)
- [Database Schema](#database-schema)
- [Business Problems](#business-problems)
- [SQL Queries & Analysis](#sql-queries--analysis)
- [Getting Started](#getting-started)
- [Questions & Feedback](#questions--feedback)
- [Contact Me](#contact-me)

---

## Introduction

This project showcases core SQL competencies through the analysis of a dataset from FitPro Gym. By leveraging SQL, I examined membership information, customer demographics, and visit patterns to uncover actionable insights. The analysis highlights key SQL techniques, such as **table creation, data querying, and in-depth data analysis**, demonstrating the practical application of foundational SQL skills in a real-world context.

## Project Structure

1. **SQL Scripts**: Includes scripts for creating the database schema and executing queries for analysis.
2. **Dataset**:  Contains real-time data on gym visits, memberships, and member demographics.
3. **Analysis**:  A series of SQL queries designed to address key business questions, providing targeted solutions to practical challenges.

---

## Database Schema

Here’s an overview of the database structure:

### 1. **Members Table**
- **member_id**: Unique identifier for each member
- **name**: Name of the member

### 2. **Memberships Table**
- **member_id**: Unique identifier linked to the `members` table
- **age**: Age of the member
- **gender**: Gender of the member ('M' or 'F')
- **membership_type**: Type of membership (e.g., Monthly, Quarterly)
- **join_date**: Date when the member joined
- **status**: Membership status (e.g., Active, Cancelled)

### 3. **Visits Table**
- **visit_id**: Unique identifier for each visit
- **member_id**: Linked to the `members` table
- **visit_date**: Date of the visit
- **check_in_time**: Check-in time of the visit
- **check_out_time**: Check-out time of the visit

## Business Problems

The following queries were created to solve specific business questions. Each query is designed to provide insights based on gym membership and visit data.

1. Retrieve the **name** and **membership_type** of female members.
2. Find members who have a **Monthly membership** and joined after **2023-11-01**.
3. List the **name** and **status** of active members over **25**.
4. Get details of **visits** on a specific date (**2024-01-01**).
5. List members with a **Quarterly membership** aged between **20 and 30**.

### Additional Aggregations and Grouping

1. Count the total visits made by each member.  
2. Count members by membership type (e.g., Monthly, Weekly, Quarterly).  
3. Calculate the average age of members, grouped by membership type.  
4. Calculate total visits for each visit date.  
5. Count members by status (e.g., Active or Cancelled).  

### Advanced Queries

6. Identify the top 3 members with the highest visits.  
7. List active monthly members grouped by membership type, sorted by recent join dates.  
8. Retrieve members with more than 2 visits, sorted by total visits, displaying the top 5.  
9. Identify members who joined in 2023, grouped by membership type (with each group having >1 member).  
10. Calculate the average age of active members, grouped by membership type, limited to the top 3 results.


---

## SQL Queries & Analysis

The `analysis.sql` file contains all SQL queries developed for this project. Each query corresponds to a business problem and demonstrates skills in SQL syntax, data filtering, aggregation, grouping, and ordering.

## Getting Started

### Prerequisites
- PostgreSQL (or any SQL-compatible database)
- Basic understanding of SQL

### Steps
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/fitpro-gym-sql-project.git
   ```
2. **Set Up the Database**:
   - Run the `schema.sql` script to set up tables and insert sample data.

3. **Run Queries**:
   - Execute each query in `analysis.sql` to explore and analyze the data.

---

## Questions & Feedback

If you have any questions or feedback, feel free to create an issue or reach out!

---

## Contact Me

📄 **[Resume](#)**  
📧**[Email](mailto:surekafathimasf2003@gmail.com)**
📞 **Phone**: +91 82481 25454

--
