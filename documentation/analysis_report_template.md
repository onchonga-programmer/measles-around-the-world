# Measles Surveillance Analysis Report

## 1. Executive Summary
- One-paragraph summary of the main findings.
- Why the findings matter.

## 2. Objectives
- Objective 1:
- Objective 2:
- Objective 3:

## 3. Data Sources
### 3.1 Raw Inputs
- `data/cases_month.csv`
- `data/cases_year.csv`

### 3.2 Cleaned Inputs
- `data/cases_month_clean.csv`
- Add yearly cleaned file path after export.

## 4. Methodology
### 4.1 Data Cleaning
- Standardized column names and text fields.
- Converted numeric columns and dates.
- Handled missing values and invalid negative counts.
- Removed duplicates.

### 4.2 Exploratory Analysis
- Distribution and missingness checks.
- Regional and country-level burden comparisons.
- Time trend analysis.
- Correlation analysis for key surveillance metrics.

## 5. Results
### 5.1 Data Quality Findings
- Missingness summary:
- Duplicate records removed:
- Validation checks:

### 5.2 Key Epidemiological Findings
- Finding 1:
- Finding 2:
- Finding 3:

### 5.3 Regional Patterns
- Regions with highest burden:
- Regions with strongest trends:

### 5.4 Temporal Trends
- Monthly patterns:
- Yearly patterns:

## 6. Visual Evidence
Add exported figures here and reference using relative paths.

### Figure 1. Global Measles Trend
![Global trend](../outputs/figures/figure_01_global_measles_trend.png)

### Figure 2. Top Countries by Measles Burden
![Top countries](../outputs/figures/figure_02_top_countries_measles.png)

### Figure 3. Regional Comparison
![Regional comparison](../outputs/figures/figure_03_regional_comparison.png)

## 7. Limitations
- Surveillance completeness may vary by country and year.
- Missing values may affect comparability for some indicators.
- Aggregated yearly indicators can mask subnational variation.

## 8. Conclusions
- Main conclusion 1:
- Main conclusion 2:
- Main conclusion 3:

## 9. Reproducibility Notes
- Notebooks used:
  - `notebooks/monthly_measles.ipynb`
  - `notebooks/yearly_measles.ipynb`
- Python dependencies listed in `requirements.txt`.
- Run notebooks top-to-bottom before exporting figures.

## 10. Appendix
- Additional tables
- Supplemental plots
- Data dictionary excerpts
