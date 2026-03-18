# Exploratory Data Analysis (EDA)

## Overview
Exploratory Data Analysis (EDA) is the process of understanding the dataset before performing detailed analysis or modeling. In this module, I explored the dataset using multiple tools such as shell commands, Python, and SQL to identify patterns, inconsistencies, and relationships.

---

### Dataset Overview
- Observed the structure of the dataset including rows and columns
- Identified types of features (numerical and categorical)
- Understood the context and purpose of the dataset

---

### Data Inspection

Using shell commands:

```bash
head data.csv
```
- Viewed the first few rows of the dataset

```bash
wc -l data.csv
```
- Checked total number of records

Using Python:

```python
import pandas as pd
df = pd.read_csv("data.csv")
df.head()
df.info()
```
- Inspected column names and data types

---

### Summary Statistics

Using Python:

```python
df.describe()
```
- Calculated mean, median, standard deviation, min, and max values

Using SQL (DuckDB):

```sql
SELECT AVG(column), MIN(column), MAX(column)
FROM data;
```
- Performed aggregate statistical analysis

---

### Missing Values Analysis

Using Python:

```python
df.isnull().sum()
```
- Identified missing values in each column

Using shell:

```bash
grep ",," data.csv
```
- Detected rows with missing fields
---

### Duplicate Records

Using shell:

```bash
sort data.csv | uniq -d
```
- Checked duplicate entries

Using Python:

```python
df.duplicated().sum()
```
- Counted duplicate rows
---

### Data Distribution

- Observed distribution of numerical features
- Checked whether data is skewed or normally distributed
- Identified ranges of values

Example (Python):

```python
df['column'].value_counts()
```
---

### Correlation Analysis

Using Python:

```python
df.corr()
```
- Identified relationships between numerical variables

Insight:
- Helped understand which features are strongly related
---

### Outlier Detection

- Looked for extreme values in numerical columns
- Compared values against expected ranges

Example:

```python
df['column'].describe()
```
- Used statistical summaries to identify unusual values
---
### Data Filtering and Exploration

Using shell:

```bash
grep "India" data.csv
```
- Filtered specific records

Using SQL:

```sql
SELECT column, COUNT(*)
FROM data
GROUP BY column;
```
- Aggregated and explored grouped data

---

### Key Observations

- Identified missing values in multiple columns
- Found duplicate records that need removal
- Observed strong correlations between certain variables
- Detected outliers that may affect analysis
- Noted inconsistencies in text formatting

---

### Conclusion

EDA helped in understanding the dataset structure, identifying data quality issues, and discovering patterns.  
This step is essential before performing advanced analysis or building machine learning models, as it ensures that the dataset is well understood and properly prepared.
