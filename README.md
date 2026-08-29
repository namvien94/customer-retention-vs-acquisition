# Customer Retention vs. Acquisition Analysis

## The Decision

Should the business continue relying on new customer acquisition for growth, or invest more heavily in increasing revenue from existing customers?

This analysis examines 22K+ customers and approximately $30M in retail revenue using SQL and Tableau.  
The findings show that new customers generate the largest share of revenue, but average revenue per customer remains nearly flat across customer segments, suggesting that growth is being driven by customer volume rather than increasing customer value.

The analysis also identifies two important revenue risks: **heavy concentration among customers ages 18–34** and **dependence on a single top-performing brand**.

## What the Business Needs to Know

| Total Revenue | Customers | New Customer Revenue | Avg. Sales per Customer |
|---|---:|---:|---:|
| ~$30M | 22K+ | ~$12M / 40% | ~$1,370 |

New customers generate the largest share of revenue, but average sales per customer remain approximately $1,370 across customer segments. This suggests that revenue growth depends primarily on acquiring more customers rather than increasing the value generated from existing relationships.

Revenue is also highly concentrated among customers ages 18–34, while one brand alone contributes approximately $8.5M, or 28%, of total revenue.

![Sales by Age, Gender, and Income](https://github.com/namvien94/customer-retention-vs-acquisition/blob/main/images/sales-by-age-gender-and-income.png?raw=true)

## Explore the Dashboard

Two linked, interactive Tableau dashboards support the recommendations above. Filtering by brand on one dashboard updates the customer demographics view on the other, so a stakeholder can trace any recommendation back to the underlying data.

🔗 [View live dashboard on Tableau Public](https://public.tableau.com/views/CustomerSalesPerformanceAnalysis/SalesDashboard?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

![Sales Dashboard](https://github.com/namvien94/customer-retention-vs-acquisition/blob/main/images/sales-dashboard.png?raw=true)

![Customer Dashboard](https://github.com/namvien94/customer-retention-vs-acquisition/blob/main/images/customer-dashboard.png?raw=true)

## Recommended Actions

### 1. Test retention and cross-sell strategies for existing customers

New customers generate approximately $12M, or 40% of total revenue, yet average sales per customer remain near $1,370 across New, Regular, and Premium segments. This suggests that higher revenue from new customers is driven primarily by customer volume rather than greater customer value.

Test loyalty, bundling, or cross-sell offers designed to increase spending among existing customers. Measure changes in average sales per customer and incremental revenue to determine whether retention investment can generate growth without a proportional increase in acquisition activity.

![Average Sales Per Customer](https://github.com/namvien94/customer-retention-vs-acquisition/blob/main/images/average-sales-per-customer.png?raw=true)

### 2. Reduce revenue concentration among customers ages 18–34

Customers ages 18–34 account for the large majority of revenue, while contribution declines sharply among older customer groups.  
This concentration creates exposure if demand or purchasing behavior changes within the business's dominant demographic.

Test targeted campaigns for underrepresented customer groups, particularly ages 35–54, and measure customer acquisition, conversion, and incremental revenue before expanding the strategy.

![Sales by Age, Gender, and Income 35-54](https://github.com/namvien94/customer-retention-vs-acquisition/blob/main/images/sales-by-age-gender-and-income-35-54.png?raw=true)

### 3. Target acquisition efforts during seasonal revenue dips

Revenue declines in several months align more closely with lower customer counts than with lower average spending per customer.  
This suggests that the declines are primarily associated with customer traffic rather than reduced customer value.

Test targeted acquisition campaigns during historically weaker months and measure incremental customers and revenue before considering broader pricing or product changes.

![Sales vs. Customers](https://github.com/namvien94/customer-retention-vs-acquisition/blob/main/images/sales-customers.png?raw=true)

### 4. Reduce brand concentration risk

The highest-revenue brand generates approximately $8.5M, or 28% of total revenue, substantially more than any other brand.  
This creates meaningful revenue concentration around a single source.

Evaluate growth opportunities among the next-highest-revenue brands through targeted merchandising or promotional tests, and monitor whether revenue becomes less concentrated over time.

![Top Brands](https://github.com/namvien94/customer-retention-vs-acquisition/blob/main/images/top-brands.png?raw=true)

## How I Built It

- **SQL:** Joined customer and transaction data and used aggregations, CASE WHEN logic, CTEs, and window functions including RANK() and LAG() to analyze customer segments, brand performance, and month-over-month trends.
- **Databricks:** Developed and documented SQL analysis in a notebook environment for reproducible exploration and validation.
- **Tableau:** Built two linked interactive dashboards with cross-dashboard filtering, Top N parameters, calculated fields, demographic segmentation, and highest/lowest month highlighting.
- **Tools:** SQL, Databricks, Tableau
