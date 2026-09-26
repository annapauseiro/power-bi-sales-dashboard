# Sales Performance Dashboard (Power BI) 📈

An interactive Power BI report analyzing sales, customer, and product performance across four regions, 2011–2014. It's the reporting layer of a wider portfolio project that takes a SQL-based sales/CRM/ERP data warehouse and turns it into a single-page, filter-driven view of the business.


<img width="1102" height="734" alt="dashboard-overview" src="https://github.com/user-attachments/assets/dd8a2771-fe1d-4796-a7a4-0df13ce0ade5" />

## 🗄️ Data source

The report connects to the **Gold layer** (star schema) of the [`sql-data-warehouse-project`](https://github.com/annapauseiro/sql-data-warehouse-project) repository, built with a Bronze → Silver → Gold (Medallion) architecture in SQL Server:

- `gold.fact_sales` — order-level sales transactions
- `gold.dim_customers` — customer attributes and country
- `gold.dim_products` — product name and category

Data is imported into the Power BI model, so the `.pbix` file is self-contained and opens directly in Power BI Desktop without a live connection to the source database.

## ⚙️ Features

- **KPI cards** — total orders, total customers, and total sales, all filter-aware
- **Quarterly sales trend** — a line chart tracking `gold.fact_sales` by year and quarter, 2011–2014
- **Category breakdown** — a donut chart showing revenue share by product category
- **Product ranking** — a horizontal bar chart of total sales by product
- **Cross-filtering slicers** — country, order date (range), and category, all driving every visual on the page

## 🛠️ Tools & techniques

- Power BI Desktop — data modeling and report design
- Power Query — shaping the Gold-layer tables on load
- Implicit (column-based) aggregations for the current KPIs and charts, with a move to explicit DAX measures planned next

## 🗺️ Roadmap

- Port the existing SQL analytical logic (trends, segmentation, cumulative and part-to-whole metrics) into explicit DAX measures
- Add AI-generated narrative summaries via Microsoft Copilot

## 🧠 Skills demonstrated

Data modeling, Power Query, dashboard design, KPI reporting, cross-filtering/interactivity design.

## 🔗 Related repositories

- [`sql-data-warehouse-project`](https://github.com/annapauseiro/sql-data-warehouse-project) — Bronze/Silver/Gold data warehouse this report is built on
- [`sql-data-analytics-project`](https://github.com/annapauseiro/sql-data-analytics-project) — SQL exploratory analysis (trends, segmentation, cumulative and part-to-whole metrics)

---
## 👩‍💻 About Me

Hey there! I’m Anna Pauseiro, an IT professional passionate about data and the stories we can tell through it.

