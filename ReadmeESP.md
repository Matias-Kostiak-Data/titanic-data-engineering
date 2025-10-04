# 🚢 Proyecto de Ingeniería de Datos – Titanic  

---

## 📘 Descripción del Proyecto  
Este proyecto demuestra un flujo completo de **ingeniería de datos** utilizando el dataset del Titanic.  
Incluye **limpieza de datos, integración con base de datos PostgreSQL, consultas SQL y visualización de resultados** usando **Python (pandas, psycopg2, matplotlib, seaborn)**.  

---

## 🧩 Tecnologías Utilizadas  
- **Base de Datos:** PostgreSQL  
- **Librerías de Python:** pandas, psycopg2, matplotlib, seaborn  
- **Entorno de Trabajo:** Jupyter Notebook  
- **Dataset:** `test_clean.csv` (versión limpia del dataset original del Titanic)  

---

## ⚙️ Flujo del Proyecto  

### 1️⃣ Configuración de la Base de Datos  
- Base de datos creada: `titanic_db2`  
- Usuario: `mati_user`  
- Tabla: `titanic`  
- Columnas:  PassengerId, Pclass, Name, Sex, Age, SibSp, Parch, Ticket, Fare, Cabin, Embarked, Title


### 2️⃣ Limpieza de Datos  
- Se corrigieron errores de codificación y formato.  
- Se eliminaron valores nulos o inconsistentes.  
- Se verificaron los tipos de datos correctos para cada columna.  
- Se guardó la versión final como `test_clean.csv`.  

### 3️⃣ Inserción de Datos  
- Se conectó Python a PostgreSQL usando psycopg2.  
- Se insertaron los datos del CSV limpio fila por fila.  
- Los datos quedaron listos para su análisis mediante SQL.  

---

## 📊 Consultas SQL e Insights  

### 🧮 Pasajeros por Clase  

SELECT Pclass, COUNT(*) AS num_passengers 
FROM titanic 
GROUP BY Pclass 
ORDER BY Pclass;

### Insight: La mayoría de los pasajeros viajaban en tercera clase, lo que refleja un predominio de personas con menor poder adquisitivo. 


-----------------------------------------------------------------------

👩‍🦱 Edad Promedio por Género

SELECT Sex, AVG(Age) AS avg_age 
FROM titanic 
GROUP BY Sex;


Insight: La edad promedio de las mujeres fue ligeramente superior a la de los hombres.
------------------------------------------------------------------------
💰 Top 10 Boletos Más Caros

SELECT Name, Ticket, Fare 
FROM titanic 
ORDER BY Fare DESC 
LIMIT 10;


### Insight: Los boletos más caros pertenecían a pasajeros de primera clase, reflejando las claras diferencias sociales de la época.-----------------------------------------------------------------------

📈 Visualizaciones

Generadas con Matplotlib y Seaborn:


🧠 Conocimientos Adquiridos

### Conexión entre Python y PostgreSQL.

### Inserción de datos desde pandas a una tabla SQL.

### Ejecución de consultas SQL directamente desde Python.

### Visualización de resultados con librerías de Python.

### Estructuración y documentación de un proyecto de datos profesional.

👨‍💻 Autor

Matías Kostiak – Ingeniero de Datos
📍 Ciudad del Este, Paraguay
📧 Contacto: matiaskostiak25@gmail.com