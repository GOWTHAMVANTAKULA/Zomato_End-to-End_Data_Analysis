# Zomato_End-to-End_Data_Analysis
End-to-end data analysis project using food delivery data processed in PostgreSQL. Performed data cleaning and business analysis using SQL with aggregations and ranking logic. Integrated results into Microsoft Excel via ODBC to build an interactive dashboard delivering revenue and city-level insights.

**Project Architecture :**
            ┌─────────────────────┐
            │     Raw CSV Data    │
            └──────────┬──────────┘
                       │
                       ▼
            ┌─────────────────────┐
            │   PostgreSQL DB     │
            │ (Data Storage Layer)│
            └──────────┬──────────┘
                       │
                       ▼
            ┌─────────────────────┐
            │  Data Cleaning &    │
            │  Feature Engineering│
            │                     │
            └──────────┬──────────┘
                       │
                       ▼
            ┌─────────────────────┐
            │  Business Analysis  │
            │  (15 SQL Queries)   │
            └──────────┬──────────┘
                       │
                       ▼
            ┌─────────────────────┐
            │     ODBC Bridge     │
            │ (Database → Excel)  │
            └──────────┬──────────┘
                       │
                       ▼
            ┌─────────────────────┐
            │   Excel Dashboard   │
            │ (KPIs, Charts,      │
            │  Slicers, Insights) │
            └──────────┬──────────┘
                       │
                       ▼
            ┌─────────────────────┐
            │  Business Insights  │
            │ & Decision Support  │
            └─────────────────────┘


**End-to-End Workflow**

1. Data Engineering in PostgreSQL

- Raw CSV data was imported into PostgreSQL for structured storage and analysis.

2. Data Processing Included:

- Data type standardization

- Handling missing values

- Date formatting and transformation

- Category normalization

- Creation of derived metrics (revenue-based measures)

- Feature engineering for business insights

3.  SQL Analysis 

- Total Revenue & Order Volume

- Advanced SQL concepts used:

- GROUP BY and Aggregations

- CASE WHEN

- RANK() / ROW_NUMBER() window functions

- Conditional filtering

- Sorting and top-N analysis

4.  ODBC Integration

An ODBC connection was established between PostgreSQL and Microsoft Excel to dynamically extract processed data. This enabled seamless transition from backend analytics to front-end dashboard visualization.

5.  Dashboard Overview & Business Insights

The Excel dashboard provides an interactive, decision-support view of business performance.

**🔹 Key KPIs**

1. Total Sales: ₹ 53.01 Cr

2. Total Orders: 197,430

3. Average Spend: ₹ 268.51

4. Average Rating: 4.34

These KPIs indicate strong transaction volume with healthy customer satisfaction levels.

🔹 Monthly Sales Trend

- Stable revenue performance across initial months.

- Significant drop observed in later months, suggesting possible seasonality or reduced order volume.

- Indicates need for promotional campaigns during low-performing periods.

🔹 Market Spread Across Cities

- Certain metropolitan cities dominate revenue contribution.

- Restaurant density does not always directly correlate with revenue, indicating demand concentration in specific markets.

- High-performing cities represent strong expansion opportunities.

🔹 Top 10 Performing Restaurants

- Revenue concentration is visible among top brands.

- Ranking logic identifies high-value contributors.

- Suggests strong brand dominance in the food delivery ecosystem.

🔹 Cuisine Demand Insights

- Non-Veg category shows highest demand.

- Fast Food and Veg Meals follow as major contributors.

- Lower demand categories may require targeted marketing strategies.

🎯 Business Impact

1. Identify revenue-driving cities

2. Optimize category-based promotions

3. Detect seasonal fluctuations

4. Recognize top-performing restaurant brands

5. Support strategic expansion decisions

**Conclusion :**
This project successfully demonstrates an end-to-end data analytics workflow, from data cleaning and transformation in PostgreSQL to interactive dashboard development in Microsoft Excel. The analysis uncovered key insights into revenue trends, city-level performance, restaurant rankings, and cuisine demand patterns. The dashboard enables dynamic exploration of business metrics to support data-driven decisions. Overall, the project highlights strong SQL, analytical, and business intelligence capabilities.
