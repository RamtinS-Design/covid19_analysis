# COVID-19 Global Data Analysis

A beginner data analysis project using **Python**, **Pandas**, and **NumPy**.

---

## About This Project

This project analyzes the COVID-19 global dataset from Kaggle. The goal was to practice real-world data science skills: cleaning messy data, calculating meaningful statistics, and drawing conclusions from numbers.

This is part of my learning journey — I focused on getting solid with Pandas and NumPy before adding visualizations.

---

## Dataset
**Source:** [COVID-19 Dataset — Kaggle](https://www.kaggle.com/datasets/imdevskp/corona-virus-report)  
**Coverage:** January 22, 2020 – July 27, 2020  

| File | Description |
|------|-------------|
| `worldometer_data.csv` | Latest snapshot per country (cases, deaths, tests, population) |
| `country_wise_latest.csv` | Confirmed, deaths, recovered per country |
| `day_wise.csv` | Global daily totals over time |
| `covid_19_clean_complete.csv` | Full time-series by country and province |

---

## What I Did

### 1. Data Cleaning
- Checked for and handled **missing values** using three strategies: fill with `0`, fill with `median`, or fill with `'Unknown'`
- Checked for **duplicate rows**
- Fixed **data types** (count columns were stored as floats and needed to be integers)
- **Renamed columns** to remove spaces and slashes
- Created **new calculated columns**: Case Fatality Rate, Recovery Rate, Active Rate

### 2. Exploratory Analysis
- Global totals: confirmed cases, deaths, recovered, active
- Top 10 countries by cases and by deaths
- Breakdown by continent

### 3. Mortality & Recovery Rate Analysis
- Compared Case Fatality Rate (CFR) across countries
- Found that countries with **more testing showed lower CFR** — because more testing detects mild cases
- Split countries into high-testing and low-testing groups and compared outcomes

### 4. Time-Series Analysis
- Tracked how CFR and recovery rates changed month by month
- Added a **7-day rolling average** to smooth out daily reporting gaps
- Compared the first week vs. last week of available data

### 5. Summary Statistics
- Descriptive stats (mean, median, std, percentiles)
- CFR percentile breakdown
- Recovery rate by continent

---

## Key Findings
1. **The Americas had the most cases** — the USA and Brazil drove the majority of global case counts by mid-2020.
2. **More testing = lower apparent CFR** — countries testing heavily showed significantly lower fatality rates, not because the virus was less deadly, but because more mild cases were being counted.
3. **Recovery rates improved significantly over time** — from near 0% in January 2020 to over 60% by July 2020.
4. **July 2020 had the highest monthly new case count** — the monthly breakdown shows clear acceleration into mid-2020.
5. **Median CFR across significant countries was around 2–3%**, but outliers pulled the average higher.

---

## How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/RamtinS-Design/covid19_analysis.git
   cd covid19_analysis
   ```

2. Install dependencies:
   ```bash
   pip install pandas numpy jupyter
   ```

3. Open the notebook:
   ```bash
   jupyter notebook covid19_data_analysis.ipynb
   ```

4. Run all cells from top to bottom.

---

## Project Structure

```
covid19_analysis/
│
├── covid19_data_analysis.ipynb   ← Main analysis notebook
├── worldometer_data.csv
├── country_wise_latest.csv
├── day_wise.csv
├── covid_19_clean_complete.csv
├── full_grouped.csv
├── usa_county_wise.csv
└── README.md
```

---

## Future Improvements
- **Visualizations** with `matplotlib` and `seaborn`
- **Interactive maps** with `plotly`
- **Time-series forecasting** with `statsmodels` or `Prophet`
- **Machine learning** to predict outcomes

---

## License
MIT. See[License](License)

## Author
Made by (RamtinS-Design) 
