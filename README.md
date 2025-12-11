Markdown

# Supply Chain Analytics Dashboard (SQL + Power BI)

## 📌 Project Overview
This project simulates a real-world **Luxury Retail Supply Chain Dashboard**, inspired by the business context of a South Asia Supply Chain team. 

The dashboard is designed to support high-level decision-making in:
* **Omnichannel order performance monitoring**
* **Sell-through analysis & product performance review**
* **Inventory aging and stock optimization**
* **Store-level inventory comparison for rebalancing actions**

The report provides a comprehensive view of supply chain health, moving from order fulfillment efficiency to deep-dives into inventory risks.

> **Note:** All datasets used in this project are synthetically generated for learning and demonstration purposes.

---

## 🗂 Project Files

```text
📁 LV-Supply-Chain-Dashboard/
│
├── 📂 data/
│   ├── dim_products.csv           # SKU-level attributes
│   ├── dim_stores.csv             # Store and country information
│   ├── fact_orders.csv            # Order transactions (channels, dates, fulfillment)
│   ├── fact_inventory_monthly.csv # Monthly inventory snapshots and aging
│
├── 📂 pbix/
│   └── Supply Chain Analysis_GUAN.pbix  # Power BI Source File
│
├── 📂 pdf/
│   └── Supply Chain Analysis_GUAN.pdf   # Static Report Export
│
└── README.md
📊 Dashboard Pages
1️⃣ Page 1: Orders & Omnichannel Performance
Focus: Client order management, fulfillment efficiency, and monthly operational stability.

🔹 Key Performance Indicators (KPIs)
Total Orders

Fulfillment Rate %

Cancellation Rate %

Average Lead Time (Days)

🔹 Visuals
Orders by Channel (Boutique vs. E-commerce vs. Omni)

Order Status Breakdown

Average Lead Time Monthly Trend

Optional: Orders by Country

💡 Business Insight 1 — Fulfillment Performance Orders show stable fulfillment levels across the year. However, occasional increases in lead time suggest seasonal demand fluctuations. Recommendation: Monitoring peak months closely can improve response times and customer satisfaction.

💡 Business Insight 2 — Channel Contribution Boutique remains the dominant channel, while E-commerce and Omni channels show steady activity. Recommendation: Understanding channel behavior helps optimize staffing and stock allocation specific to channel needs.

2️⃣ Page 2: Sell-through & Inventory Health
Focus: Evaluating product performance, inventory freshness, and rebalancing opportunities.

🔹 Key Performance Indicators (KPIs)
Units Sold (YTD)

Top Seller Contribution %

Total Inventory Units

Aged Stock % (>60 days)

🔹 Visuals
Top 10 Best Selling SKUs

Bottom 10 Slowest Moving SKUs

Sales Distribution by Category

Inventory Aging Distribution (<30 days to >90 days)

Store Inventory Comparison

💡 Business Insight 1 — Sales Concentration Sell-through is highly concentrated in a small number of SKUs (Pareto Principle), while many products contribute minimally. Risk: High product dependency. Recommendation: Targeted rebalancing or markdown strategies for slow movers.

💡 Business Insight 2 — Inventory Aging Risk Aged inventory (>60 days) is accumulating in specific stores. Risk: Increased holding costs and reduced sell-through efficiency. Recommendation: Immediate store-level rebalancing and SKU-level review are required to clear aged stock.

🧪 Data Model
The data model follows a clean Star Schema to ensure optimal performance and accurate filtering.

Tables
Dimensions: dim_products, dim_stores

Facts: fact_orders, fact_inventory_monthly

Entity Relationship Diagram (ERD) logic
Plaintext

(Dimension)          (Fact)
dim_products (1) ──── (*) fact_orders
dim_stores   (1) ──── (*) fact_orders

dim_products (1) ──── (*) fact_inventory_monthly
dim_stores   (1) ──── (*) fact_inventory_monthly
🔧 Technologies Used
SQL: For data calculation, validation, and cleaning.

Power BI Desktop: For dashboard design and visualization.

DAX (Data Analysis Expressions): For complex measures (Ranking, Contribution %, Aging Logic).

Power Query: For ETL (Extract, Transform, Load) processes.

Python: Used for synthetic data generation.

Data Modeling: Implemented Star Schema best practices.

🚀 Key Learning Outcomes
Through this project, I demonstrated the ability to:

Design End-to-End Solutions: Built a BI dashboard aligned with real-world Job Descriptions (JD) for Supply Chain roles.

Data Modeling: Modeled relational data effectively for analytics.

Advanced DAX: Created dynamic KPIs including ranking logic, contribution percentages, and inventory aging buckets.

Visual Analytics: Performed specific supply chain analyses: Sell-through rate, Fulfillment efficiency, and Inventory aging.

Storytelling: Communicated actionable business insights derived from data.
