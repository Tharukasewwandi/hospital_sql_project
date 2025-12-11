# hospital_sql_project
# 🏥 Hospital Patient Management SQL Project  
A complete SQL project designed to manage hospital patients, visits, doctors, medicines, and revenue analysis.  
This project includes database schema, dummy data, and real-world data analysis queries useful for Data Analyst portfolios.

---

## 📌 Project Overview
This SQL project is built to simulate a simple hospital management system.  
It includes:

- Patient information  
- Visit details  
- Diseases & doctors  
- Medicines per visit  
- Revenue tracking  
- Daily visit trends  
- Common disease identification  
- City & gender insights  

This project is ideal for showcasing SQL skills for a Data Analyst / Data Engineer job.

---

## 📁 Folder Structure
---

## 🗂️ 1. Database Schema (Tables)

### Patients Table
`sql
CREATE TABLE Patients (

  patient_id INT AUTO_INCREMENT PRIMARY KEY,
  
  name VARCHAR(100) NOT NULL,
  
  age INT,
  
  gender VARCHAR(10),
  
  city VARCHAR(100)
  
);

####visits tables


CREATE TABLE Visits (

  visit_id INT AUTO_INCREMENT PRIMARY KEY,
  
  patient_id INT,
  
  visit_date DATE,
  
  disease VARCHAR(100),
  
  doctor VARCHAR(100),
  
  bill_amount DECIMAL(10,2),
  
  FOREIGN KEY (patient_id) REFERENCES Patients(patient_id)
);


###Medicines table

CREATE TABLE Medicines (

  med_id INT AUTO_INCREMENT PRIMARY KEY,
  
  visit_id INT,
  
  medicine_name VARCHAR(100),
  
  qty INT,
  
  FOREIGN KEY (visit_id) REFERENCES Visits(visit_id)
);



🧪 2. Dummy Data (Sample Records)
5 patients

6 visits

Medicines for each visit


All data included in:
dummy_data.sql 


📊 3. Analysis Queries (Insights)
This project includes several real-world analysis queries:
Total patients
Most common disease
Daily visit trends
Revenue by doctor
Gender distribution
City-wise patient count
Most used medicine
All queries included in:
analysis_queries.sql 


📈 Sample Analysis Output (Expected)
Total Patients → 5

Most Common Disease → Fever / Allergy

Highest Revenue Doctor → Dr. Nadee

City With Most Patients → Colombo

Most Used Medicine → Cetirizine / Panadol


🛠️ How to Run This Project

1️⃣ Create a new MySQL database
CREATE DATABASE hospital_db; USE hospital_db; 

2️⃣ Run the schema
Open schema.sql → Execute All

3️⃣ Insert dummy data
Open dummy_data.sql → Execute All

4️⃣ Run analysis queries
Open analysis_queries.sql → Execute All


📌 Tech Stack
MySQL 8.0
MySQL Workbench


💡 Why This Project Is Useful for Data Analysts?

✔ Shows SQL table design skills

✔ Shows data modeling

✔ Includes real-world insights

✔ Good for GitHub portfolio

✔ Recruiters can see your SQL knowledge easily



✨ Author
Tharuka Sewwandi
A passionate student learning Data Analysis and SQL.

