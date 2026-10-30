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


# Project 2: Student Performance Analysis

Analysis of 1,200 students (Grades 9–12) to study academic performance, pass/fail rates, subject-wise scores, attendance and study habits.

## Contents
- `project2_student_performance.ipynb`: complete analysis with data cleaning, visualizations and statistical tests
- `analysis.py`: reusable analysis functions
- `generate_data.py`: generates the simulated student dataset (seed 42)
- `project2_student_performance_report.pdf`: 8-page report with executive summary and recommendations
- `student_performance.csv`: source dataset

## Key findings
- Overall pass rate: 71.5% (799 out of 1,117 complete students)
- Computer Science has the highest average score (60.6); Math has the lowest (54.1)
- Attendance has a strong positive relationship with academic performance (r = 0.57)
- Students receiving tutoring have an average score of 60.4 compared to 56.8 without tutoring
- 194 students were identified as high-risk (attendance below 75% and average score below 50)
- Study hours and parental education are also associated with student performance

## Run
```bash
pip install pandas numpy scipy matplotlib seaborn

python generate_data.py
python analysis.py
```

**Note:** The project uses simulated data. The findings are for demonstration purposes and do not represent real student performance.
