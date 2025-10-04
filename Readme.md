# 🚢 Titanic Data Engineering Project / Proyecto de Ingeniería de Datos – Titanic  

---

## 🇬🇧 **English Version**

### 📘 Project Overview  
This project demonstrates a complete **data engineering workflow** using the Titanic dataset.  
It includes **data cleaning, PostgreSQL database integration, SQL queries, and visual analysis** using **Python (pandas, psycopg2, matplotlib, seaborn)**.  

---

### 🧩 Technologies Used  
- **Database:** PostgreSQL  
- **Python Libraries:** pandas, psycopg2, matplotlib, seaborn  
- **Environment:** Jupyter Notebook  
- **Dataset:** `test_clean.csv` (cleaned version of the original Titanic dataset)  

---

### ⚙️ Project Workflow  

#### 1️⃣ Database Setup  
- Database created: `titanic_db2`  
- User: `mati_user`  
- Table: `titanic`  
- Columns:  PassengerId, Pclass, Name, Sex, Age, SibSp, Parch, Ticket, Fare, Cabin, Embarked, Title 

#### 2️⃣ Data Cleaning  
- Fixed encoding and formatting issues.  
- Removed missing or inconsistent values.  
- Verified data types for each column.  
- Saved the cleaned version as `test_clean.csv`.  

#### 3️⃣ Data Insertion  
- Connected Python to PostgreSQL using psycopg2.  
- Inserted data row by row from the cleaned CSV file.  
- Data is now ready for SQL analysis.  

### 📊 SQL Queries & Insights  

#### 🧮 Passengers per Class  

SELECT Pclass, COUNT(*) AS num_passengers 
FROM titanic 
GROUP BY Pclass 
ORDER BY Pclass;


### Insight: Most passengers traveled in third class, showing a predominance of lower-income individuals.


👩‍🦱 ### Average Age by Gender

SELECT Sex, AVG(Age) AS avg_age 
FROM titanic 
GROUP BY Sex;


### Insight: The average age of female passengers was slightly higher than that of male passengers.

💰 ### Top 10 Highest Fares

SELECT Name, Ticket, Fare 
FROM titanic 
ORDER BY Fare DESC 
LIMIT 10;

### Insight: The most expensive tickets belonged to first-class passengers, highlighting strong social and economic divisions of the time.


📈 Visualizations
### Generated with Matplotlib and Seaborn:

🧠 Key Learnings
### Connecting Python with PostgreSQL.

### Inserting data from pandas into a SQL table.

### Running SQL queries directly from Python.

### Visualizing SQL results with Python libraries.

### Structuring and documenting a professional data project.

👨‍💻 Author
Matías Kostiak – Data Engineer
📍 Ciudad del Este, Paraguay
📧 Contact: matiaskostiak25@gmail.com