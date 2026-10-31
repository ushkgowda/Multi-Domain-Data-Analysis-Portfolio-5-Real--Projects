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


# Project 3: Weather Data Analysis

Analysis of 1,461 days of weather data (2012–2015) for Seattle, USA, focusing on temperature trends, seasonal patterns, rainfall distribution and extreme weather events.

## Contents
- `project3_weather_analysis.ipynb`: complete analysis with data validation, visualizations and statistical tests
- `analysis.py`: reusable functions for data analysis and visualization
- `build_report.py`: generates the PDF report
- `project3_weather_report.pdf`: 9-page report with executive summary and recommendations
- `visualizations/`: generated charts and graphs
- `datasets/seattle_weather.csv`: source dataset

## Key findings
- Average maximum and minimum temperatures were 16.4°C and 8.2°C.
- August was the warmest month (20.4°C average), while January was the coolest (5.5°C).
- Total precipitation over four years was 4,426 mm.
- Winter received the highest rainfall (34.1%), while summer received only 7.8%.
- Hot days increased from 9 in 2012 to 30 in 2015.
- The wettest day recorded 55.9 mm of rainfall (March 15, 2015).
- Seasonal changes were the strongest factor influencing weather patterns.

## Run
```bash
pip install pandas numpy scipy matplotlib seaborn
```
# Project 4: COVID-19 Trends Analysis

Analysis of global and country-level COVID-19 cases and deaths across 197 countries and territories (January 2020 – March 2023), focusing on pandemic waves, case fatality rates and country comparisons.

## Contents
- `project4_covid19_analysis.ipynb`: complete analysis with data validation, visualizations and statistical tests
- `analysis.py`: reusable functions for data processing, metrics and visualizations
- `build_report.py`: generates the PDF report
- `project4_covid19_report.pdf`: 9-page report with executive summary and recommendations
- `visualizations/`: generated charts and graphs
- `datasets/`: source COVID-19 dataset from Johns Hopkins University CSSE

## Key findings
- Analyzed 676.6 million confirmed cases and 6.88 million reported deaths.
- Global reported case fatality ratio was approximately 1.02%.
- The Omicron wave recorded the highest daily cases, reaching 3.4 million on 24 January 2022.
- India reported 44.69 million cases and 530,779 deaths.
- India's Delta wave was the deadliest, peaking at 391,232 daily cases.
- Death surges generally followed case surges by approximately 14 days.
- Reported deaths per 100 cases declined significantly over time.

## Run
```bash
pip install pandas numpy matplotlib seaborn scipy

python analysis.py
python build_report.py
```

**Note:** The project uses the Johns Hopkins University CSSE COVID-19 dataset. It contains reported confirmed cases and deaths, not actual infection counts. The dataset ends on 9 March 2023.

# Project 5: Social Media Analytics

Analysis of 1,500 social media posts across four platforms (Instagram, Facebook, X and LinkedIn), covering November 2025 to October 2026, focusing on engagement rates, audience growth and content performance.

## Contents
- `project5_social_media_analysis.ipynb`: complete analysis with data validation, visualizations and statistical tests
- `analysis.py`: reusable functions for data processing, metrics and visualizations
- `generate_data.py`: generates the simulated social media dataset (seed 7)
- `build_report.py`: generates the PDF report
- `project5_social_media_report.pdf`: 10-page report with executive summary and recommendations
- `visualizations/`: generated charts and graphs
- `datasets/`: simulated social media posts and follower data

## Key findings
- Analyzed 1,500 posts across four social media platforms.
- Total impressions reached 32.4 million with 1.58 million engagements.
- Instagram generated 90% of total engagements.
- Carousels achieved the highest engagement rate (6.09%), followed by videos (4.54%).
- Evening posts (6 PM–9 PM) performed better than late-night posts.
- Giveaways increased engagement rates by approximately 78%.
- LinkedIn recorded the highest follower growth (+41.1%).
- The top 10% of posts generated 55% of total engagements.

## Run
```bash
pip install pandas numpy matplotlib seaborn scipy

python generate_data.py
python analysis.py
python build_report.py
```

**Note:** This project uses a simulated dataset with a seeded data generator (seed 7). The findings demonstrate social media analytics techniques and do not represent actual social media account performance.
