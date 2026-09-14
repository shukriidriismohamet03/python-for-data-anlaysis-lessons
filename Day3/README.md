# 📊 Day 3 — Crime Data Cleaning & Transformation

## Overview

As part of my **Crime Data Analysis project**, Day 3 focused on preparing the dataset for reliable analysis by cleaning inconsistent categorical values, standardizing data, renaming columns, converting categorical variables into numerical values, and formatting date information.

The goal was to improve **data consistency, quality, and usability** before moving into exploratory analysis and visualization.

---

## 🛠️ Tools & Technologies

* **Python**
* **Pandas**
* **Google Colab**
* **Microsoft Excel**

---

## 📁 Dataset

**Dataset:** `CRIME-DATA-ANALYSIS-COMPLA.xlsx`

### Key Variables

| Column           | Description                          |
| ---------------- | ------------------------------------ |
| `Crime_ID`       | Unique identifier for each crime     |
| `Crime_Date`     | Date when the crime occurred         |
| `Crime_Type`     | Type/category of crime               |
| `District`       | District where the crime occurred    |
| `Victim_Gender`  | Gender of the victim                 |
| `Case_Status`    | Current status of the case           |
| `Severity_Level` | Severity classification of the crime |

---

## 🧹 Data Cleaning & Transformation

### 1. Load the Dataset

The dataset was imported from an Excel file using Pandas.

```python
import pandas as pd

data = pd.read_excel(
    "/content/drive/MyDrive/Colab Notebooks/CRIME-DATA-ANALYSIS-COMPLA.xlsx"
)

data.head()
```

### 2. Rename Column

The `Crime_ID` column was renamed to `Crimid` for a shorter and more convenient column name.

```python
data = data.rename(columns={
    "Crime_ID": "Crimid"
})
```

### 3. Standardize District Values

The `District` column was reviewed using `value_counts()` to identify inconsistent entries.

```python
data["District"].value_counts()
```

An inconsistent lowercase value was standardized:

```python
data["District"] = data["District"].replace(
    "hodan", "Hodan"
)
```

### 4. Review Crime Types

The distribution of crime categories was checked to identify the values available in the dataset.

```python
data["Crime_Type"].value_counts()
```

### 5. Standardize Victim Gender

Inconsistent lowercase gender values were converted to a standardized format.

```python
data["Victim_Gender"] = data["Victim_Gender"].replace({
    "male": "Male",
    "female": "Female"
})
```

The results were then verified:

```python
data["Victim_Gender"].value_counts()
```

### 6. Standardize Case Status

Case status values were standardized to maintain consistency throughout the dataset.

```python
data["Case_Status"] = data["Case_Status"].replace({
    "open": "Open",
    "closed": "Closed",
    "under investigation": "Under Investigation"
})
```

### 7. Encode Severity Levels

The categorical `Severity_Level` variable was converted into numerical values to support quantitative analysis.

| Severity | Code |
| -------- | ---: |
| Low      |    1 |
| Medium   |    2 |
| High     |    3 |

```python
data["Severity_Level"] = data["Severity_Level"].replace({
    "Low": 1,
    "Medium": 2,
    "High": 3
})
```

### 8. Convert Crime Date

The `Crime_Date` column was converted to Pandas datetime format.

```python
data["Crime_Date"] = pd.to_datetime(
    data["Crime_Date"],
    errors="coerce"
)
```

Using `errors="coerce"` ensures that invalid date values are converted to `NaT` rather than causing the program to fail.

### 9. Validate Data Types

Finally, the data types of the dataset were reviewed:

```python
data.dtypes
```

---

## ✅ Day 3 Results

The dataset was successfully prepared for the next stage of analysis.

### Completed Tasks

* Renamed `Crime_ID` to `Crimid`
* Identified and corrected inconsistent district values
* Standardized victim gender categories
* Standardized case status categories
* Reviewed crime type categories
* Encoded severity levels numerically
* Converted `Crime_Date` to datetime
* Validated column data types

---

## 🎯 Why This Matters

Data cleaning is an essential step in the data analysis process. Inconsistent spelling, capitalization, categorical formats, and data types can lead to inaccurate analysis and misleading results.

By standardizing the dataset first, the data becomes more reliable and ready for **exploratory data analysis (EDA), visualization, and further statistical analysis**.

---


## 👤 Author

**Shukri Idiris Mohamet**

Bachelor of Computer Applications (BCA) Graduate
Interested in **Data Analysis, Data Management, Software Development, and Technology**.
