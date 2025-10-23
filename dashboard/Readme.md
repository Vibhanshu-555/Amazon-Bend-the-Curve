# 📊 Dashboard – Catalog Health Insights

This folder contains the **Power BI Dashboard** developed to visualize and analyze catalog health metrics derived from Amazon’s product listings.  
It is the final step of the **“Bend the Curve”** project, providing clear, actionable insights for improving product performance and catalog efficiency.

---

## 🔍 Dashboard Overview

The Power BI dashboard consolidates data processed from previous Jupyter notebooks and showcases key metrics such as:

- **Product Health Scores** – calculated using sales, ratings, return rate, and completeness.  
- **Category Performance** – total sales, average ratings, and health scores by category.  
- **Listing Quality** – identification of dead listings, overcrowded categories, and high-potential products.

---

## 📈 Key Visualizations

1. **Health Score Distribution**  
   Displays how product health scores are spread across the catalog, helping identify low-performing items.

2. **Category-wise Performance**  
   Bar charts showing **total sales**, **average ratings**, and **average health scores** across categories.

3. **Dead Listings Overview**  
   Highlights listings with **low ratings** and **no sales**, indicating products that may need removal or improvement.

4. **Overcrowded Categories**  
   Visual representation of categories with a high number of listings but limited differentiation or sales.

5. **High-Potential Listings**  
   Shows products with **high health scores**, **good ratings**, and **moderate competition**—ideal for scaling up.

---

## 🛠️ Dashboard Features

- 🎛️ **Interactive Filters** – filter by category, health score range, or other parameters.  
- 💡 **Dynamic Tooltips** – hover for detailed insights and metrics.  
- 🔄 **Real-time Data Refresh** – reflects the latest processed data from CSV files.  
- 📊 **Visual Variety** – includes bar charts, scatter plots, donut charts, and tables with conditional formatting.

---

## 📂 Folder Contents

| File | Description |
|------|--------------|
| `Dashboard.pbix` | Main Power BI file containing all visuals and dashboards |
| `Dashboard.pdf` | Static exported version of the dashboard for presentations |
| [`data/summary_data/`](../data/summary_data/) | Folder containing processed CSV files used as data sources |

---

## 🚀 How to Use

1. Open the `Dashboard.pbix` file in **Power BI Desktop/Service**.  
2. Ensure the **data connections** point to the CSV files inside the [`data/summary_data/`](../data/summary_data/) folder.  
3. Use slicers and filters to explore different KPIs and categories.  
4. Export visuals or full reports as needed for analysis or presentation.

---

## 🎯 Purpose

The dashboard aims to:

- 🧩 **Identify Underperforming Listings** – flag dead or low-rated items.  
- 🗂️ **Optimize Catalog Structure** – highlight overcrowded or weak-performing categories.  
- 📈 **Support Strategic Decisions** – provide a visual, data-driven foundation for catalog optimization.

---

## 🔗 Live Dashboard Link

You can view the dashboard online here:  
👉 [**Power BI Dashboard Link**](https://app.powerbi.com/links/S6yBOPn61E?ctid=a56be167-9ffb-4100-a624-ae3e45045aa6&pbi_source=linkShare&bookmarkGuid=e25c7614-ccaf-4258-bb46-73ab87e3f25d)
