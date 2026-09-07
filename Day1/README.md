# 📊 Day 1 – Data Analysis with Pandas

This project is part of my **Data Analysis learning journey**.
In this first-day practice, I learned how to use **Python and Pandas** to load, inspect, and understand a dataset.

## 📌 Project Overview

The notebook focuses on exploring a **Crime Data Analysis** dataset using the Pandas library.

The dataset contains **300 records and 7 columns**, including crime information such as crime type, district, victim gender, case status, and severity level.

## 🛠️ Technologies Used

* Python 🐍
* Pandas
* Google Colab
* Excel Dataset

## 📂 Dataset Columns

| Column           | Description                        |
| ---------------- | ---------------------------------- |
| `Crime_ID`       | Unique crime identification number |
| `Crime_Date`     | Date when the crime occurred       |
| `Crime_Type`     | Type of crime                      |
| `District`       | District where the crime occurred  |
| `Victim_Gender`  | Gender of the victim               |
| `Case_Status`    | Current status of the case         |
| `Severity_Level` | Severity of the crime              |

## 🔍 What I Learned

During this exercise, I practiced:

* Importing Pandas
* Loading an Excel dataset
* Viewing the first 5 rows using `head()`
* Viewing the last 5 rows using `tail()`
* Displaying random records using `sample()`
* Checking dataset dimensions using `shape`
* Viewing column names using `columns`
* Checking data types using `dtypes`
* Understanding dataset information using `info()`
* Generating statistical summaries using `describe()`
* Exploring categorical data using `describe(include='object')`

## 💻 Example

```python
import pandas as pd

data = pd.read_excel("CRIME-DATA-ANALYSIS-COMPLA.xlsx")

data.head()
data.tail()
data.shape
data.columns
data.dtypes
data.info()
data.describe(include="all")
```

## 📈 Dataset Summary

The initial inspection showed:

* **Rows:** 300
* **Columns:** 7
* **Crime types:** 8 unique categories
* **Districts:** 7 unique categories
* **Victim gender:** 4 recorded categories
* **Case statuses:** 6 unique categories
* **Severity levels:** 5 unique categories

The dataset also contains missing values in several columns, which can be explored and cleaned in later stages of the analysis.

## 📁 Project Structure

```text
Day-1-Data-Analysis/
│
├── Day1l.ipynb
└── README.md
```

## 🚀 Learning Journey

This is **Day 1** of my Data Analysis learning journey. I will continue building my skills in:

* Data Cleaning
* Data Exploration
* Data Visualization
* Excel
* SQL
* Python
* Pandas
* NumPy
* Power BI

## 👩‍💻 Author

**Shukri Idiris Mohamet**

Bachelor of Computer Applications | Aspiring Data Analyst
