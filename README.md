# Statistical Estimation of Onion Seedling Density: A Planning Framework for Smallholder Traditional Farms in Pwalugu, Ghana

## Overview
This repository contains the dataset and analysis scripts for the study on onion seedling density and land-use efficiency ($R_i$) in the Upper East Region of Ghana.

## Repository Structure
- `data/raw/onion_sampling_raw.csv`: Original field measurements including text-based dimensions.
- `data/processed/onion_farm_layout_metric.csv`: Cleaned, machine-readable dataset used for statistical modeling.
- `analysis_notebook.ipynb`: The complete Python workflow (Pandas, Scipy, Statsmodels).

## Data Dictionary
| Column | Description |
| :--- | :--- |
| `Bed_ID` | Unique identifier for each sampled plot. |
| `Bed_Length_m` | Length of the bed in meters. |
| `Bed_Width_m` | Width of the bed in meters. |
| `Seedling_Count` | Physical count of onion seedlings within the bed area. |
| `Effective_Bed_Area_m2` | Calculated area available for planting ($Length \times Width$). |
| `Seedling_Density_per_m2` | Density calculated as $Seedling\_Count / Effective\_Bed\_Area\_m2$. |
| `Ri` | Land-Use Efficiency Ratio ($Bed\_Area / (Bed\_Area + Canal\_Area)$). |

## Data Provenance (Raw to Processed)
The transition from raw field notes to the processed dataset is handled within the `analysis_notebook.ipynb`. We utilize `pandas` to parse dimensions and calculate the derived metrics ($R_i$ and Density) to ensure reproducibility.



## Methodology & Analysis

### Statistical Framework
The analysis employs **Inferential Statistics** to estimate mean seedling density across varied bed geometries.

### Confidence Intervals
We apply the **Central Limit Theorem (CLT)** and use a **T-distribution** to compute 95% confidence intervals. This provides a robust framework for planning seedling requirements under uncertainty.

### Correlation & Regression
An **Ordinary Least Squares (OLS) regression** is implemented to examine the relationship between:
- Bed-Canal ratio ($R_i$)
- Observed seedling density

## Core Script Functions

### 1. Descriptive Statistics
- Mean seedling density  
- Standard deviation  
- Coefficient of Variation (CV)

### 2. Estimation Logic
- Inferential bounds for predicting seedling counts across larger plot areas  

### 3. Correlation Analysis
- Statistical validation of the impact of traditional canal systems on effective planting area  

## Purpose
This analysis supports data-driven decision-making for optimizing planting density and improving land-use efficiency in smallholder farming systems.
