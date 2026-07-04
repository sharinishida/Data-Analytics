# Supply Chain Resiliency & Margin Protection in Prestige Beauty
### An Enterprise Systems Integration Case Study

**Author:** Shari Nishida  
**Program:** Correlation One Data Analytics  
**Industry Focus:** Prestige Beauty — Luxury CPG Supply Chain Analytics

---

## Executive Overview

In the prestige beauty sector, high gross profit margins (70–80%) are highly vulnerable to macro trade penalties, cross-border tariff fluctuations, and single-source vendor failures. This project establishes an analytical scenario-modeling framework that integrates **1.09 million rows of consumer demand sentiment data (Sephora)** with **upstream operational logistics logs** to insulate luxury margins and optimize safety stock configurations.

This case study serves as an analytical proof-of-concept for modernizing enterprise data environments, demonstrating how external data signals can calibrate master data views across core corporate systems:

- **ERP (SAP S/4HANA):** Calibrating Costing Views via a dynamic, engineered Tariff Impact Coefficient.
- **WMS (Manhattan Active):** Dynamically updating Reorder Points (ROP) based on lead-time variances.
- **S&OP Planning (Anaplan / o9 Solutions):** Transforming historical text reviews into forward-looking demand-sensing signals.

---

## Technical Stack

Unlike standard visualization portfolios, this project is backed by **20+ years of professional ERP configuration, SQL database tuning, and technology consulting experience**. It bridges the gap between frontline e-commerce fulfillment data and backend server table architecture.

- **Database Engineering:** SQLite, Data Curation, Relational Joins, and Production Table Remediation.
- **Advanced Analytics & Programming:** Python (Pandas, NumPy, SciPy) for automated pipeline wrangling and outlier risk modeling.
- **Business Intelligence:** Interactive Tableau / Power BI executive datafolios built for C-suite S&OP decision-making.

---

## Key Analytical Breakthroughs (EDA Phase)

1. **Systemic Quality Constraints:** Disproved the core industry hypothesis by revealing that quality risk (Haircare at 2.48% defect rate) and tariff risk (Cosmetics) are completely independent dimensions, requiring dual-track mitigation.
2. **Critical Sourcing Vulnerabilities:** Isolated an anonymized manufacturing node (Supplier 4) operating at a catastrophic **66.7% inspection failure rate** with zero passed batches, identifying the primary candidate for near-shore diversification.
3. **Logistics Bottleneck Anomalies:** Identified a major 9.9-day lead-time planning variance, revealing that expensive Air freight counterintuitively incurred the longest delivery delays (18.27 days) due to outbound distribution recording structures.
4. **Demand-Sensing Validation:** Proved a 6.5x surge in consumer review velocity preceding retail stockout events, providing an actionable 30-day advance warning window for warehouse stock adjustments.

---

## Datasets Used

| File | Source |
|---|---|
| `supply_chain_data.csv` | [Supply Chain Analysis Dataset](https://www.kaggle.com/datasets/harshsingh2209/supply-chain-analysis) |
| `product_info.csv` | [Sephora Products & Reviews](https://www.kaggle.com/datasets/nadyinky/sephora-products-and-skincare-reviews) |
| `reviews_0-250.csv` | Same source above |
| `reviews_250-500.csv` | Same source above |
| `reviews_500-750.csv` | Same source above |
| `reviews_750-1250.csv` | Same source above |
| `reviews_1250-end.csv` | Same source above |
| USTR Section 301 Tariff Schedules | [USTR.gov](https://ustr.gov/issue-areas/enforcement/section-301-investigations/section-301-china/tariff-actions) |
| EU Commission MFN Tariffs, HS Chapter 33 | [EC.Europa.eu](https://taxation-customs.ec.europa.eu/customs-4/calculation-customs-duties/customs-tariff_en) |

> **Note:** The five review files combined total 496.9 MB and exceed GitHub's 100 MB per-file limit. Do not commit these files to the repository. Download them directly from Kaggle and place them in the project root directory locally. A `.gitignore` entry is recommended.
>
> `supply_chain_data.csv` (20.6 KB) and `product_info.csv` (7.5 MB) are small enough to commit directly to GitHub if you choose to include the primary datasets in the repository.

---

## Repository Structure

- `notebooks/`: Python data profiling, data curation pipelines, and exploratory data analysis.
- `sql_scripts/`: Relational schema definitions and cross-dataset category bridge logic.
- `dashboards/`: Tableau Public workbook links, executive wireframes, and layout summaries.
- `eda_charts/`: All chart outputs generated from Python EDA analysis.

---

## How to Run

### Prerequisites

Python 3.8 or higher is required. Install all dependencies using the requirements file:

```bash
pip install -r requirements.txt
```

### Dataset Setup

Download the datasets listed above from Kaggle and place them in the project root directory before running any scripts.

### Run EDA Analysis (Python)

```bash
python eda_analysis.py
```

Charts will be saved to the `eda_charts/` directory.

### Run SQL Pipeline

The SQL script is written in standard ANSI SQL and is compatible with SQLite, PostgreSQL, and MySQL.

```bash
# SQLite example
sqlite3 prestige_beauty.db < sql_scripts/supply_chain_analysis.sql
```

---

## Requirements

See `requirements.txt` for the full dependency list:

```
pandas>=1.5.0
numpy>=1.23.0
matplotlib>=3.6.0
scipy>=1.9.0
```

---

## About the Author

Managing Director, NexGen Consulting, LLC. Specializing in business transformation, legacy system modernization, and data governance across Fortune 500 clients and government agencies. This project combines 20+ years of enterprise ERP configuration and supply chain consulting with modern cloud analytics to demonstrate how external data signals can drive real-time decision-making across global supply networks.

- **Core Strengths:** Strategy, Digital Transformation, ERP Integration, and Executive Advising.
- **Certifications:** PMP, PMI-ACP, CSM, Oracle Cloud AI, McKinsey Forward.
