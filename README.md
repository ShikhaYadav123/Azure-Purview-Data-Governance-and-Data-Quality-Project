# Azure Data Governance & Data Quality Project: Supply Chain

This project demonstrates **data transformation, quality checks, and governance** using **Azure Data Factory**, **Microsoft Purview**, and **Azure Data Lake Storage (ADLS)**. 

The focus is on **building a trusted data foundation** through automated pipelines and governance policies tailored for the **supply chain** domain.

---

## Objective

To design and implement a robust Azure-based pipeline that ensures:
- **Data quality at scale** during ingestion and transformation
- **Traceable data lineage and business metadata**
- **Governance readiness** for e-Commerce supply chain data

---

## Tech Stack

| Azure Service              | Role                                                  |
|----------------------------|--------------------------------------------------------|
| **Azure Data Factory (ADF)** | Data ingestion, transformation & quality rules         |
| **Azure Data Lake Gen2**     | Centralized storage for raw and cleaned data          |
| **Azure Synapse Analytics**  | Serverless querying for partitioned `.csv` datasets    |
| **Microsoft Purview**        | Data cataloging, lineage, classification & glossary   |

---

## Dataset Overview

- **Source**: Kaggle
- **Total Records**: ~55K

---

## Implementation Breakdown

### Phase 1: Raw Data Ingestion (ADF)
- Uploaded source `.csv` to **ADLS** `raw-data/` container.
- Created **linked services** and **datasets** in ADF( **Azure Data Factor**).
- Designed a pipeline to copy raw data into ADLS Gen2.

###  Phase 2: Data Cleaning & Quality Checks
- Transformed and standardized data:
  - Renamed columns
  - Parsed `OrderDate` and validated formats
  - Ensured `Quantity` > 0 and `Unit Price` > 0
  - Derived `TotalSales` column
    
- Used ADF’s **data flow** with **derived columns**, **null checks**, and **data filters**.
- Stored `cleaned` and `invalid` data to **different folders**.

###  Phase 3: Data Governance with Microsoft Purview
- Registered data sources: **ADLS**.
- Created **business glossary terms** for supply chain concepts (`OrderDate`, `CustomerID`, etc.).
- Scanned and **classified** sensitive fields.
- **Data lineage** from ingestion to transformation.
- Enhanced metadata discoverability and compliance readiness.
---

## 📸 Screenshots

> *https://github.com/ShikhaYadav123/Azure-Purview-Data-Governance-and-Data-Quality-Project/tree/main/Screenshots*

- ADF Pipeline for Raw to Cleaned
- Cleaned partitioned files in ADLS
- Purview Glossary
- Purview Data Catalog
---

## Key Outcomes

- End-to-end **data quality checks** using Azure services.
- Completed **data lineage and governance** using Microsoft Purview.
- Created a **business glossary** aligned with supply chain concepts.

---
**Thanks**
**Shikha**
