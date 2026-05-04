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

## Key KPIs
- Yield rate
- Defect rate
- Scrap rate
- Rework rate
- Cost of poor quality
- Delay rate

## Analytical Approach
1. Loaded raw manufacturing-style data into staging tables
2. Built clean dimensional tables
3. Created fact tables for production events
4. Calculated manufacturing KPIs
5. Used SQL to identify defect and cost drivers
6. Prepared BI-ready outputs for dashboarding

## Key Insights
- Defects are concentrated in specific machines, products, or process conditions
- Higher-complexity HDI boards show higher risk of defects and delays
- Scrap and rework create measurable cost impact

## Business Impact
This analysis supports better process monitoring, faster root cause investigation, and data-driven decisions to improve yield and reduce cost.

## Recommendations
- Monitor high-risk machines weekly
- Track yield by product complexity
- Investigate repeated defects by material and surface finish
- Use dashboard alerts for abnormal scrap or rework rates
