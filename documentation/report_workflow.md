# Report Workflow

Use this workflow to produce a final report that stays reproducible with the analysis notebooks.

## 1. Run analysis notebooks
1. Open `notebooks/monthly_measles.ipynb` and run all cells.
2. Open `notebooks/yearly_measles.ipynb` and run all cells.

## 2. Export figures and tables
Save outputs with stable names:
- Figures: `outputs/figures/figure_XX_short_name.png`
- Tables: `outputs/tables/table_XX_short_name.csv`

## 3. Draft report
1. Copy `documentation/analysis_report_template.md` to a new dated file.
2. Fill sections with findings from notebook outputs.
3. Link or embed figures using relative paths.

## 4. Final checks
- Ensure every key claim has a supporting figure/table.
- Ensure paths in the report resolve correctly.
- Include run date and package environment if needed.
