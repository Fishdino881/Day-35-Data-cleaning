# Day-35 Data cleaning

Overview

Data cleaning is the process of fixing or removing incorrect, incomplete, duplicate, or inconsistent data.
In real-world datasets, clean data is rare data cleaning is a mandatory step before analysis or machine learning.

Pandas provides powerful tools to clean, transform, and prepare data efficiently.

---

Common Data Issues

 Missing values (NaN)
 Duplicate records
 Incorrect data types
 Inconsistent formatting
 Outliers

---

Handling Missing Values

Detect Missing Data

```python
df.isnull()
df.isnull().sum()
```

Remove Missing Values

```python
df.dropna()
```

Fill Missing Values
```python
df.fillna(0)
df["Age"].fillna(df["Age"].mean(), inplace=True)
```

---

Removing Duplicates

```python
df.duplicated()
df.drop_duplicates(inplace=True)
```

---

Fixing Data Types

```python
df.dtypes
df["Age"] = df["Age"].astype(int)
```

---

Renaming Columns

```python
df.rename(columns={"old_name": "new_name"}, inplace=True)
```

---

Handling Inconsistent Data

Standardizing Text

```python
df["City"] = df["City"].str.lower()
```

Trimming Spaces

```python
df["Name"] = df["Name"].str.strip()
```

---

Detecting & Handling Outliers

```python
df.describe()
```

(Outliers are often handled using IQR or Z-score methods.)

---

Why Data Cleaning Matters

 Improves model accuracy
 Prevents misleading analysis
 Saves time in later stages
 Essential for real-world datasets

