# Ecommerce-Dashboard
## Full Project Documentation

The complete project documentation, including dataset processing, dashboard development steps, and detailed explanations, is available on Notion.

🔗 View the full documentation:  
https://resisted-cod-e57.notion.site/E-Commerce-Sales-Customer-Insights-Dashboard-321f8865bed080f28c61f9d5625cf82c?source=copy_link

## **Goal**

We built a **Power BI dashboard** for an **E-Commerce dataset** to **analyze sales performance and customer behavior**, providing insights that help the business track key metrics, monitor trends, and make data-driven decisions.

**Dataset Name:** Global_Ecommerce_Sales.csv

**Description:**

Contains transactional sales data with fields such as : **Transaction Date, Product, Category, Region, Quantity, Revenue, Discount %, and Payment Method.**

**Size:**

500,000 rows × 10 columns

**Source:**

Internal company dataset / simulated data

The full Power BI dashboard file is available in the GitHub repository below.

You can download the `.pbix` file and open it in Power BI Desktop to explore the KPIs, charts, and slicers.

🔗 **GitHub Repository:** https://github.com/Abigaelchemtai/Ecommerce-Dashboard

---

## **1️⃣ Project Overview**

The dashboard provides a comprehensive view of sales across products, regions, and customers. 

It allows users to:

- Track key business metrics (KPIs) at a glance
- Analyze sales trends over time
- Identify top-performing products and regions
- Evaluate the impact of discounts
- Understand customer payment preferences

**Objectives:**

- Track key business metrics (KPIs)
- Visualize trends over time
- Identify top-performing products and regions
- Analyze discounts and payment behavior
- Enable interactive filtering through slicers

---

## **2️⃣ KPIs (Key Business Metrics)**

**These KPIs are displayed as cards at the top of the dashboard for a quick summary.**

Below the dashboard title, the **main KPIs are displayed as cards**. See the uploaded picture below for reference.

| KPI | Description | How Calculated |
| --- | --- | --- |
| Total Revenue | Total money generated | TOTAL REVENUE = SUM(global_ecommerce_sales[Total Revenue]) |
| Total Orders | Number of transactions | TOTAL ORDERS = COUNTROWS(ALL('global_ecommerce_sales')) |
| Total Quantity Sold | Total items sold | TOTAL QUANTITY SOLD = SUM(global_ecommerce_sales[Quantity]) |
| Average Discount | Average discount given | AVERAGE DISCOUNT = AVERAGE(global_ecommerce_sales[Discount (%)]) |

![Dashboard.png](Ecommerce-Dashboard/Dashboard.png)

---

## **3️⃣ Charts & Visualizations**

The dashboard includes interactive charts to explore sales performance and customer behavior. Each chart answers a specific business question:

![Dashboard.png](Ecommerce-Dashboard/Dashboard.png)

| Chart | Purpose | Fields Used | Notes |
| --- | --- | --- | --- |
| Sales Trend (Line Chart) | Shows revenue change over time | Transaction Date, Total Revenue | Trend analysis |
| Revenue by Category (Stack Area Chart) | Compare revenue by product category | Category, Total Revenue | Highlights top-performing categories |
| Top Products (Clustered Bar Chart) | Best-selling products | Product, Total Revenue | Top 10 filter applied |
| Payment Method Distribution (Donut Chart) | Most used payment methods | Payment Method, Count of Orders | Understand customer preferences |
| Category vs Discount (Scatter Chart) | Shows how discounts vary across product categories | Category, Discount%, Total Revenue | Analyzes the effect of discounts per category |
| Sales by Region (Pie Chart) | Shows revenue distribution by region | Region, Total Revenue | Easy comparison of regional contributions |

---

## **4️⃣ Slicers / Filters**

- **Date** – Year, month, or day
- **Category** – Filter by product type
- **Region** – Filter by geographic location
- **Product** – Focus on individual products
- **Quantity** – Filter by units sold
- **Discount %** – Analyze specific discount ranges

All slicers are interactive, allowing dynamic exploration of the dashboard.

So you can filter as per your requirements as shown below.

![slicers.png](Ecommerce-Dashboard/slicers.png)

![filter_by_date.png](Ecommerce-Dashboard/filter_by_date.png)

![filter_by_category.png](Ecommerce-Dashboard/filter_by_category.png)

![filter_by_others.png](Ecommerce-Dashboard/filter_by_others.png)

---

## **5️⃣ Dashboard Layout**

This Power BI dashboard visualizes E-Commerce sales and customer behavior. It includes KPI cards, interactive charts, and slicers to track performance, monitor trends, and explore the dataset dynamically. Users can quickly identify top products, high-performing regions, revenue trends, discount impacts, and payment method preferences.

![Dashboard.png](Ecommerce-Dashboard/Dashboard.png)

---

## **6️⃣ Dataset & Processing Steps**

The dashboard is built using a **global E-Commerce sales dataset**. To prepare the data for analysis, the following steps were performed:

1. **Data Understanding**
    - Reviewed the dataset structure, fields, and data types
    - Identified key metrics: `Revenue`, `Quantity`, `Discount %`, `Orders`, `Region`, `Category`, `Payment Method`
2. **Data Cleaning**
    - Checked for missing or null values and replaced or removed them
    - Formatted dates to a standard format
    - Ensured numeric fields (`Revenue`, `Quantity`, `Discount`) were correctly typed
3. **Data Transformation**
    - Created calculated columns and measures using **DAX**:
        - Total Revenue = Quantity × Unit Price
        - Average Discount = AVERAGE(Discount %)
        - Total Orders = COUNTROWS(Orders Table)
    - Aggregated data where needed for KPIs and visualizations
4. **Validation**
    - Verified all KPIs and charts against raw data for accuracy
    - Ensured totals, averages, and filters return correct results

---

## **7️⃣ Platform & Technologies Used**

- **Platform:** Power BI Desktop – used for dashboard building, visualization, and interactivity
- **Data Modeling & Calculation:** DAX (Data Analysis Expressions)
- **Data Preparation:** Excel / CSV for raw dataset formatting
- **Visualization Features:**
    - KPI cards for high-level metrics
    - Line, bar, pie, scatter, and donut charts for insights
    - Interactive slicers for filtering by all dataset fields
