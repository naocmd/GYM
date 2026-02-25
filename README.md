
# Gym Performance Tracking Database
Project Overview

This project consists of the design and implementation of a relational database to track gym attendance, exercises performed, training volume, and performance metrics.

The objective is to simulate a real-world fitness tracking system and extract meaningful insights using SQL queries.

This project focuses on:

Database modeling

Relational integrity (PK/FK)

Data normalization

Analytical SQL queries

Performance and attendance analysis

# Database Structure

The database is composed of five main tables:

PERSONA

ENTRENAMIENTOS

DETALLE_ENTRENAMIENTO

EJERCICIOS

MUSCULOS

Entity Relationship Model
PERSONA

Stores registered users.

Field	Type	Description
ID_PERSONA	INT (PK)	Unique identifier
NOMBRE	VARCHAR(50)	Person name
GENERO	CHAR(1)	Gender (M/F)

Relationship:

One person can have multiple training sessions.

ENTRENAMIENTOS

Represents each gym attendance record.

Field	Type	Description
ID_ENTRENAMIENTO	INT (PK)	Training session ID
FECHA	DATE	Date of session
DIA_SEMANA	VARCHAR(20)	Day of week
ASISTENCIA	BOOLEAN	Attendance flag
ID_PERSONA	INT (FK)	References PERSONA

Relationship:

Many trainings belong to one person.

DETALLE_ENTRENAMIENTO

Stores exercises performed in each session.

Field	Type	Description
ID_DETALLE	INT (PK)	Detail ID
ID_ENTRENAMIENTO	INT (FK)	References ENTRENAMIENTOS
ID_EJERCICIO	INT (FK)	References EJERCICIOS
PESO	DECIMAL	Weight used
REPETICIONES	INT	Repetitions performed

Relationship:

One training session includes multiple exercises.

EJERCICIOS

Stores available exercises.

Field	Type	Description
ID_EJERCICIO	INT (PK)	Exercise ID
NOMBRE	VARCHAR(50)	Exercise name
DESCANSO	INT	Rest time (minutes)
ID_MUSCULO	INT (FK)	References MUSCULOS

 MUSCULOS

Stores muscle groups.

Field	Type	Description
ID_MUSCULO	INT (PK)	Muscle ID
NOMBRE	VARCHAR(50)	Muscle name

# Relationships Summary

PERSONA 1:N ENTRENAMIENTOS

ENTRENAMIENTOS 1:N DETALLE_ENTRENAMIENTO

EJERCICIOS 1:N DETALLE_ENTRENAMIENTO

MUSCULOS 1:N EJERCICIOS

# Analytical Queries Implemented

The project includes SQL queries designed to answer real-world performance questions such as:

Who lifts the maximum weight?

Most frequently performed exercise

Attendance ranking

Total repetitions per person

Exercise distribution per muscle group

Most active training day

Strongest male and female athlete

Exercise with highest and lowest recorded weight

These queries demonstrate:

JOIN operations (INNER / LEFT)

Aggregations (COUNT, SUM, MAX)

GROUP BY

Subqueries

Ranking logic

# Example Business Insights

Using SQL aggregation and filtering, the system can determine:

Training consistency per user

Strength comparison between athletes

Muscle group distribution

Volume load (weight × reps)

Performance trends

# Future Improvements

Planned upgrades to evolve the project into a production-level model:

Implement N:M relationship between exercises and muscles

Add constraints (NOT NULL, CHECK, UNIQUE)

Add indexing for performance optimization

Implement training volume calculations

Add weekly progression analysis

Automate personalized performance recommendations

# Technologies Used

MySQL

Relational Database Design

SQL (DDL & DML)

Data Aggregation & Analysis

# Purpose of the Project

This project was built to strengthen:

Relational modeling skills

SQL query writing

Analytical thinking

Data interpretation

It simulates a realistic use case in fitness performance tracking and demonstrates the ability to design and query structured relational systems.

# Author

[Naomi Cruz Alcañiz]

Aspiring Data Analyst / Database Developer
Focused on SQL, relational modeling and data-driven insights.
