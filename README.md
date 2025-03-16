# Sales Performance at OfficeMart: Key Trends and Profitability Insights (2023)

## Table of Contents
- [Project Background](#project-background)
- [Data Structure & Initial Checks](#data-structure--initial-checks)
- [Executive Summary](#executive-summary)
- [Insights Deep Dive](#insights-deep-dive)
  - [Sales and Seasonal Trends](#sales-and-seasonal-trends)
  - [Profitability Trends and Volatility](#profitability-trends-and-volatility)
  - [Sales Volume and Demand Patterns](#sales-volume-and-demand-patterns)
  - [Subcategory Performance: Growth vs. Profitability](#subcategory-performance-growth-vs-profitability)
  - [Weekly Sales and Profit Analysis: 2023 vs. 2022](#weekly-sales-and-profit-analysis-2023-vs-2022)
- [Recommendations](#recommendations)
- [Assumptions & Caveats](#assumptions--caveats)

---

## Project Background

For this project, I analyzed year-over-year sales performance for OfficeMart, a fictional office supply and furniture retailer, to help sales managers and executives make informed decisions. This report explores total sales trends, profitability, product category performance, and sales seasonality, providing insights to help business leaders optimize revenue, refine product strategies, and improve overall performance.

Interactive Tableau Dashboard for exploring sales and profit trends can be found [here.](https://public.tableau.com/app/profile/seana.parker/viz/2023SalesPerformanceDashboard/SalesDashboard#1)

Raw datasets can be found [here.](Exploration)

---

## Data Structure & Initial Checks

The company's main database consists of three tables: `Orders`, `Location`, and `Products`, with a total of 12,165 records. A description of each table is as follows:

- `Orders` (Fact Table)
  Contains transactional sales data, including order details, shipping information, customer segment, and financial metrics such as sales, quantity, discount, and profit. It is linked to the Location table via Postal Code and the Products table via `Product ID`.
  
- `Location` (Dimension Table)
  Stores geographic data, including city, state, region, and country. This table allows for the analysis of sales performance across different locations and is linked to the `Orders` table by `Postal Code`.

- `Products` (Dimension Table)  
  Contains product details, including category, subcategory, and product name. It is linked to the `Orders` table via `Product ID`, enabling sales performance analysis by product type.

<p align="center">
    <img src="Visualizations/Sales & Profitability ERD.png" alt="Sales & Profitability ERD" width="450">
</p>

---

## Executive Summary

Sales reached $730K in 2023, a 20% increase from the previous year, with the strongest gains in Q4, particularly in November (up 49% YoY). While revenue growth was strong, profit increased at a slower rate (14% YoY), highlighting pricing and cost challenges. Categories like Phones, Copiers, and Accessories drove profitability, while Machines, Tables, and Envelopes struggled. Strengthening early-year sales, refining pricing strategies, and optimizing underperforming categories could help improve overall profitability.

<p align="center">
    <img src="Visualizations/Sales Performance Dashboard.png" alt="Sales Performance Dashboard" width="725">
</p>
---

## Insights Deep Dive

### Sales and Seasonal Trends
- Sales consistently increased in Q3 and Q4, with November 2023 reaching the highest sales ($118K, up 49.16% YoY).
- February 2023 had the lowest sales ($20K, down 11.65% YoY), reinforcing post-holiday demand weakness.
- Mid-year fluctuations between March and July suggest external market shifts or inconsistent promotional efforts.
- Year-over-year comparisons confirm growth, but some months underperformed despite overall revenue gains.

<p align="center">
    <img src="Visualizations/Total Sales KPI.png" alt="Total Sales KPI" width="750">
</p>

### Profitability Trends and Volatility
- Total profit reached $93K (up 14.24% YoY), but was inconsistent.
- March saw the highest profit ($15K, up 308.42% YoY), potentially due to higher-margin product sales or cost control measures.
- April recorded the lowest profit ($1K, down 68.66% YoY), indicating possible heavy discounting or cost spikes.
- The second half of the year showed more stability, but managing mid-year volatility remains key.

<p align="center">
    <img src="Visualizations/Total Profit KPI.png" alt="Total Profit KPI" width="750">
</p>

### Sales Volume and Demand Patterns
- Total units sold increased by 26.83% YoY, reaching 12K.
- November 2023 had the highest unit sales (1,840, up 30.87% YoY), reinforcing the importance of seasonal promotions.
- Despite February being the lowest in sales, it still saw an 18.63% YoY increase, suggesting improved strategies over 2022.
- Consistent seasonal fluctuations indicate a need for improved off-season sales strategies.

<p align="center">
    <img src="Visualizations/Total Quantity KPI.png" alt="Total Quantity KPI" width="750">
</p>

### Subcategory Performance: Growth vs. Profitability

#### **Top Performers**
- Phones ($105K, +33% YoY), Copiers ($63K, +27% YoY), and Accessories ($60K, +43% YoY) were the highest-performing subcategories, demonstrating both strong revenue growth and profitability.
- Copiers had the highest profit at $25K, showing strong margins even with moderate sales growth.

#### **Challenges in Key Categories**
- Machines ($44K, -22% YoY) and Tables ($61K, +0.1% YoY) remained unprofitable, suggesting issues with pricing, demand, or costs.
- Tables generated $61K in revenue but remained unprofitable with an $8K loss, suggesting a need for pricing adjustments or cost efficiencies.

#### **Moderate Growth but Lower Margins**
- Storage ($70K, +19% YoY) and Chairs ($96K, +14% YoY) saw steady sales growth but weaker profit margins, likely due to higher costs or pricing challenges.

#### **Low-Impact Categories**
- Envelopes ($3K, -29% YoY) and Fasteners ($1K, -11% YoY) continued to see declining sales and minimal profitability.
- These categories contribute little to overall revenue and may need to be discontinued or repositioned if trends continue.

<p align="center">
    <img src="Visualizations/Sales & Profit by Subcategory.png" alt="Sales & Profit by Subcategory" width="750">
</p>

### Weekly Sales and Profit Analysis: 2023 vs. 2022
- Sales improved year-over-year, with 2023 weekly averages at $14K vs. $12K in 2022.
- Q4 was the strongest period in both years, confirming the need for seasonal planning.
- Profitability volatility persisted, despite revenue growth, indicating inefficiencies in pricing or cost management.
- Q1 remained a weak period in both years, requiring targeted marketing and promotions.

<p align="center">
    <img src="Visualizations/2023 Weekly Trends.png" alt="2023 Weekly Trends" width="750">
</p>

<p align="center">
    <img src="Visualizations/2022 Weekly Trends.png" alt="2022 Weekly Trends" width="750">
</p>

---

## Recommendations

### **Boost Q1 Performance**
- Develop early-year promotional strategies to counteract the typical post-holiday slowdown.
- Offer targeted discounts or loyalty incentives in January and February to stimulate demand.

### **Optimize Profitability & Cost Structures**
- Adjust pricing or implement cost-control measures for low-profit subcategories like Machines, Tables, and Bookcases.
- Reassess high-sales but low-margin categories (Storage, Chairs, and Paper) to find opportunities for improved profitability.
- Closely monitor Q2 discounting strategies to maintain a balance between sales volume and profit margins.

### **Leverage Q4 Growth Trends**
- Increase marketing budgets for seasonal promotions in Q4, as November consistently sees the highest sales.
- Improve inventory planning to better align with year-end demand spikes.

### **Refine Pricing and Discounting Strategies**
- Ensure peak sales weeks lead to stronger profitability by minimizing unnecessary discounts.
- Analyze customer purchasing behavior to refine pricing strategies and maximize revenue potential.

---

## Assumptions & Caveats
- This analysis does not account for external factors like economic conditions, consumer behavior shifts, or supply chain disruptions, which may have influenced sales.
- Higher sales volume does not always mean higher profits. Some growth may be due to discounts or increased costs.
- The impact of product lifecycle and competition was not included, so long-term sales trends may be influenced by external market forces.

--- 
- Interactive Tableau Dashboard for exploring sales and profit trends can be found [here.](https://public.tableau.com/app/profile/seana.parker/viz/2023SalesPerformanceDashboard/SalesDashboard#1)
- Raw datasets can be found [here.](Exploration)
- For more of my projects and data journey, visit my portfolio website and reach out!
