# 🧾 Methodology

This document outlines the complete methodology followed for the **Amazon “Bend the Curve” Catalog Health Project**.  
It explains the approach, formulas, and logic used across data cleaning, metric computation, and analysis.

---

## 1️⃣ Data Preparation

### **a. Initial Exploration**
- Imported and inspected the dataset using `pandas`.
- Used `.info()` and `.head()` to check data structure and column types.
- Identified categorical and numerical columns for targeted cleaning.

### **b. Handling Missing Values**
- **Numerical columns:** Filled with **median** values to maintain data distribution.
- **Categorical columns:** Filled with **"Unknown"** to avoid loss of records.

### **c. Outlier Detection and Treatment**
- Applied the **Interquartile Range (IQR)** method:
  ```
  IQR = Q3 - Q1
  Lower Bound = Q1 - 1.5 * IQR
  Upper Bound = Q3 + 1.5 * IQR
  ```
- Capped outliers beyond upper/lower bounds instead of removing them.
- Visualized distributions and outliers using **Matplotlib** boxplots and histograms.

---

## 2️⃣ Catalog Health Metrics

To evaluate product performance, several key metrics were computed and combined into a **Health Score**.

### **a. Sales Score**
- Normalized total product sales using **Min-Max normalization**:  
  `Sales_Score = (Sales - Sales_min) / (Sales_max - Sales_min)`

### **b. Rating Score**
- Normalized product ratings between 0–1:  
  `Rating_Score = (Rating - Rating_min) / (Rating_max - Rating_min)`

### **c. Return Rate Score**
- Since a higher return rate is negative, it was **inverted** after normalization:  
  `Return_Rate_Score = 1 - ((Return_Rate - min(Return_Rate)) / (max(Return_Rate) - min(Return_Rate)))`

### **d. Completeness Score**
- Based on the percentage of non-missing attributes for each listing:
- Score = **1.0** if complete, else proportional to filled fields.

---

## 3️⃣ Health Score Calculation

A weighted formula was applied to combine the above metrics into one comprehensive indicator:

```python
df['Health_Score'] = (
  0.4 * df['Sales_Score'] +
  0.3 * df['Rating_Score'] +
  0.15 * df['Return_Rate_Score'] +
  0.15 * df['Completeness_Score']
)
```
---

## 4️⃣ Analytical Grouping

Products were grouped by Category to identify performance and improvement areas.

### Metrics computed:
- Total Sales per category
- Average Rating
- Average Health Score
- Low/Zero Sales %
- Number of Products

---

## 5️⃣ Classification Logic

|Classification Type|	Criteria|
|------|--------------|
|Dead Listings|	Low Rating (<3.5) and No/Low Sales|
|Overcrowded Categories|	High product count but below-average sales|
|High-Potential Listings|	High rating (>4.2), medium sales, and high health score|

---

## 6️⃣ Outputs for Dashboard

The following CSVs were generated for Power BI integration:

- Category_Summary.csv
- Dead_Listings.csv
- Healthy_Potential_Listings.csv
- Overcrowded_Categories.csv

These outputs form the base for visualization and further insight generation.

---

## 7️⃣ Tools & Libraries Used

- **Python:** Core analysis
- **Pandas:** Data manipulation and aggregation
- **Matplotlib:** Outlier and distribution visualization
- **Power BI:** Interactive dashboard creation

---

*📘 This methodology ensures reproducibility, transparency, and traceability across all stages of the analysis pipeline.*
