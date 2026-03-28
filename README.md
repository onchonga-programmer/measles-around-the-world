# Measles Surveillance Analysis (TidyTuesday)

This project explores global measles and rubella surveillance data using Python notebooks. It includes:

- Monthly case-level analysis and cleaning.
- Yearly aggregated analysis and cleaning.
- Exploratory data analysis (EDA) with static and interactive visualizations.

The analysis is organized in Jupyter notebooks under `notebooks/`, with source data in `data/`.

## Project Goals

- Understand measles and rubella reporting patterns across countries and regions.
- Build a clean, analysis-ready monthly dataset.
- Clean and validate yearly surveillance aggregates.
- Produce visual summaries of burden, trend, and regional variation.

## Repository Structure

```text
.
├── README.md
├── requirements.txt
├── data/
│   ├── cases_month.csv
│   ├── cases_month_clean.csv
│   └── cases_year.csv
├── documentation/
│   └── measles_report.docx
└── notebooks/
	├── monthly_measles.ipynb
	└── yearly_measles.ipynb
```

## Data Files

### `data/cases_month.csv`
Raw monthly surveillance data with fields such as:

- `region`, `country`, `iso3`, `year`, `month`
- `measles_suspect`, `measles_clinical`, `measles_epi_linked`, `measles_lab_confirmed`, `measles_total`
- `rubella_clinical`, `rubella_epi_linked`, `rubella_lab_confirmed`, `rubella_total`
- `discarded`

### `data/cases_month_clean.csv`
Cleaned monthly output currently checked into the repo. It includes the monthly fields above plus:

- `report_date` (constructed date column from `year` + `month`)

### `data/cases_year.csv`
Raw yearly aggregated data with fields such as:

- `total_population`, `annualized_population_most_recent_year_only`
- `total_suspected_measles_rubella_cases`
- Measles and rubella totals, breakdowns, and incidence rates
- `discarded_cases`, `discarded_non_measles_rubella_cases_per_100000_total_population`

## Notebooks

### `notebooks/monthly_measles.ipynb`
Main monthly workflow:

- Loads raw monthly data.
- Documents variable meanings.
- Cleans and standardizes fields.
- Converts data types and handles missing/invalid values.
- Builds `report_date`.
- Saves cleaned monthly output.
- Runs EDA and visualizations (Matplotlib, Seaborn, Plotly).

### `notebooks/yearly_measles.ipynb`
Main yearly workflow:

- Loads yearly aggregated data.
- Standardizes schema and region labels.
- Applies validation checks for surveillance consistency.
- Handles nulls and type conversion.
- Adds helper flags such as `surveillance_reported` and `measles_breakdown_missing`.
- Produces descriptive statistics, regional summaries, trends, and correlation analysis.

## Environment Setup

### 1. Create and activate a virtual environment

```bash
python -m venv venv
source venv/bin/activate
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

## Running the Analysis

Launch Jupyter and open either notebook:

```bash
jupyter lab
```

Then run notebooks in this order:

1. `notebooks/monthly_measles.ipynb`
2. `notebooks/yearly_measles.ipynb`

Running top-to-bottom in each notebook ensures intermediate cleaning steps and outputs are produced in sequence.

## Tools and Libraries

Core stack used in this project:

- Data processing: Pandas, NumPy
- Statistical and modeling utilities: SciPy, Statsmodels, scikit-learn
- Visualization: Matplotlib, Seaborn, Plotly
- Notebook/runtime: Jupyter, ipykernel

See `requirements.txt` for the full environment definition.

## Outputs

- Clean monthly dataset: `data/cases_month_clean.csv`
- Figures and interactive plots generated directly in notebooks
- Additional narrative/report material in `documentation/measles_report.docx`

## Reporting

Use the built-in report scaffold to create a reproducible analysis report:

- Report template: `documentation/analysis_report_template.md`
- Report workflow guide: `documentation/report_workflow.md`
- Figure exports: `outputs/figures/`
- Table exports: `outputs/tables/`

Suggested process:

1. Run notebooks and export figures/tables.
2. Fill the template with key findings and embedded visuals.
3. Save your final report in `documentation/`.

## Notes

- The notebooks currently rely on relative paths like `../data/...`, so run them from within `notebooks/` (or through a notebook editor that preserves notebook-relative paths).
- Some yearly cleaning/output steps are defined in the notebook; if you want a checked-in cleaned yearly CSV, run `notebooks/yearly_measles.ipynb` end-to-end and export the final frame.

## Future Improvements

- Add a scripted pipeline version (Python module/CLI) for non-notebook reproducibility.
- Add automated data validation tests.
- Track generated artifacts in a dedicated `outputs/` folder.
