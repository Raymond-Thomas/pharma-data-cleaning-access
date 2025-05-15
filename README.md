# Pharmacy Patient and Medication Data Cleaning & Management Project

## Project Overview
This project focuses on cleaning and preparing pharmacy patient and medication datasets for relational database management and reporting. Using Excel, I removed invalid characters, standardized data formats, and ensured data quality. The cleaned data was imported into Microsoft Access, where I designed relational tables, created queries to analyze patient-medication relationships, and generated reports simulating real-world pharmacy data workflows.

> Note: The Microsoft Access `.accdb` file is not included in this repository. Screenshots, cleaned datasets, and SQL queries are provided to demonstrate the project work.

## Project Status
This project is an initial demonstration of my skills in data cleaning, database management, and reporting using Excel and Access. It is currently a basic example and will be expanded upon to include additional datasets, more complex queries, and advanced reporting features as I continue to develop the project.

## Tools Used
- Microsoft Excel 2021
- Microsoft Access 2021
- SQL (Access SQL dialect)

## Skills Demonstrated
- Data Cleaning and Standardization
- Relational Database Design (Patients → Medications)
- Query Writing (e.g., Medications per Patient, Total Medication Cost)
- Data Analysis and Reporting

## Key Tasks Completed
- Cleaned `patients.csv` and `medications.csv` by removing invalid characters and ensuring data integrity.
- Designed relational tables in Access with enforced relationships between patients and medications.
- Created SQL queries to analyze medication usage and costs by patient.
- Generated screenshots of the database relationships, queries, and reports.

## Project Files
- `/patients.csv` — Cleaned patient dataset.
- `/medications.csv` — Cleaned medication dataset.
- `/screenshots/` — Screenshots of database structure, queries, and results.
- `/queries/` — Sample Access SQL queries.

## Example Queries
```sql
SELECT p.FIRST & ' ' & p.LAST AS PatientName, COUNT(m.CODE) AS MedCount
FROM Patients p
INNER JOIN Medications m ON p.Id = m.PATIENT
GROUP BY p.FIRST, p.LAST;
