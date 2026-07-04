# Supply Chain Resiliency & Margin Protection in Prestige Beauty
## An Enterprise Integration Case Study

**Author:** Shari Nishida  
**Program:** Correlation One Data Analytics  
**Industry Focus:** Prestige Beauty — Luxury CPG Supply Chain Analytics

---

## Project Overview

This portfolio project investigates how a prestige beauty brand can transition from a high-risk, single-factory sourcing model to a diversified, multi-supplier network without diluting retail gross margins. The analysis integrates operational supply chain data with Sephora consumer review data to identify sourcing vulnerabilities, model tariff impact scenarios, and validate consumer review velocity as a forward-looking S&OP demand signal.

---

## Repository Structure

```
├── eda_analysis.py              # Python EDA analysis script (all 8 charts)
├── eda_charts/
│   ├── chart1_defect_rate.png          # Defect Rate by Product Type
│   ├── chart2_margin.png               # Baseline vs. Tariff-Adjusted Margin
│   ├── chart3_lead_time_variance.png   # Lead Time Variance Distribution
│   ├── chart4_transport.png            # Transportation Mode Cost vs. Lead Time
│   ├── chart5_inspection.png           # Inspection Results by Supplier
│   ├── chart6_review_velocity.png      # Sephora Review Velocity 2010-2023
│   ├── chart7_exclusivity_rating.png   # Rating by Product Exclusivity Tier
│   └── chart8_stock_scatter.png        # Stock Levels vs. Units Sold
├── wireframe_eda_colors.svg     # Dashboard wireframe (SVG source)
├── wireframe_eda_colors.png     # Dashboard wireframe (PNG export)
└── README.md
```

---

## Datasets Used

| Dataset | Source | Size | License |
|---|---|---|---|
| Supply Chain Analysis | [Kaggle](https://www.kaggle.com/datasets/harshsingh2209/supply-chain-analysis) | 20.6 KB, 100 rows | CC0 Public Domain |
| Sephora Products & Reviews | [Kaggle](https://www.kaggle.com/datasets/nadyinky/sephora-products-and-skincare-reviews) | 496.9 MB, 1,094,411 reviews | Public |
| USTR Section 301 Tariff Schedules | [USTR.gov](https://ustr.gov/issue-areas/enforcement/section-301-investigations/section-301-china/tariff-actions) | Reference only | Public Domain |
| EU Commission HS Chapter 33 Tariffs | [EC.Europa.eu](https://taxation-customs.ec.europa.eu/customs-4/calculation-customs-duties/customs-tariff_en) | Reference only | Public Domain |

---

## Key Analytical Components

### Tariff Impact Coefficient
A feature engineering methodology mapping 2026 trade tariff penalties to product categories:
- **Cosmetics:** 25% East Asia Section 301 penalty applied to manufacturing cost
- **Skincare:** 10% EU MFN premium applied to manufacturing cost
- **Haircare:** 0% near-shore baseline (control group)

### Key Findings
1. **Supplier 4** carries a 66.7% inspection failure rate — the primary single-source quality risk
2. **Defect risk and tariff risk are independent dimensions** requiring separate mitigation strategies
3. **Skincare** is the highest-priority resilience investment across all four risk dimensions
4. **Sephora review velocity** grew 6.5x between 2015 and 2020, validating it as a leading S&OP demand signal
5. **Near-shoring** reduces both cost and lead time variance simultaneously

---

## Technical Stack

- **Python:** pandas, numpy, matplotlib (EDA and chart generation)
- **SQL:** Data wrangling and tariff proxy mapping logic
- **Tableau / Power BI:** Interactive dashboard (in progress)
- **Tools:** Jupyter Notebook, VS Code

---

## Portfolio Deliverables

| Deliverable | Status |
|---|---|
| Project Description | Complete |
| Project Scope | Complete |
| Data Curation Report | Complete |
| Exploratory Data Analysis | Complete |
| Interactive Dashboard | In Progress |
| Final Report | In Progress |

---

## GenAI Disclosure

Claude (Anthropic, Claude Sonnet 4.6) was used as a development and documentation partner for this project. All Python analysis was executed on actual datasets. All numerical findings derive from real data execution. Domain interpretation, analytical decisions, and ERP system integration recommendations reflect the author's 20+ years of professional supply chain and ERP consulting experience.

---

*This portfolio was developed for thought leadership visibility targeting the luxury CPG industry.*
