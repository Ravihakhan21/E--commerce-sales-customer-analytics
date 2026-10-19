# Project Brief: E-commerce Sales & Customer Analytics

## 1. Business context
An online marketplace generates data across orders, order items, customers, products, payments, sellers, delivery, and customer reviews. These records can help a business understand sales performance and the customer experience, but only when the data is checked and analyzed systematically.

## 2. Problem statement
The business needs evidence-based answers about order and sales performance, product/category contribution, payment behavior, delivery outcomes, and customer reviews. Without a structured view, it is difficult to identify which areas deserve further investigation and which operational or customer-experience improvements may be worthwhile.

This project will use the Olist public dataset to investigate these areas and produce clear, evidence-backed recommendations.

## 3. Project objectives
1. Understand the dataset structure and the relationships between tables.
2. Validate data quality before drawing conclusions.
3. Measure order activity and sales value using clearly documented definitions.
4. Compare product/category performance.
5. Explore payment behavior, delivery outcomes, and review scores.
6. Investigate customer purchasing patterns where the data permits.
7. Present the most useful results in a Power BI dashboard.
8. Translate verified findings into practical business recommendations.

## 4. Stakeholders and decisions
- **E-commerce/business manager:** understand order and sales trends.
- **Merchandising/product team:** identify categories and products that contribute to sales.
- **Operations/delivery team:** investigate delivery delays and order outcomes.
- **Customer experience team:** explore review patterns and potential service issues.
- **Marketing/CRM team:** use supported customer and sales insights to inform future questions; campaign effectiveness cannot be measured without suitable campaign data.

## 5. Initial KPIs and definitions
Definitions will be confirmed after schema inspection.

- **Order count:** count of distinct order IDs, with included statuses stated explicitly.
- **Sales value:** sum of order-item price; freight/shipping value will be shown separately unless a clearly documented alternative is used.
- **Average order value (AOV):** defined sales value divided by the relevant distinct order count; exclusions and status rules must be stated.
- **Product/category contribution:** order-item sales value grouped by product or category.
- **Delivery time:** difference between purchase timestamp and delivered timestamp, for valid delivered orders.
- **Late delivery rate:** delivered orders whose actual delivery timestamp is later than the estimated delivery timestamp, divided by eligible delivered orders.
- **Average review score:** average recorded review score, with missing reviews handled transparently.
- **Payment mix:** payment records or order-level payment totals grouped by payment type; avoid double-counting orders with multiple payment rows.

## 6. Scope
### In scope
- Data inspection and quality checks
- SQL-based descriptive analysis
- Sales, product/category, payment, delivery, and review analysis
- Customer purchase patterns where supported
- Power BI dashboard
- Documented insights and recommendations

### Out of scope for this dataset alone
- Reliable paid-campaign CTR, CPC, CAC, or ROAS without campaign impressions, clicks, spend, and conversion data
- Causal claims about why customers behave a certain way
- Treating historical records as current market performance

## 7. Starter business questions
1. How many unique orders are in the dataset?
2. What is the order-status distribution?
3. How does order volume change over time?
4. What is the sales value from order items?
5. Which product categories contribute the most sales value?
6. Which products contribute the most sales value?
7. How does freight value vary across orders or regions?
8. Which payment types are most frequently used?
9. How are payment installments distributed?
10. What is the average order value under a clearly defined order scope?
11. What is the delivery-time distribution?
12. What percentage of eligible delivered orders arrived late?
13. Are late deliveries associated with lower review scores?
14. What is the distribution of review scores?
15. Which states or cities account for the most customers/orders, subject to location data quality?
16. What proportion of orders are canceled or unavailable?
17. Are there products/categories with unusually high freight relative to item price?
18. What data-quality issues should be resolved or disclosed?
19. Can repeat purchasing be measured reliably from customer/order identifiers?
20. Which evidence-backed business actions should be prioritized?

These questions are provisional. They will be refined after inspecting columns, data types, table grain, and join keys.

## 8. Method
1. Inspect the CSV files and record each table's grain and columns.
2. Create/import tables into MySQL.
3. Check nulls, duplicates, key consistency, and date ranges.
4. Define metric logic before writing each query.
5. Run SQL analyses and save queries plus outputs.
6. Build visuals from validated results.
7. Write recommendations that connect a finding to an action and a measurable follow-up KPI.

## 9. Deliverables
- Data dictionary / schema notes
- SQL scripts
- Data-quality checks
- Results and interpretation
- Power BI dashboard and screenshots
- Final README with limitations and recommendations

## 10. Success criteria
The project is complete when another person can understand the problem, reproduce the main queries, see the evidence behind each finding, and understand the limits of the conclusions.

## 11. Current status
Dataset downloaded and extracted locally. Table inspection, SQL import, analysis, dashboarding, and findings are not yet complete.
