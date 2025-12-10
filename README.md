📘 Marks_Analysis 

Using MySQL to analyze student performance using the Students Performance dataset. 
This project demonstrates how to import CSV data into a relational database, document data types, and perform analytical SQL queries. 

Shape 

📂 Repository Structure 

File 

Description 

StudentsPerformance.csv 

The dataset containing all student records. 

MySQL week 1.sql 

SQL script for creating tables, loading data, and running analysis queries. 

README.md 

Documentation for the project. 

Shape 

🧑‍🏫 Project Overview 

This project analyzes student performance based on demographic attributes and exam scores in Math, Reading, and Writing. The goal is to explore how different factors influence academic outcomes using SQL. 

This is ideal for: 

Learning SQL data-analysis workflows 

Understanding dataset documentation best practices 

Practicing data cleaning, transformation, and exploration 

Shape 

📊 Dataset Description 

The dataset (StudentsPerformance.csv) contains several attributes describing students’ backgrounds and their exam results. 

Below is the data dictionary (data types + description + characteristics). 

Shape 

🗂️ Data Types & Characteristics 

🎯 Student Performance Dataset – Data Dictionary 

Column Name 

Column Name 

Description 

Characteristics 

gender 

VARCHAR(20) 

Student’s gender 

Categorical, typically “male” or “female” 

race/ethnicity 

VARCHAR(50) 

Group identifier for demographic category 

Categorical (Group A–E) 

parental level of education 

VARCHAR(100) 

Highest education level achieved by parents 

Categorical (bachelor’s, some college, high school, etc.) 

lunch 

VARCHAR(50) 

Type of lunch the student receives 

Categorical (“standard”, “free/reduced”) 

test preparation course 

VARCHAR(50) 

Whether student completed prep course 

Categorical (“completed”, “none”) 

math score 

INT 

Math exam score (0–100) 

Numerical, discrete 

reading score 

INT 

Reading exam score (0–100) 

Numerical, discrete 

writing score 

INT 

Writing exam score (0–100) 

Numerical, discrete 

average_score 

DECIMAL(5,2) 

Average of the three exam scores 

Numeric, calculated field 

pass_fail 

VARCHAR(10) 

Performance classification 

Categorical (“Pass”, “Fail”) 

math 

DECIMAL(5,2) 

Standardized math score 

Numeric, derived 

reading_z (if added) 

DECIMAL(5,2) 

Standardized reading score 

Numeric, derived 

writing_z (if added) 

DECIMAL(5,2) 

Standardized writing score 

Numeric, derived 

Shape 

📥 Importing the Dataset (MySQL Setup) 

Clone the repository: 

git clone https://github.com/Insightful-squard-Capaciti-for-Data/Marks_Analysis.git 

Open MySQL Workbench or your preferred SQL client. 

Run the script: 
MySQL week 1.sql 

Load data from StudentsPerformance.csv into your table. 

Validate insert: 

SELECT COUNT(*) FROM studentsperformance; 

Shape 

🔎 Example Analysis Queries 

-- Average score by gender 

SELECT gender, AVG(average_score)  

FROM studentsperformance  

GROUP BY gender; 

 

-- Performance impact of test prep course 

SELECT `test preparation course`, AVG(average_score) 

FROM studentsperformance 

GROUP BY `test preparation course`; 

 

-- Students who failed math 

SELECT * FROM studentsperformance 

WHERE `math score` < 50; 

Shape 

🚀 Why This Project Is Useful 

Teaches how to document datasets correctly 

Shows real SQL workflows used in analytics 

Helps build data literacy and exploratory analysis skills 

Can be expanded to dashboards or predictive modeling 

Shape 

🔧 Future Enhancements 

Add ERD (Entity-Relationship Diagram) 

Add Python notebook for visual analysis 

Create derived metrics (overall pass rate, subject pass rate) 

Implement MySQL stored procedures for automated insights 

Shape 

👥 Contributors 

Insightful Squad – Capaciti Data Programme Project Team 
