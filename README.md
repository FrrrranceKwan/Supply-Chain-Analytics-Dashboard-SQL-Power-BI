# Supply-Chain-Analytics-Dashboard-SQL-Power-BI
A Power BI Project for Omnichannel, Sell-through, and Inventory Health AnalysisA Power BI Project for Omnichannel, Sell-through, and Inventory Health Analysis

📌 Project Overview

This project simulates a real-world Luxury Retail Supply Chain Dashboard inspired by the business context of Company’s South Asia Supply Chain team.
The dashboard is designed to support:
	•	Omnichannel order performance monitoring
	•	Sell-through analysis & product performance review
	•	Inventory aging and stock optimization
	•	Store-level inventory comparison for rebalancing actions

The Power BI report includes two pages:
	1.	Page 1 — Orders & Omnichannel Performance
	2.	Page 2 — Sell-through & Inventory Health

All datasets used are synthetically generated for learning purposes.

⸻

🗂 Project Files
📁 LV-Supply-Chain-Dashboard/
│
├── data/
│   ├── dim_products.csv
│   ├── dim_stores.csv
│   ├── fact_orders.csv
│   ├── fact_inventory_monthly.csv
│
├── pbix/
│   └── Supply Chain Analysis_GUAN.pbix
│── pdf/
│   └── Supply Chain Analysis_GUAN.pdf
└── README.md

📊 Dashboard Pages

⸻

📌 Page 1 — Orders & Omnichannel Performance

This page focuses on client order management, fulfillment efficiency, and monthly operational stability.

🔹 KPIs Included
	•	Total Orders
	•	Fulfillment Rate
	•	Cancellation Rate
	•	Average Lead Time
	•	Date Slicer

🔹 Visuals
	•	Orders by Channel
	•	Order Status Breakdown
	•	Average Lead Time Trend
	•	Optional: Orders by Country

🔹 Business Insights
Insight 1 — Fulfillment Performance
Orders show stable fulfilment levels across the year, with occasional increases in lead time 
suggesting seasonal demand fluctuations. Monitoring peak months can improve response time.

Insight 2 — Channel Contribution
Boutique remains the dominant channel, while E-commerce and Omni channels show steady activity.
Understanding channel behaviour helps optimize staffing and stock allocation.

📌 Page 2 — Sell-through & Inventory Health

This page evaluates product performance, inventory freshness, and rebalancing opportunities.

🔹 KPIs
	•	Units Sold (YTD)
	•	Top Seller Contribution
	•	Total Inventory
	•	Aged Stock % (>60 days)

🔹 Visuals
	•	Top 10 Best Selling SKUs
	•	Bottom 10 Slowest SKUs
	•	Sales Distribution by Category
	•	Inventory Aging Distribution
	•	Store Inventory Comparison

🔹 Business Insights
Insight 1 — Sales Concentration
Sell-through is concentrated in a small number of SKUs, while many products contribute minimally.
This indicates product dependency risk and suggests opportunities for targeted rebalancing.

Insight 2 — Inventory Aging Risk
Aged inventory (>60 days) is accumulating in several stores. This increases holding cost and 
reduces sell-through efficiency. Store-level rebalancing and SKU-level review are recommended.

🧪 Data Model

The data model follows a clean Star Schema:

Dimensions
	•	dim_products — SKU-level attributes
	•	dim_stores — Store and country information

Fact Tables
	•	fact_orders — Order transactions (channels, dates, fulfillment, quantities)
	•	fact_inventory_monthly — Monthly inventory snapshots and aging

Relationships
products (1) ──── (*) orders
stores   (1) ──── (*) orders
products (1) ──── (*) inventory
stores   (1) ──── (*) inventory

🔧 Technologies Used
	•	SQL for Data Calculation & Cleaning
  •	Power BI Desktop
	•	DAX (Data Analysis Expressions)
	•	Power Query
	•	Synthetic data generation (Python)
	•	Data modeling (Star Schema best practices)

⸻

🚀 Key Learning Outcomes

This project demonstrates ability to:
	•	Design end-to-end BI dashboards aligned with real business JD
	•	Model relational data for analytics
	•	Create DAX KPIs including ranking, contribution %, and aging logic
	•	Perform supply chain visual analytics: sell-through, fulfillment, aging
	•	Communicate insights through dashboard storytelling
