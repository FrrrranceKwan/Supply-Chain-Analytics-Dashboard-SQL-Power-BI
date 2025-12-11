# 📦 Supply Chain Analytics Dashboard

![Power Bi](https://img.shields.io/badge/power_bi-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![SQL](https://img.shields.io/badge/sql-003B57?style=for-the-badge&logo=mysql&logoColor=white)
![Python](https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

> **A Strategic Dashboard for Omnichannel, Sell-through, and Inventory Health Analysis.**

---

## 📖 Table of Contents
- [📌 Project Background](#-project-background)
- [📊 Dashboard Showcase](#-dashboard-showcase)
- [💡 Key Business Insights](#-key-business-insights)
- [⚙️ Data Architecture](#-data-architecture)
- [📂 Project Structure](#-project-structure)
- [🚀 How to Use](#-how-to-use)

---

## 📌 Project Background

This project simulates a real-world **Luxury Retail Supply Chain Dashboard**, designed to address specific operational challenges faced by the South Asia Supply Chain team.

The primary objective is to move beyond simple reporting to **actionable analytics**, focusing on:
1.  **Fulfillment Efficiency:** Monitoring Lead Time and Fill Rate.
2.  **Channel Performance:** Comparing Boutique vs. E-commerce vs. Omni metrics.
3.  **Inventory Health:** Identifying aged stock risks and rebalancing opportunities.

*Note: All datasets are synthetically generated for demonstration purposes.*

---

## 📊 Dashboard Showcase

### 1️⃣ Page 1: Orders & Omnichannel Performance
*Focus: Operational stability, Order fulfillment, and Channel split.*

![Insert Screenshot of Page 1 Here](https://via.placeholder.com/800x450?text=Please+Upload+Your+Dashboard+Screenshot+Here)
*(Replace the link above with your actual screenshot)*

**Key Metrics Tracked:**
* `Total Orders` | `Fulfillment Rate %` | `Cancellation Rate %` | `Avg Lead Time (Days)`

---

### 2️⃣ Page 2: Sell-through & Inventory Health
*Focus: Product lifecycle, Stock aging risks, and Store-level distribution.*

(https://via.placeholder.com/800x450?text=Please+Upload+Your+Dashboard+Screenshot+Here)
*(Replace the link above with your actual screenshot)*

**Key Metrics Tracked:**
* `Units Sold (YTD)` | `Top Seller Contribution %` | `Aged Stock % (>60 Days)`

---

## 💡 Key Business Insights

The analysis revealed several critical findings that drive business decisions:

> **📉 The "Pareto" Risk**
> Sell-through is highly concentrated. A small percentage of SKUs drive the majority of revenue.
> * **Action:** Review the "Long Tail" products for markdown or de-listing to free up working capital.

> **⏳ Inventory Aging Alert**
> There is a significant accumulation of stock aged **>60 days** in specific boutique locations, increasing holding costs.
> * **Action:** Initiate immediate store-to-store transfers (rebalancing) to move aged stock to high-traffic locations.

> **🚚 Lead Time Seasonality**
> Average lead time spikes during peak promotional months.
> * **Action:** Adjust staffing rosters and logistics capacity planning 2 months prior to forecasted peaks.

---

## ⚙️ Data Architecture

The project utilizes a **Star Schema** to ensure optimal performance in Power BI.

### Entity Relationship Diagram (ERD)
*(GitHub will render this diagram automatically)*

```mermaid
erDiagram
    DIM_PRODUCTS ||--o{ FACT_ORDERS : "contains"
    DIM_STORES   ||--o{ FACT_ORDERS : "fulfills"
    DIM_PRODUCTS ||--o{ FACT_INVENTORY : "stocks"
    DIM_STORES   ||--o{ FACT_INVENTORY : "stores"

    DIM_PRODUCTS {
        string SKU
        string Category
        string Collection
    }
    DIM_STORES {
        string StoreID
        string Country
        string Channel
    }
    FACT_ORDERS {
        date OrderDate
        int Quantity
        string Status
        int LeadTime
    }
    FACT_INVENTORY {
        date SnapshotDate
        int Quantity
        string AgingBucket
    }
📂 Project Structure
Plaintext

📁 Supply-Chain-Dashboard/
│
├── 📂 data/                   # Raw CSV files
│   ├── dim_products.csv
│   ├── dim_stores.csv
│   ├── fact_orders.csv
│   └── fact_inventory_monthly.csv
│
├── 📂 pbix/                   # Power BI Source File
│   └── Supply Chain Analysis_GUAN.pbix
│
├── 📂 assets/                 # Screenshots & Icons for README
│   ├── dashboard_p1.png
│   └── dashboard_p2.png
│
└── README.md
