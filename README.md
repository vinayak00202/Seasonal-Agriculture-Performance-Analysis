# Seasonal Agriculture Performance Analysis

**VOIS AICTE Batch 1 (2026–2027) — Major Project**

**Student:** Kanishk Singh
**College:** International Institute of Information Technology, Pune
**AICTE Student ID:** STU6a4366c4b05f41782802116

## Problem Statement

Agricultural activities are influenced by seasonal variations in environmental conditions, farming practices, resource availability and market conditions. Raw agricultural data does not, on its own, explain how performance changes across seasons. This project analyzes a seasonal agricultural dataset to identify meaningful patterns, trends, relationships and differences in agricultural performance across the **Kharif**, **Rabi** and **Zaid** seasons.

## Dataset

`seasonal_agriculture_performance_dataset.csv` — 4,000 farm records across 8 Indian states, with columns covering:
- Farm details (state, district, crop, season, farm area)
- Environmental conditions (rainfall, temperature, humidity, sunlight, soil pH/moisture)
- Inputs (fertilizer, pesticide, nitrogen/phosphorus/potassium, seed quality, irrigation method)
- Outcomes (yield, production, market price, cost, revenue, profit)
- Resource metrics (water used, water efficiency, disease/pest risk)

## Repository Contents

| File | Description |
|---|---|
| `Seasonal_Agriculture_Performance_Analysis.ipynb` | Full analysis notebook — cleaning, EDA, statistical testing, visualizations, insights & recommendations |
| `seasonal_agriculture_performance_dataset.csv` | Raw dataset |
| `cleaned_seasonal_agriculture_dataset.csv` | Cleaned dataset used for analysis |
| `season_summary.csv` | Season-wise summary statistics |
| `VOIS_Major_Project_PPT_Submission_Kanishk_Singh.pptx` | Final project presentation |


## Methodology

1. **Data Cleaning** — Season/crop-aware median imputation for missing values (rainfall, soil moisture, yield); IQR-based outlier treatment on yield and water efficiency; duplicate check.
2. **Exploratory Data Analysis** — Distribution checks across season, state and crop.
3. **Seasonal Comparison** — Average yield, profit, water usage/efficiency, disease/pest risk and rainfall by season.
4. **Statistical Testing** — One-way ANOVA to confirm whether seasonal differences in yield and profit are statistically significant.
5. **Correlation Analysis** — Identify which environmental/input factors are most related to yield.
6. **Crop × Season Analysis** — Pivot tables/heatmaps of yield and profit by crop and season.
7. **Insights & Recommendations** — Evidence-based conclusions for seasonal agricultural planning.

## Key Findings

- **Kharif** is the strongest season for both yield (2.26 t/ha avg) and profit (₹1.79L avg), aided by higher rainfall.
- **Zaid** is the weakest season — lowest yield and a **negative average profit**, driven by low rainfall and low water-use efficiency.
- Seasonal differences in yield and profit are **statistically significant** (ANOVA, p < 0.001).
- **Water-use efficiency**, not fertilizer or pesticide volume, is the strongest driver of yield (correlation 0.78).
- Disease/pest risk is roughly constant across seasons and does not explain the profitability gap.
- Best/worst performing crops differ by season, so recommendations should be crop-specific rather than generic.

## Tools & Technologies

- Python 3, Pandas, NumPy
- Matplotlib, Seaborn (visualization)
- SciPy (statistical testing)
- Jupyter Notebook

## How to Run

```bash
pip install pandas numpy matplotlib seaborn scipy jupyter
jupyter notebook Seasonal_Agriculture_Performance_Analysis.ipynb
```

## Project Report

See `Major_Project_Seasonal_Agriculture_Performance_Analysis.pdf` (project brief provided by VOIS/AICTE) for the original problem statement and objectives.
