# End-to-End Brazilian E-Commerce Supply Chain & Predictive Analytics Suite

## 📌 Project Overview
As a Data Analyst, I engineered an end-to-end data pipeline and a 3-page interactive analytics suite analyzing **75K+ transactions** from a Brazilian e-commerce platform. This project goes beyond basic reporting by integrating enterprise relational databases, Python-driven ETL pipelines, and advanced data science modeling (Market Basket Analysis) to optimize supply chains and drive cross-selling strategies.

---

## 📂 Data Architecture & Pipeline Workflow
The project architecture successfully reflects a real-world enterprise data lifecycle across four distinct stages:

[ SQL Server (SSMS) ]│▼  (Extraction via pyodbc)[ Jupyter Notebook ] ──➔ (EDA, Data Wrangling, & Preprocessing)│▼  (Automated ETL Script Loading)[ Power BI Desktop ] ──➔ (DAX Modeling: Support, Confidence, Lift)│▼[ Executive Dashboard Suite ]


1. **Database Warehousing (SSMS)**: Ingested and structured the raw relational e-commerce tables within SQL Server Management Studio (SSMS).
2. **Programmatic Extraction (`pyodbc`)**: Established a secure database connection inside a Jupyter Notebook using the `pyodbc` driver to extract the relational data into Python data structures.
3. **Data Preprocessing & Wrangling**: Utilized Python (`Pandas`, `NumPy`) inside the notebook to conduct exploratory data analysis (EDA), handle structural missing values, cast localized dates, and eliminate transactional anomalies.
4. **Automated Power BI ETL Loading**: Embedded the finalized Python cleaning script directly into Power BI's **Python Script Data Connector**. This completely automated the transformation and data-loading phase into Power BI's internal in-memory engine.
5. **Advanced DAX & Analytical Visualization**: Constructed a clean Star Schema data model and authored advanced DAX measures to calculate marketplace KPIs and complex Market Basket Analysis rules.

---


## 📊 Dashboard Architecture & Page Breakdown

### Page 1: Supply Chain & Operational Diagnostics
Designed to help logistics managers audit fulfillment velocities and clear delivery blockers.
* **Fulfillment Funnel**: Maps precise processing duration stages (Average hours to approve vs. Average hours to ship).
* **Customer Sentiment Core**: Correlates delivery performance directly to user review scores, demonstrating the heavy metric drop-off when orders are late.
* **Financial Distribution**: Categorizes transaction share value split cleanly by customer payment preferences (Credit Card, Boleto, Voucher, Debit).

### Page 2: Product Lifecycle & Merchant Growth Matrix
Designed for marketing managers and inventory planners to evaluate commercial trends and optimize distributor coverage.
* **Maturity Index**: Tracks rolling 90-day category revenue variations to isolate mature, plateaued product lines from emerging growth sectors.
* **Launch Performance**: Evaluates short-term volume contribution indexing for recently introduced product categories.
* **Demand Seasonality**: Employs a multi-panel visual grid to isolate localized monthly category purchase spikes for inventory planning.
* **Geographic Merchant Tracking**: Isolates top-tier local sellers (Review Score ≥ 4.5) suffering from low local market share penetration to pinpoint logistical expansion targets.

### Page 3: Market Basket Analysis (Predictive Affinity Modeling)
An advanced data science view that moves beyond basic descriptive charts to identify strategic product grouping opportunities.
* **Association Rule Parameters**: Built complex, multi-layered DAX measures to compute **Support** (overall occurrence probability), **Confidence** (conditional purchase probability), and **Lift** (strength of item dependency) across product category pairs.
* **Strategic Bundling**: Equips digital marketing and catalog management teams with a data-driven blueprint for product recommendations and promotional bundles to increase Average Order Value (AOV).

---

## 🛠️ Technical Toolkit & Skills Demonstrated
* **Database & Ingestion**: SQL Server Management Studio (SSMS), Relational Database Management.
* **Languages & Drivers**: Python (`Pandas`, `NumPy`), `pyodbc` Database Connector.
* **BI Platform & ETL**: Power BI Desktop (Python Script Data Connector Engine).
* **Data Modeling**: Star Schema Optimization (Fact and Dimension relationships).
* **Advanced Analytics (DAX)**: Market Basket Analysis Rule Mining (`Support`, `Confidence`, `Lift`), Rolling 90-day metrics, localized sales percentages.
* **UI/UX Optimization**: Executive dark-mode canvas theme, synchronized global year slicers, cross-page navigation layouts, and robust data label formatting.

---

## 💡 Key Business Insights Uncovered
* **Logistics Gaps**: Order processing experiences an operational lag of ~75 hours between payment approval and physical dispatch, presenting a massive opportunity for warehousing automation.
* **Satisfaction Drop**: Late deliveries drop average customer review scores significantly, proving that fulfillment speed is the strongest driver of platform retention.
* **Cross-Selling Potential**: Market Basket Analysis identified significant Lift parameters between specific complementary categories, indicating that co-locating digital listings or offering pre-packaged product bundles could directly increase platform gross merchandise volume (GMV).

## 📂 Project Structure & Files
This repository is organized as an end-to-end data pipeline, moving from raw data to a fully deployed dashboard:

1. **`Dashboard_images/`**: Contains high-resolution screenshots of the 3-page interactive Power BI dashboard for quick viewing.
2. **`01_Data_Cleaning.ipynb`**: Houses the initial exploratory data analysis (EDA) and data wrangling phase using Python and the `pyodbc` database connector to pull from SSMS.
3. **`02_python_script.py`**: The finalized, production-ready Python transformation script embedded directly inside Power BI's Data Connector interface to automate data loading.
4. **`Brazilian E-commerce Supply Chain Insights Project.pbix`**: The complete Power BI dashboard suite containing the star schema model, global sync-slicers, and custom MBA DAX metrics.
