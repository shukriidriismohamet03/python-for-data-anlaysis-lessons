
# 📊  DAY2 
Crime Data Analysis — Data Cleaning & Transformation

A beginner-friendly data analysis project using **Python, Pandas, Google Colab, and Excel**. This project focuses on selecting, filtering, and sorting crime data as part of the data cleaning and transformation process.

---

## 📌 Project Overview

This project demonstrates basic **Pandas data manipulation techniques** using a crime dataset stored in an Excel file.

The main objectives are to learn how to:

- Import Pandas
- Read Excel data
- Select columns
- Select rows
- Use `iloc`
- Use `loc`
- Filter data
- Filter multiple categories
- Apply multiple conditions
- Sort data
- Sort data in ascending order
- Sort data in descending order

---

## 🛠️ Technologies Used

- Python
- Pandas
- Google Colab
- Microsoft Excel
- GitHub

---

## 📂 Dataset

The dataset used is:

`CRIME-DATA-ANALYSIS-COMPLE.xlsx`

The dataset contains crime-related information such as:

- Crime ID
- Crime Date
- Crime Type
- District
- Victim Gender
- Case Status
- Severity Level

---

## 🚀 Data Analysis Code

### 1. Import Pandas

```python
import pandas as pd
````

### 2. Read Excel Data

```python
data = pd.read_excel(
    "/content/drive/MyDrive/Colab Notebooks/CRIME-DATA-ANALYSIS-COMPLE.xlsx"
)
```

### 3. Select One Column

```python
data['Victim_Gender']
```

### 4. Select Multiple Columns

```python
data[['Crime_Type', 'District', 'Victim_Gender']]
```

### 5. Select One Row Using `iloc`

`iloc` selects data based on integer position.

```python
data.iloc[1]
```

### 6. Select Multiple Rows Using `iloc`

```python
data.iloc[0:10]
```

### 7. Select Rows and Columns Using `iloc`

```python
data.iloc[5:10, 2:]
```

### 8. Select Rows and Columns Using `loc`

`loc` allows us to select rows and columns using their labels.

```python
data.loc[10:200, ['Victim_Gender', 'District']]
```

### 9. View the First Rows

```python
data.head()
```

### 10. Filter Female Victims

```python
data[
    data['Victim_Gender'].str.strip().str.lower() == 'female'
]
```

* `.str.strip()` removes unnecessary spaces.
* `.str.lower()` converts text to lowercase.
* `== 'female'` selects female records.

### 11. Filter Multiple Categories Using `isin()`

```python
data[
    data['Victim_Gender'].isin(['Male', 'Female'])
]
```

This selects records where the victim gender is either **Male** or **Female**.

### 12. Filter Using Multiple Conditions

```python
data[
    (data['Victim_Gender'] == 'Female') &
    (data['Severity_Level'] == 'High')
]
```

This selects records where:

* Victim Gender = Female
* Severity Level = High

The `&` operator means **AND**.

### 13. Sort Data

```python
data.sort_values('Crime_Type')
```

By default, Pandas sorts the values in ascending order.

### 14. Sort in Ascending Order

```python
data.sort_values(
    'Crime_Type',
    ascending=True
)
```

### 15. Sort in Descending Order

```python
data.sort_values(
    'Crime_Type',
    ascending=False
)
```

---

## 📚 Pandas Functions Used

| Function                 | Purpose                    |              |
| ------------------------ | -------------------------- | ------------ |
| `pd.read_excel()`        | Read an Excel file         |              |
| `data['column']`         | Select one column          |              |
| `data[['col1', 'col2']]` | Select multiple columns    |              |
| `data.iloc[]`            | Select data by position    |              |
| `data.loc[]`             | Select data by label       |              |
| `data.head()`            | Display the first rows     |              |
| `.str.strip()`           | Remove extra spaces        |              |
| `.str.lower()`           | Convert text to lowercase  |              |
| `.isin()`                | Filter multiple categories |              |
| `sort_values()`          | Sort data                  |              |
| `ascending=True`         | Ascending order            |              |
| `ascending=False`        | Descending order           |              |
| `&`                      | AND condition              |              |
| `                        | `                          | OR condition |

---

## 🎯 Learning Outcomes

By completing this project, I practiced how to:

* Work with Excel datasets using Pandas
* Select specific columns and rows
* Use `iloc` and `loc`
* Filter data using conditions
* Filter multiple categories
* Clean text values
* Apply multiple conditions
* Sort data in different orders
* Prepare data for further analysis

---

## 🔮 Future Improvements

The project can be expanded by adding:

* Missing value handling
* Duplicate removal
* Data type conversion
* Date formatting
* Grouping and aggregation
* `groupby()` analysis
* Pivot tables
* Crime statistics
* Data visualization
* Crime trend analysis
* Interactive dashboards

---

## 👩‍💻 Author

**Shukri Idiris Mohamet**

Bachelor of Computer Applications Graduate

**Interests:** Data Analysis • Information Management • Technology

---

⭐ **If you find this project useful, please consider giving the repository a star!**

```
```

