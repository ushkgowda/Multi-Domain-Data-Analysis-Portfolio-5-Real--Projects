# Supermarket-Sales-Analysis
# Project 1: Supermarket Sales Analysis

Retail analysis of 2,000 invoices (Jan-Dec 2023, 3 branches, 6 product lines).

## Contents
- `project1_sales_analysis.ipynb`: full analysis with data validation, 9 visualizations and statistical tests
- `analysis.py`: reusable functions (loading, validation, metrics, charts)
- `build_report.py`: generates the PDF report from the analysis results
- `../reports/project1_supermarket_sales_report.pdf`: 10-page report with executive summary
- `../visualizations/`: all generated charts
- `../datasets/supermarket_sales.csv`: source data

## Key findings
- Total sales 519,281 across 2,000 invoices; average transaction 259.64
- Health & Beauty is the largest product line (18.7%); Fashion Accessories the smallest (14.9%)
- Weekends are below average (25.7% of sales vs 28.6% if even)
- No segment difference is statistically significant (all p > 0.2)
- Data quality issues: Total does not equal Unit Price x Quantity, Tax has no consistent rate, branches map to all cities

## Run
```bash
pip install pandas numpy matplotlib seaborn scipy reportlab
python analysis.py          # writes results.json and charts/
python build_report.py      # writes the PDF
```
Paths in `analysis.py` point at the dataset location; adjust `SRC` if you move files.
