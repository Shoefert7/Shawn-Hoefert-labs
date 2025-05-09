# 🌦️ Weather Data Analytics Project (Python, SQL, Excel)

**Course:** CEIS 110 – Introduction to Programming  
**Author:** Shawn Hoefert  
**Tools Used:** Python (Anaconda/Spyder), SQLite, Excel  
**Date:** April 2023

---

## 📌 Project Overview

This project demonstrates how to gather, clean, and analyze weather data using a cloud-based source. The data includes temperature and humidity values across two weeks, stored in a local SQLite database, queried using SQL, and analyzed in Python using `pandas` and `matplotlib`.

---

## 🔧 Tools & Technologies

- Python (with Anaconda + Spyder)
- Microsoft Excel
- SQLite (weather.db)
- SQL (basic queries)
- Data cleansing
- Data visualization: histograms, box plots, line charts, scatter plots

---

## 🔄 Workflow Summary

1. **Install Python & Anaconda**
2. **Download weather observation data**
3. **Store data in local database** (`weather.db`)
4. **Query data using SQL**
5. **Cleanse and export relevant data to CSV files**
6. **Visualize with Python/Matplotlib**
7. **Perform basic predictive analysis**

---

## 🧪 SQL Query Examples

``sql
-- Retrieve all data
SELECT * FROM observations;

-- Get min/max temperatures
SELECT MIN(temperature), MAX(temperature) FROM observations;

-- Find weather entries marked as "clear"
SELECT temperature, windSpeed, textDescription 
FROM observations 
WHERE textDescription LIKE '%clear%';

## python
# Histogram of humidity (Week 2)
df2 = pd.read_csv("formatdata2.csv")
df2['Humidity'].hist(bins=10, alpha=0.5)
plt.suptitle("Histogram of Humidity")
plt.show()

# Line chart: Celsius temperature, Week 1 vs Week 2
df1 = pd.read_csv("formatdata1.csv")
df2 = pd.read_csv("formatdata2.csv")
df1.Celsius.plot(label='Week 1')
df2.Celsius.plot(label='Week 2')
plt.legend()
plt.suptitle("Celsius Temperature – Week 1 vs Week 2")
plt.show()

