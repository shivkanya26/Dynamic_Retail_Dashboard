# Dynamic Retail Dashboard in Excel

## Overview
The **Dynamic Retail Dashboard** is an interactive and data-driven tool built in Excel to visualize and analyze retail data. It connects to datasets hosted on GitHub, uses Power Query for data transformation, and presents insights through dynamic charts and KPIs. The dashboard solves key business questions, enabling informed decision-making.

---

## Datasets Used

### 1. **Orders Table**
The Orders table contains details of customer orders, including product, shipping, and financial metrics.

**Sample Data:**
| Order ID       | Returned | Order Date   | Ship Date   | Ship Mode       | Customer Name   | Segment    | Country         | Market | Sales   | Profit   | Discount |
|----------------|----------|--------------|-------------|-----------------|-----------------|------------|-----------------|--------|---------|----------|----------|
| CA-2012-124891 | No       | 31-07-2020   | 31-07-2020  | Same Day        | Rick Hansen     | Consumer   | United States   | US     | 2309.65 | 762.18   | 0        |
| IN-2013-77878  | Yes      | 05-02-2021   | 07-02-2021  | Second Class    | Justin Ritter   | Corporate  | Australia       | APAC   | 3709.40 | -288.77  | 0.1      |
| IN-2013-71249  | No       | 17-10-2021   | 18-10-2021  | First Class     | Craig Reiter    | Consumer   | Australia       | APAC   | 5175.17 | 919.97   | 0.1      |

### 2. **Returns Table**
Tracks orders that have been returned, along with the associated markets.

**Sample Data:**
| Returned | Order ID         | Market         |
|----------|------------------|----------------|
| Yes      | MX-2013-168137   | LATAM          |
| Yes      | US-2011-165316   | LATAM          |
| Yes      | ES-2013-1525878  | EU             |
| Yes      | CA-2013-118311   | United States  |

### 3. **People Table**
Contains details about sales representatives and their respective regions.

**Sample Data:**
| Person              | Region          |
|---------------------|-----------------|
| Anna Andreadi       | Central         |
| Chuck Magee         | South           |
| Kelly Williams      | East            |
| Matt Collister      | West            |
| Deborah Brumfield   | Africa          |

---

## Problem Statements Solved with Steps

### 1. **Key Performance Indicators (KPIs)**
   **Objective:** Calculate and display Total Sales, Total Profit, Total Quantity, Number of Orders, and Profit Margin dynamically.

   **Steps:**
   1. Import the **Orders Table** into Excel using Power Query.
   2. Create calculated columns for:
      - `Profit Margin` = `Profit / Sales`.
      - `Total Orders` = Count of `Order ID`.
   3. Use Excel formulas to calculate:
      - `Total Sales` = `=SUM(Sales)`.
      - `Total Profit` = `=SUM(Profit)`.
      - `Total Quantity` = `=SUM(Quantity)`.
   4. Build a dynamic KPI table and use symbols to enhance visual appeal.

![image](https://github.com/user-attachments/assets/c2dee0c5-5fd6-4802-9bfa-811394978bed)

---

### 2. **Sales and Profit Analysis**
   **Objective:** Visualize sales and profit trends over time to identify patterns.

   **Steps:**
   1. Create a **Pivot Table** with `Order Date` grouped by Year and Month.
   2. Add `Sales` and `Profit` as values.
   3. Create a **Line Chart** to display trends for Sales and Profit.
   4. Apply slicers to filter by category, market, or region dynamically.
<img width="558" height="432" alt="image" src="https://github.com/user-attachments/assets/8b80e843-8582-4bdd-adf9-d067ebbe7fee" />

---

### 3. **Category-Wise Profit**
   **Objective:** Analyze profitability across product categories.

   **Steps:**
   1. Create a **Pivot Table** using `Category` as rows and `Profit` as values.
   2. Sort the table in descending order of Profit.
   3. Create a **Bar Chart** to visualize category-wise profit.
   4. Add slicers for interactivity.
<img width="478" height="442" alt="image" src="https://github.com/user-attachments/assets/68dc78f6-56a6-4324-80f4-947141b3dccb" />

---

### 4. **Segment-Wise Sales Share (%)**
   **Objective:** Display the proportion of sales for each customer segment.

   **Steps:**
   1. Create a **Pivot Table** with `Segment` as rows and `Sales` as values.
   2. Calculate percentage share using `=Sales / Total Sales * 100`.
   3. Create a **Pie Chart** or **Donut Chart** to display the sales share.
   4. Add labels to show percentage values dynamically.
<img width="471" height="448" alt="image" src="https://github.com/user-attachments/assets/fa373789-4d7f-4556-b258-839a05784e79" />

---

### 5. **Sales by Country**
   **Objective:** Analyze sales performance by country.

   **Steps:**
   1. Create a **Pivot Table** with `Country` as rows and `Sales` as values.
   2. Sort the table in descending order of Sales.
   3. Use conditional formatting or a **Heatmap** to highlight top-performing countries.
<img width="697" height="437" alt="image" src="https://github.com/user-attachments/assets/b34f3a4b-8947-46d0-84c5-9a498c80b20c" />

---

### 6. **Top 5 Subcategories**
   **Objective:** Identify the top 5 performing subcategories.

   **Steps:**
   1. Create a **Pivot Table** with `Sub-Category` as rows and `Sales` as values.
   2. Sort the table in descending order of Sales.
   3. Filter to display the top 5 Sub-Categories.
   4. Use a **Column Chart** to visualize results.
<img width="568" height="428" alt="image" src="https://github.com/user-attachments/assets/0497f915-843a-4d1b-8361-9cd90d5d5a87" />

---

## Dynamic Features
The dashboard includes:
1. **Dynamic Charts:** Update in real-time based on slicer inputs.
2. **Power Query Integration:** Automates data cleaning and transformation.
3. **KPI Table:** Highlights critical metrics at a glance.

---

## Next Steps for Extension
Additional insights to enhance the dashboard:
1. **Return Analysis:** Investigate return rates by market or product category.
2. **Top and Bottom Customers:** Identify most and least profitable customers.
3. **Market Analysis:** Compare performance across different markets.
4. **Product Analysis:** Evaluate individual product contributions.

---

## Significance
This dashboard empowers retail businesses to:
- Track performance through KPIs.
- Understand category, segment, and geographic trends.
- Make data-driven decisions to optimize operations.

---

## Visuals
This repository includes:
- Visual examples for each solved problem statement.
- Snapshots of the final dashboard with all components.
