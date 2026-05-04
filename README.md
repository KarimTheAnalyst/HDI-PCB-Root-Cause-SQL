# HDI PCB Root Cause Analysis Using SQL

## Business Problem
A PCB manufacturer is experiencing yield loss, scrap, and rework in HDI production. The goal is to identify which machines, materials, products, and process factors contribute most to defects and cost.

## Manufacturing Context
This project simulates an HDI PCB manufacturing environment involving multilayer boards, drilling, lamination, plating, surface finish, and process complexity.

## Tools Used
- PostgreSQL
- SQL window functions
- CTEs
- Excel / Power Query
- Power BI
- 
## Data Model
Fact Tables:
- fact_production: production output, defects, scrap, rework, delay indicators
- fact_maintenance: machine maintenance events and cost

Dimension Tables:
- dim_machine
- dim_material
- dim_product
- dim_process
- dim_operator
- dim_customer

## Key KPIs

- Yield Rate = Good Units / Total Units
- Defect Rate = Defective Units / Total Units
- Scrap Rate = Scrapped Units / Total Units
- Rework Rate = Reworked Units / Total Units
- Delay Rate = Delayed Orders / Total Orders
- Cost of Poor Quality (COPQ) = Scrap Cost + Rework Cost

## Analytical Approach
1. Loaded raw manufacturing-style data into staging tables
2. Built clean dimensional tables
3. Created fact tables for production events
4. Calculated manufacturing KPIs
5. Used SQL to identify defect and cost drivers
6. Prepared BI-ready outputs for dashboarding

## Key Insights
- Defect concentration analysis helps identify machines, materials, and products with higher quality risk.
- Higher-complexity HDI boards are more likely to create yield loss, delays, scrap, or rework.
- Scrap and rework directly increase the Cost of Poor Quality (COPQ).
- SQL analysis provides BI-ready outputs for monitoring manufacturing performance.

## Business Impact
This analysis supports better process monitoring, faster root cause investigation, and data-driven decisions to improve yield and reduce cost.

## Recommendations
- Monitor high-risk machines weekly
- Track yield by product complexity
- Investigate repeated defects by material and surface finish
- Use dashboard alerts for abnormal scrap or rework rates

## How to Use This Project
1. Run `01_schema.sql` to create tables.
2. Load the CSV files into PostgreSQL.
3. Run `02_data_quality.sql` to validate the data.
4. Run `03_analysis.sql` to generate KPI and root-cause analysis outputs.
