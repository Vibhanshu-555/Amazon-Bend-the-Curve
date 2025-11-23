# Amazon Bend the Curve – Product Catalog Analysis

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)](https://numpy.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-F7931E?style=flat&logo=matplotlib&logoColor=white)](https://matplotlib.org/)
[![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=power-bi&logoColor=black)](https://powerbi.microsoft.com/)
[![Excel](https://img.shields.io/badge/Excel-217346?style=flat&logo=microsoft-excel&logoColor=white)](https://www.microsoft.com/microsoft-365/excel)

## Executive Summary
This project analyzes **Amazon's product catalog** to evaluate listing performance and identify actionable insights. Using **Python for data exploration, cleaning, and metrics**, and **Power BI for interactive visualization**, I derived key insights into product health, sales, and category performance. 

**Dashboard & Files:**  
- [Power BI Dashboard (.pbix)](./dashboard/Amazon_Bend_The_Curve.pbix)  
- [Dashboard PDF](./dashboard/Amazon_Bend_The_Curve.pdf)

## Business Problem
Amazon’s catalog contains thousands of products, but not all drive revenue effectively.  
**Amazon: Bend the Curve** challenge – identify **underperforming listings, dead products, and high-potential opportunities** for catalog optimization.

## Methodology
- **Data Exploration (EDA):** Inspect columns, distributions, nulls  
- **Data Cleaning:** Fill missing values, correct types, cap outliers  
- **Metrics Engineering:** Sales Score, Rating Score, Return Rate Score, Completeness Score → Health Score  
- **Analysis:** Aggregate by category, identify dead listings, overcrowded categories, high-potential products  

## Skills & Tools
- **Python:** `pandas`, `numpy`, `matplotlib` – EDA, cleaning, outlier handling, metrics calculation  
- **Power BI:** Interactive dashboard, bar charts, scatter plots, heatmaps, pie charts  
- **Business Analysis:** Catalog optimization, KPI-driven insights, sales strategy  

## Results & Business Recommendations
**Insights from analysis:**  
- **Dead Listings:** 152 products (low rating + no sales)  
- **Overcrowded Categories:** Laptops, Other Electronics, Cameras, TV & Display  
- **High-Potential Listings:** 8558 products (criteria: high rating + moderate sales + low competition)  
- **Average Health Score:** 0.68 (42675 products)  
- **Average Rating:** 4.4 / 5

![**Dashboard Screenshot**](dashboard/Amazon_Bend_the_Curve_Dashboard.png)

**Recommendations for Amazon:**  
- Promote high-rating, moderate-sales products for ROI  
- Improve listing **completeness** for discoverability  
- Optimize or remove **dead listings** to save resources  
- Focus marketing/pricing strategies on **overcrowded categories**  

## Next Steps
- Track temporal **sales trends** and seasonal patterns  
- Perform **A/B testing** on listings and promotions  
- Explore **predictive modeling** for sales and return rates  
- Continuous monitoring of **catalog health** for actionable insights  
