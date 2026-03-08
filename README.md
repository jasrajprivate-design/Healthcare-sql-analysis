Healthcare Data Analysis Using SQL
Project Overview

This project demonstrates basic SQL data analysis using a healthcare dataset.
The goal of the project is to store patient data in a SQL database and perform queries to extract meaningful insights such as disease distribution, patient demographics, and city-wise patient counts.

Tools Used

Microsoft SQL Server

SQL Server Management Studio (SSMS)

GitHub for project documentation

Dataset Description

The dataset contains sample healthcare records with the following fields:

PatientID

PatientName

Age

City

Disease

This dataset simulates patient data that could be used by healthcare organizations for analysis and reporting.

SQL Operations Performed
1. View Entire Dataset

Displayed all patient records from the table.

SELECT * FROM Patients;
2. Filter Patients with Diabetes

Identified patients diagnosed with Diabetes.

SELECT PatientName, Age, Disease
FROM Patients
WHERE Disease = 'Diabetes';
3. Find Patients Older Than 40

Filtered patient records where age is greater than 40.

SELECT PatientName, Age, Disease
FROM Patients
WHERE Age > 40;
4. City-wise Patient Count

Calculated total patients in each city.

SELECT City, COUNT(*) AS totalPatients
FROM Patients
GROUP BY City
ORDER BY totalPatients DESC;
5. Disease-wise Case Count

Calculated number of cases for each disease.

SELECT Disease, COUNT(*) AS totalCases
FROM Patients
GROUP BY Disease
ORDER BY totalCases DESC;
Key Insights

Diabetes and Asthma appear among the most common diseases in the dataset.

Toronto and Calgary have the highest number of recorded patients.

SQL aggregation functions like COUNT() help summarize healthcare data efficiently.

Skills Demonstrated

Database querying

Data filtering using WHERE

Aggregation using COUNT()

GROUP BY and ORDER BY operations

Basic healthcare data analysis

Author

Jasraj Singh
