# 📓 Notebooks – Data Preparation, Analysis & KPI Generation

This folder contains all **Jupyter notebooks** used for **data exploration, cleaning, analysis, and KPI calculation** as part of the **Amazon’s Bend the Curve – Catalog Health Analytics Project**.  

The notebooks transform raw catalog data into **clean, actionable insights** and prepared CSVs, which are then used in the **Power BI dashboard** for visualization.

---

## 🗂 Notebook Overview

| Notebook | Description |
|-----------|-------------|
| **1. Data_Exploration.ipynb** | Performs **initial exploration** of the dataset: <br> - Checks basic information using `df.info()` and `df.head()`. <br> - Explores **categorical columns** for unique values and frequency distributions. <br> - Analyzes **numerical columns** for ranges, missing values, and basic summary statistics. <br> - Uses **Matplotlib** to visualize distributions, detect trends, and identify potential outliers visually. |
| **2. Data_Cleaning.ipynb** | Handles **data cleaning and outlier treatment**: <br> - Fills **missing numerical values** with median. <br> - Fills **missing categorical values** with `'Unknown'`. <br> - Detects **outliers using IQR** for each numerical column. <br> - Uses **Matplotlib** to visualize outliers before capping. <br> - Caps outliers individually to reduce their impact while maintaining dataset integrity. |
| **3. Catalog_Health_Metrics.ipynb** | Calculates **catalog health scores** for each product: <br> - **Sales_Score** – normalized sales performance. <br> - **Rating_Score** – normalized product rating. <br> - **Return_Rate_Score** – inverted return rate. <br> - **Completeness_Score** – evaluates how complete the listing information is. <br> - **Health_Score** – composite metric calculated as: <br> `Health_Score = 0.4*(Sales_Score) + 0.3*(Rating_Score) + 0.15*(Return_Rate_Score) + 0.15*(Completeness_Score)` |
| **4. Analysis_Results.ipynb** | Prepares **final datasets and insights** for dashboard use: <br> - Generates `Category_Summary.csv` – total sales, average rating, average health score, low-sales % per category. <br> - Generates `Dead_Listings.csv` – products with low rating and no sales. <br> - Generates `High_Potential_Listings.csv` – listings with high health score and moderate competition. <br> - Generates `Overcrowded_Categories.csv` – categories with high product count and low distinctiveness. <br> - These CSVs serve as **inputs to the Power BI dashboard**. |

---

## ⚙️ Workflow

1. Run notebooks **in sequence**:  
   **Data_Exploration → Data_Cleaning → Catalog_Health_Metrics → Analysis_Results**
2. Each stage **prepares and refines** the dataset for downstream analysis and visualization.  
3. **Matplotlib** is used to visualize distributions, identify trends, and detect outliers.  
4. Cleaned and aggregated CSVs are exported to the [`/data/summary_data`](../data/summary_data/) folder for dashboard creation.  

---

## 🧩 Key Libraries

- `pandas` & `numpy` – data manipulation and calculations  
- `matplotlib` & `seaborn` – visualizations for exploration and outlier detection
- `jupyter` – interactive notebook execution  

---

## 💡 Purpose

These notebooks form the **analytical backbone** of the *Amazon Bend the Curve* project.  
They ensure that all metrics and insights visualized in Power BI are **clean, reliable, and data-driven**, enabling Amazon to:

- Evaluate catalog health  
- Identify **dead listings** and **high potential products**  
- Analyze category performance  
- Make informed decisions for improving overall catalog performance  
