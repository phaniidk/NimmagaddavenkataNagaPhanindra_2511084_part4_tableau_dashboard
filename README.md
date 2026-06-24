# NimmagaddavenkataNagaPhanindra_2511084_part4_tableau_dashboard

# Tableau Executive Sales Dashboard

## Project Overview

This project focuses on creating an interactive Tableau Executive Dashboard to analyze retail sales performance and support data-driven decision-making.

---

## Business Problem

Organizations generate large volumes of sales data but often struggle to convert it into actionable insights. This dashboard provides visibility into sales trends, profitability, customer behavior, shipping performance, discounts, and product returns.

---

## Dataset Description

The dataset contains information related to:

- Orders
- Customers
- Regions
- Categories
- Sub-Categories
- Sales
- Profit
- Discounts
- Returns
- Shipping Information

### Key Fields

- order_id
- order_date
- ship_date
- customer_segment
- region
- category
- sub_category
- sales
- profit
- discount
- return_flag
- delivery_days

---

## Calculated Fields

### Profit Margin

```text
SUM([profit]) / SUM([sales])
```

### Cost

```text
SUM([sales]) - SUM([profit])
```

### Average Order Value

```text
SUM([sales]) / COUNTD([order_id])
```

### Return Rate

```text
SUM(IF [return_flag]=1 THEN 1 ELSE 0 END)
/ COUNT([order_id])
```

### Shipping Delay Bucket

```text
IF [delivery_days] <= 2 THEN "Fast"
ELSEIF [delivery_days] <= 5 THEN "Normal"
ELSE "Delayed"
END
```

---

## Dashboard Components

### KPI Cards

- Total Sales
- Total Profit
- Profit Margin
- Return Rate

### Visualizations

- Sales Trend View
- Regional Performance View
- Category Profitability View
- Customer Segment View
- Shipping Performance View
- Discount vs Profit View
- Return Analysis View

---

## Dashboard Filters

- Region
- Category
- Customer Segment

---

## Interactive Features

- Cross-filtering between dashboard components
- Dynamic filtering using dashboard controls
- Executive KPI monitoring

---

## Key Insights

1. Sales remain stable throughout the observed period.
2. West region generates the highest sales.
3. Consumer customers contribute the largest revenue share.
4. High discounts reduce profitability.
5. Furniture products have the highest return rates.
6. Shipping efficiency varies significantly across shipping modes.
7. Certain product categories generate substantially higher profits.
8. Operational improvements can increase profitability.

---

## Repository Structure

```text
part4_tableau_dashboard/
│
├── data/
├── tableau/
├── outputs/
├── screenshots/
└── README.md
```

---

## Files Included

### Dataset

- dashboard_sales_data.xlsx

### Tableau Workbook

- executive_dashboard.twbx

### Outputs

- business_insights.md
- dashboard_story.md
- chart_selection_justification.md

### Screenshots

- sales_trend_view.png
- regional_performance_view.png
- category_profitability_view.png
- filter_interaction_view.png
- full_dashboard.png

---

## Conclusion

The Tableau Executive Dashboard successfully provides a comprehensive view of sales performance, profitability, operational efficiency, and customer behavior. The dashboard enables business users to quickly identify trends, risks, and opportunities for growth.
