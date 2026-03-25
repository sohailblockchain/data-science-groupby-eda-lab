# 📊 Data Aggregation & GroupBy Lab (Pandas)

👨‍🏫 Instructor: **Sohail Ahmed**
📚 Course: **Data Science with Python**

---

## 📌 Project Overview

This lab teaches students how to use **Pandas GroupBy, Aggregation, and Pivot Tables** to summarize data and generate insights.

---

## 🧠 Key Concept

> **GroupBy helps convert raw data into insights.**
> Instead of analyzing raw rows, we summarize data to understand patterns.

---

## 📁 Project Structure

```id="proj1"
pandas-groupby-aggregation-lab
│
├── groupby_lab_dataset.csv
├── GroupBy_Practical_Lab.ipynb
└── README.md
```

---

## ⚙️ Requirements

* Python (>= 3.8)
* Anaconda (Recommended)
* Jupyter Notebook

---

## 🚀 How to Run the Lab

### Step 1: Open Jupyter Notebook

Open **Anaconda Navigator → Launch Jupyter Notebook**

---

### Step 2: Open Notebook

Open:

```id="proj2"
GroupBy_Practical_Lab.ipynb
```

---

### Step 3: Run Cells in Order

⚠️ IMPORTANT: Always run cells in order using **Shift + Enter**

---

## ✅ Final Working Code (Use This Only)

### 🔹 Step 1: Import Pandas

```python id="code1"
import pandas as pd
```

---

### 🔹 Step 2: Load Dataset

```python id="code2"
df = pd.read_csv("groupby_lab_dataset.csv")
```

---

### 🔹 Step 3: Show Data

```python id="code3"
df.head()
```

---

### 🔹 Step 4: GroupBy (Basic)

```python id="code4"
df.groupby("City")["Price"].mean()
```

👉 Calculates average price per city

---

### 🔹 Step 5: Multiple Aggregation

```python id="code5"
df.groupby("City")["Price"].agg(["mean","max","min","count"])
```

👉 Returns:

* mean → average
* max → highest
* min → lowest
* count → total records

---

### 🔹 Step 6: GroupBy with Multiple Columns

```python id="code6"
df.groupby(["City","Gender"])["Price"].mean()
```

👉 Advanced grouping (City + Gender)

---

### 🔹 Step 7: Pivot Table

```python id="code7"
pd.pivot_table(df, values="Price", index="City", columns="Gender", aggfunc="mean")
```

👉 Similar to Excel Pivot Table

---

## 🔍 Debug Tip (IMPORTANT)

If you see errors:

### 🔹 Fix by restarting kernel

```id="fix1"
Kernel → Restart & Run All
```

---

### 🔹 Check file exists

```python id="code8"
import os
os.listdir()
```

👉 You should see:

```id="proj3"
groupby_lab_dataset.csv
```

---

## 🎓 Student Tasks

Students must complete:

1. Find average price by City
2. Find total quantity by Product
3. Find highest price product
4. Group by City and Gender
5. Create pivot table

---

## 🌍 Real-World Use Case

Companies use GroupBy to:

* Analyze sales by city
* Compare performance
* Generate reports
* Extract insights

---

## 🏆 Skills Gained

* Pandas Data Analysis
* GroupBy Operations
* Data Aggregation
* Pivot Tables
* Insight Generation

---

## 📌 Final Thought

> “Data becomes powerful when we turn it into insights.
> GroupBy is one of the most important tools to achieve this.”

---
