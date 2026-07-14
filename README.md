# Catastrophe Claim Severity Modeling (QM640 Capstone)
### Author: Narendra Kumar Reddi Nallagundla  

This repository contains the data, code, and project structure for the QM640 Data Analytics Capstone project:  
**Predicting Catastrophe Claim Severity Using Hazard, Socioeconomic, and Machine Learning Methods.**

The goal of this project is to build a transparent, reproducible catastrophe severity modeling pipeline using open datasets (NOAA, NFIP, ACS) and modern statistical and machine learning techniques.

---

## Project Overview

Catastrophe losses in the United States have increased significantly over the past two decades. Insurers need reliable, explainable models to predict **claim severity**, not just hazard occurrence.  
This project integrates:

- Hazard intensity variables (wind speed, hail size, flood depth, storm duration)  
- NFIP flood claim payouts  
- Socioeconomic indicators (median income, housing age, population density)  
- Machine learning classification (Random Forest, Gradient Boosting, XGBoost)  
- Time‑series trend analysis (Mann–Kendall, ARIMA)

The project is designed to be **fully reproducible**, with all data, code, and notebooks organized in a clear structure.

---

## Repository Structure
DataAnalyticsCapstone/
│
├── data/
│   ├── raw/                # Raw NOAA, NFIP, ACS subsets (uploaded)
│   └── processed/          # Cleaned, merged datasets (generated later)
│
├── notebooks/
│   ├── 01_eda.ipynb        # Exploratory data analysis
│   ├── 02_regression.ipynb # RQ1 & RQ2 modeling
│   ├── 03_ml.ipynb         # RQ3 machine learning models
│   └── 04_timeseries.ipynb # RQ4 trend analysis
│
├── src/
│   ├── preprocess.py       # Data cleaning & merging
│   ├── features.py         # Feature engineering
│   ├── models.py           # ML training & evaluation
│   └── utils.py            # Shared helper functions
│
├── figures/                # Exported charts, plots, tables
│
├── appendix/               # Supplementary materials
│
└── README.md               # Project documentation


This structure follows best practices for academic and industry data science workflows.

---

## Dataset Description

This project uses **public, open datasets**:

### 1. NOAA Storm Events Database  
Hazard intensity variables:  
- wind_speed  
- hail_size  
- flood_depth  
- storm_duration  
- property_damage  

### 2. NFIP Claims Dataset  
Flood claim payout variables:  
- building_damage  
- contents_damage  
- total_payout  

### 3. ACS 5‑Year Estimates  
Socioeconomic indicators:  
- median_income  
- housing_age  
- population_density  
- homeownership_rate  

### Raw CSV Samples Included  
uploaded the following files into `/data/raw/`:

- `acs_raw_subset.csv`  
- `nfip_raw_subset.csv`  
- `noaa_raw_subset.csv`

These are **small representative samples** of the full datasets 
The full datasets are large (hundreds of MB to several GB), so the README includes links and instructions to download them.

---

## Dataset Source Links

- NOAA Storm Events:  
  https://www.ncdc.noaa.gov/stormevents/

- NFIP Claims (OpenFEMA):  
  https://www.fema.gov/openfema-data-page/nfip-claims

- ACS 5‑Year Estimates:  
  https://www.census.gov/data/developers/data-sets/acs-5year.html

---

## Reproducibility Instructions

To reproduce the project:

1. Clone the repository
2. Install dependencies
3. Download full datasets
4. Run preprocessing
5. Run EDA, regression, ML, and time‑series notebooks in order

## Research Questions (RQ1–RQ4)

RQ1: Hazard intensity → severity

RQ2: Socioeconomic moderation

RQ3: ML classification of high severity

RQ4: Severity trend over 20 years

## Planned Outputs

Cleaned & merged dataset

Regression & moderated regression results

ML classification metrics (Accuracy, Precision, Recall, F1, ROC‑AUC)

SHAP feature importance plots

Time‑series trend charts

Final PDF report 

## License
This project uses public datasets and is intended for academic use under QM640 guidelines.

## Acknowledgments
Walsh College Faculty
Mentor: Mr. Sridhar S
NOAA, FEMA OpenFEMA, U.S. Census Bureau
