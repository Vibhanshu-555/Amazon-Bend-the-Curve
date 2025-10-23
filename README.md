# Amazon Bend the Curve - Product Catalog Analysis

## Executive Summary
This project analyzes Amazon's product catalog to evaluate catalog health, identify high-potential products, uncover dead listings, and provide actionable insights to improve sales performance and inventory management. The analysis combines data cleaning, health scoring, and visualization using Python and Power BI.

## Business Problem
Amazon's product catalog contains thousands of listings, some of which underperform or may have incomplete information. The goal is to:
- Identify low-performing or dead listings.
- Highlight high-potential products for focused marketing or inventory support.
- Assess listing completeness and catalog health.
- Provide actionable recommendations for category management and sales optimization.

## Methodology
1. **Data Exploration**: 
   - Inspected dataset structure, checked categorical and numerical columns, and visualized distributions using `matplotlib`.
2. **Data Cleaning & Outlier Handling**:
   - Filled missing numerical values with medians and categorical values with `'Unknown'`.
   - Identified and capped outliers using the IQR method to reduce skew.
3. **Catalog Health Metrics**:
   - Calculated Sales Score, Rating Score, Return Rate Score (inverted), and Completeness Score.
   - Combined metrics into a Health Score using:
     ```
     Health_Score = 0.4*Sales_Score + 0.3*Rating_Score + 0.15*(1-ReturnRate) + 0.15*Completeness
     ```
4. **Insights & Analysis**:
   - Generated category-level summaries for sales, ratings, and health.
   - Identified dead listings, overcrowded categories, and high-potential listings.
   - Exported key metrics and analysis results as CSVs for dashboard integration.
5. **Visualization & Dashboard**:
   - Created a Power BI dashboard with bar charts, scatter plots, heatmaps, pie charts, and tables to visualize catalog health, sales, ratings, and inventory metrics.

## Skills
- Python: Data exploration, cleaning, and analysis using `pandas`, `numpy`, `matplotlib`.
- Data Visualization: Power BI for interactive dashboards.
- Data Handling: Outlier detection, missing value imputation, and data normalization.
- Business Analysis: Identifying key performance indicators (KPIs), catalog health metrics, and actionable insights.

## Results and Business Recommendations
- **Dead Listings**: Products with low sales and poor ratings should be reviewed or removed.
- **High-Potential Listings**: Identify listings with high ratings and moderate sales for focused promotion.
- **Overcrowded Categories**: Categories like Laptops, Other Electronics, and Cameras are highly competitive; strategize pricing and promotions.
- **Catalog Health**: Majority of products are healthy, but completeness and return rates can be improved for specific categories.
- **Actionable Recommendations**:
  - Improve product data completeness across listings.
  - Promote high-potential listings to increase revenue.
  - Regularly monitor dead and low-performing listings for removal or optimization.

## Next Steps
- Integrate additional temporal sales data to track trends over time.
- Add more KPIs for inventory turnover, discount impact, and return analysis.
- Expand dashboard interactivity with filters for category, rating, and sales ranges.
- Continuously monitor catalog health metrics to optimize listings and performance.
