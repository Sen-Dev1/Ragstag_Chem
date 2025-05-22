# Ragstag_Chem
A robust, cloud-enabled data platform that integrates, models, and visualizes raw operational and sales data from Ravago’s ERP, CRM, and logistics systems to optimize decision-making across supply chain and sales forecasting.

# Ravago Materials Intelligence Hub (RMIH)

**Purpose**:  
This project simulates a full-scale enterprise data intelligence platform for Ravago. It integrates, models, and visualizes raw ERP, CRM, and logistics data to support data-driven decision-making across the organization. The architecture reflects industry best practices using Azure Cloud, Snowflake, dbt, and Power BI.

---

## 🧱 Project Architecture Overview

**Tech Stack**:
- **Ingestion**: Fivetran | Azure Data Factory | Azure Event Hub
- **Storage**: Azure Data Lake Gen2 (Raw → Curated layers)
- **Modeling**: dbt (Kimball + DataVault modeling)
- **Warehouse**: Snowflake
- **Visualization**: Power BI
- **CI/CD**: Azure DevOps Pipelines
- **Governance**: dbt Tests | Azure Monitor | Microsoft Purview

---

## 🗃️ Data Domains

- **Sales**: Regional sales data, product performance, customer segmentation
- **Inventory**: Stock levels, movement history, safety stock analysis
- **Logistics**: Shipment events, delays, carrier performance
- **CRM**: Customer interactions, engagement scoring

---

## 📊 Power BI Dashboards

- 📦 Shipment Delay Tracker (live from Event Hub)
- 📈 Sales Forecast vs Actual by Region
- 📉 Low Inventory Alerts
- 🧾 Customer 360 View

---

## 📂 Folder Structure

Ragstag_Chem-materials-intelligence-hub/
│
├── ingestion/
│ ├── fivetran_config/
│ └── adf_pipeline/
│
├── data_lake/
│ ├── raw/
│ ├── clean/
│ └── curated/
│
├── dbt/
│ ├── models/
│ │ ├── staging/
│ │ ├── marts/
│ │ └── vault/
│ ├── macros/
│ └── dbt_project.yml
│
├── powerbi/
│ ├── dashboards/
│ └── visuals/
│
├── ci_cd/
│ └── azure-pipelines.yml
│
└── docs/
├── ERD.pdf
├── DataDictionary.xlsx
└── Readme.md
