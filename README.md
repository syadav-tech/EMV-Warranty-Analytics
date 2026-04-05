# EMV Motors - Warranty Cost Intelligence

## Project Overview
An end-to-end automotive warranty analytics project built using the PACE framework 
(Plan, Analyse, Construct, Execute). This project analyses synthetic warranty claims 
data for EMV Motors to identify the highest-cost failure modes, components and 
geographic patterns - enabling the Engineering team to prioritise a 10% cost 
reduction target by Q3 2026.

## Problem Statement
EMV Motors is facing increased warranty expenditures due to increasing warranty claims 
over the fiscal year 2025-2026. This increased cost is impacting QA/QC teams and R&D 
teams budgets. This analysis will identify the highest-cost failure modes and components, 
enabling the Engineering team to prioritise mitigation strategy and resource allocation 
and target a reduction of 10% in warranty expenditure by Q3 2026.

## Key Findings
- Powertrain components account for **47.4% (£767,037)** of total warranty expenditure (£1,618,223)
- Warranty costs increased **433.5%** over six quarters - Q4 2024 (£52,154) to Q1 2026 (£278,226)
- **Early-life failures (0–6 months)** generate the highest claim volume - pointing to manufacturing and assembly issues
- **Supplier quality score alone does not predict claim cost** - component family is the primary confounding variable
- **Americas + Leisure** and **EU + Commercial** are the highest-risk market and use case combinations

## Methodology
PACE Framework:
- **Plan** - Problem statement, stakeholder identification, 5 analytical questions
- **Analyse** - Synthetic dataset generation across 3 relational tables (8 suppliers, 15 components, 2,000 claims)
- **Construct** - Exploratory data analysis answering all 5 analytical questions with visualisations
- **Execute** - Executive summary, recommendations and limitations

## Dataset
Synthetic data generated using Python - 3 relational tables:

| Table | Rows | Description |
|---|---|---|
| suppliers.csv | 8 | Supplier master data - quality scores, tier, location |
| components.csv | 15 | Component reference - 5 families across 15 parts |
| claims.csv | 2,000 | Warranty claims - costs, failure modes, time to claim |
| sales.csv | 13,500 | Sales transactions - components sold by market and use case |

## Notebooks

| Notebook | Stage | Description |
|---|---|---|
| 01_data_generation.ipynb | Plan & Analyse | Synthetic dataset generation |
| 02_eda_analysis.ipynb | Construct | EDA - 5 analytical questions with charts |
| 03_executive_summary.ipynb | Execute | Findings, recommendations, limitations |

## Tech Stack
- Python 3.13
- pandas - data manipulation
- numpy - numerical operations
- matplotlib - visualisations
- seaborn - heatmap and statistical charts
- Jupyter - notebook environment

## How to Run
1. Clone the repository
2. Install dependencies: `pip install pandas numpy matplotlib seaborn jupyter`
3. Run `01_data_generation.ipynb` first to generate CSV files
4. Run `02_eda_analysis.ipynb` for exploratory analysis
5. Review `03_executive_summary.ipynb` for findings and recommendations

## Author
**Shubham Yadav** | Systems & Requirements Engineer | April 2026  
