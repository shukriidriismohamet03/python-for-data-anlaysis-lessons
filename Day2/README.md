# Crime Data Analysis – Day 2

## 📌 Project Overview

This project focuses on **data cleaning and transformation using Python and Pandas**. The dataset contains crime records, including information about crime types, districts, victim gender, case status, severity level, and crime dates.

The work was completed using **Google Colab** and demonstrates basic Pandas techniques for inspecting, selecting, cleaning, and transforming data.

## 🎯 Objectives

The main objectives of this project are to:

* Load crime data into a Pandas DataFrame.
* Inspect the structure and contents of the dataset.
* Select individual columns.
* Select multiple columns.
* Identify missing values.
* Clean inconsistent categorical values.
* Transform data into a more useful format.
* Prepare the dataset for further analysis.

## 🛠️ Technologies Used

* **Python 3**
* **Pandas**
* **Google Colab**
* **Microsoft Excel** dataset

## 📊 Dataset

The project uses a crime dataset named:

`CRIME-DATA-ANALYSIS-COMPLE.xlsx`

The dataset contains approximately **300 crime records**.

Important columns include:

| Column           | Description                        |
| ---------------- | ---------------------------------- |
| `Crime_ID`       | Unique identifier for a crime case |
| `Crime_Date`     | Date when the crime occurred       |
| `Crime_Type`     | Type/category of crime             |
| `District`       | District where the crime occurred  |
| `Victim_Gender`  | Gender of the victim               |
| `Case_Status`    | Current status of the case         |
| `Severity_Level` | Severity of the crime              |

## 🔍 Data Exploration

The notebook demonstrates how to select a single column:

```python
data['Victim_Gender']
```

It also demonstrates selecting multiple columns:

```python
data[['Crime_Type', 'District', 'Victim_Gender']]
```

These operations help focus the analysis on specific variables.

## 🧹 Data Cleaning

The dataset contains some data-quality issues, including:

* Missing values (`NaN`)
* Inconsistent capitalization such as `Male`, `MALE`, and `male`
* Inconsistent case-status values such as `Closed` and `closed`
* Inconsistent severity values such as `Medium`, `MEDIUM`, and `medium`
* Unknown values in some categorical fields

These issues need to be standardized before performing reliable analysis.

For example, categorical values can be standardized using:

```python
data['Victim_Gender'] = data['Victim_Gender'].str.strip().str.title()
```

Similarly:

```python
data['Case_Status'] = data['Case_Status'].str.strip().str.title()
data['Severity_Level'] = data['Severity_Level'].str.strip().str.title()
```

## 📈 Possible Future Analysis

After cleaning the dataset, it can be used to investigate questions such as:

* Which crime type occurs most frequently?
* Which district has the highest number of reported crimes?
* What is the distribution of crimes by victim gender?
* How many cases are open, closed, or under investigation?
* Which crimes have the highest severity?
* How do crime patterns change over time?

## ▶️ How to Run

### Using Google Colab

1. Open the notebook in Google Colab.
2. Upload the crime dataset.
3. Import Pandas:

```python
import pandas as pd
```

4. Load the Excel file:

```python
data = pd.read_excel("CRIME-DATA-ANALYSIS-COMPLA.xlsx")
```

5. Run the notebook cells from top to bottom.

### Using Jupyter Notebook

Install Pandas and the Excel-reading dependency if necessary:

```bash
pip install pandas openpyxl
```

Then run the notebook using Jupyter Notebook or JupyterLab.

## 📁 Project Structure

```text
Crime-Data-Analysis/
│
├── Day2.ipynb
├── CRIME-DATA-ANALYSIS-COMPLA.xlsx
└── README.md
```

## 📝 Learning Outcomes

By completing this project, you practice:

* Importing Pandas
* Reading Excel files
* Working with DataFrames
* Selecting columns
* Inspecting datasets
* Identifying data-quality problems
* Cleaning categorical data
* Preparing data for analysis



---

⭐ This project is part of a practical learning exercise in **Python, Pandas, and Data Analysis**.
