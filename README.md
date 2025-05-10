# 📊 Shipping Data Warehouse & BI Reporting Project

This project implements a complete **Sales and Shipping Data Warehouse** using SQL Server, SSIS, SSRS, and Tableau — providing interactive analytics and reporting to support data-driven decisions.

---

## 🚀 Project Overview

This end-to-end BI solution consists of:

- 📁 Data stored in a **relational star schema**
- 🔄 ETL pipeline built using **SSIS**
- 📊 Dashboards built in **Tableau**
- 📄 Paginated reports built in **SSRS**
- 📦 Source data extracted from Excel (`SalesRecord.xlsx`)

---

## 🎯 Business Requirements

The business required insights into:

- Profitability trends across **item types**, **regions**, and **sales channels**
- Year-on-year changes in **gross profit and profit margin**
- Sales channel performance comparison (online vs offline)
- Report delivery through both **interactive dashboards** and **paginated reports**

---

## 🧩 Schema Design

The warehouse uses a **star schema**, including:

- **Fact Table:**
  - `Sales_Fact` – revenue, cost, and profit metrics
- **Dimension Tables:**
  - `Item_Dim` – product hierarchy
  - `Location_Dim` – country, region, city
  - `Sales_Channel_Dim` – online/offline
  - `Calendar_Dim` – year, quarter, month

📌 See: `schema_diagram.png`

---

## 🔁 ETL Process (SSIS)

Key components of the SSIS pipeline:

- Excel-based source ingestion
- Data cleansing and validation
- Surrogate key lookups and data enrichment
- Population of star schema tables

📌 See: `data_flow_diagram.png`

---

## 📊 Tableau Dashboards

Interactive Tableau visuals provide:

1. **Gross Profit by Year**
2. **Gross Profit by Item Type per Year**
3. **Average Profit Margin by Item Type per Year**
4. **Average Profit Margin by Sales Channel**
5. **Profit by Region per Item**

> **Note:** Dashboards use a SQL Server data source and must be reconnected locally.

---

## 📄 SSRS Reports

The project includes **paginated SSRS reports** for operational needs:

- 🔹 Monthly Profit Summary
- 🔹 Sales by Item Type
- 🔹 Profit Margin Breakdown Report
- 🔹 Year-over-Year Comparison Report

Reports are built using **SQL Server Reporting Services (SSRS)** and can be deployed to a report server or viewed locally via Report Builder.

📁 Reports located in: `SSRS_Reports/`

---

## 📂 Files Included

| File | Description |
|------|-------------|
| `SalesRecord.xlsx` | Raw sales data |
| `SSIS_Project/` | ETL packages for SQL Server |
| `SQL_Scripts/` | Scripts to create star schema and populate tables |
| `Sales_Analytics.twbx` | Tableau workbook (reconnect to your local SQL DB) |
| `SSRS_Reports/` | `.rdl` files for reporting |
| `schema_diagram.png` | Star schema architecture |
| `data_flow_diagram.png` | ETL workflow overview |

---

## ✅ How to Run the Project

1. **Restore/Create** the SQL Server database using scripts in `SQL_Scripts/`
2. Run the **SSIS packages** to load the data warehouse
3. Open and deploy **SSRS reports** (`.rdl`) via Report Builder or SSRS portal
4. Open **Tableau workbook**, reconnect to your local SQL Server, and explore dashboards

---

## 📌 Conclusions

- Region- and item-level profitability insights revealed margin opportunities
- Sales channel comparisons showed variations in profit behavior
- SSRS reports enabled scheduled, paginated operational reporting
- Tableau dashboards supported fast, interactive executive analysis

---



