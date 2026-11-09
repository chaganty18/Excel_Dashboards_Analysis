# Data Science Job Market Analysis

An Excel based analysis of the global data science job market, covering salaries, job types, countries, platforms, and in demand skills. The project combines a large real world job postings dataset with Power Query, Power Pivot, and an interactive dashboard built entirely with native Excel formulas and charts.

## Overview

This project explores data job postings to answer practical questions for anyone researching the data job market:

- How does median salary vary by job title, country, and employment type
- Does requesting more skills in a job posting correlate with higher pay
- Which skills appear most often in postings, and which ones pay the most
- How do US salaries compare to non US salaries for the same roles
- Where are jobs posted most often, and on which platforms

The project is split into two parts, each with its own README:

- **[Project 1, Salary Dashboard](Project1-Dashboard/README.md)**: a single page interactive dashboard for exploring salary, country, and job type.
- **[Project 2, Project Analysis](Project2-Analysis/README.md)**: PivotTable based analysis of salaries against skills, region, and platform, including the Power Query and Data Model work behind it.

## Repository Structure

```
Project1-Dashboard/
  1_Salary_Dashboard.xlsx        Interactive salary dashboard
  README.md                      Dashboard images and walkthrough

Project2-Analysis/
  1_Project_Analysis.xlsx        PivotTable based skills and salary analysis
  README.md                      Analysis images, data prep, and data model walkthrough

Resources/
  Datasets/
    data_jobs_20rows.xlsx          Small 20 row sample for quick testing
    data_jobs_salary_all.xlsx      Primary dataset, about 32,600 job postings
    data_jobs_salary_monthly.xlsx  Same data split into monthly sheets (Jan to Dec)
    data_jobs_monthly/             Job postings aggregated by month, one file per month
  Images/                         Dashboard and chart screenshots and gifs

README.md
LICENSE
```

## Dataset

The core dataset ([`data_jobs_salary_all.xlsx`](Resources/Datasets/data_jobs_salary_all.xlsx)) contains roughly 32,600 data job postings with the following fields:

`job_title_short`, `job_title`, `job_location`, `job_via`, `job_schedule_type`, `job_work_from_home`, `search_location`, `job_posted_date`, `job_no_degree_mention`, `job_health_insurance`, `job_country`, `salary_rate`, `salary_year_avg`, `salary_hour_avg`, `company_name`, `job_skills`

[`data_jobs_20rows.xlsx`](Resources/Datasets/data_jobs_20rows.xlsx) is a trimmed down sample used for quick testing without loading the full dataset. [`data_jobs_salary_monthly.xlsx`](Resources/Datasets/data_jobs_salary_monthly.xlsx) and the [`data_jobs_monthly`](Resources/Datasets/data_jobs_monthly) folder break the same postings out by month for trend analysis.

## Tools and Techniques

- Excel formulas: `VLOOKUP`, `HLOOKUP`, `XLOOKUP`, `MATCH`, `COUNTIF` / `COUNTIFS`, `SUMIF` / `SUMIFS`, `MEDIAN` with array `IF` logic, `TEXTJOIN`, `TEXTSPLIT`, `SORT`, `FILTER`
- Power Query for data cleaning, column splitting, unpivoting, and type conversion
- Power Pivot and the Excel Data Model for relating multiple tables without flattening them
- PivotTables and slicers for interactive, filterable summaries
- Dynamic, formula driven dashboard design using named ranges and conditionally highlighted charts
- Descriptive statistics for summarizing salary distributions

Full details and screenshots of the Power Query and Data Model work are in the [Project 2 README](Project2-Analysis/README.md).

## Getting Started

1. Clone or download this repository, keeping the folder structure shown above intact.
2. Open [`Project1-Dashboard/1_Salary_Dashboard.xlsx`](Project1-Dashboard/1_Salary_Dashboard.xlsx) or [`Project2-Analysis/1_Project_Analysis.xlsx`](Project2-Analysis/1_Project_Analysis.xlsx) in Excel.
3. If prompted, allow external connections and refresh the data (Data tab, Refresh All) to load the underlying dataset.
4. See the [Project 1 README](Project1-Dashboard/README.md) and [Project 2 README](Project2-Analysis/README.md) for a full walkthrough of each workbook.

Excel 365 or Excel 2021 or later is recommended, since the workbooks use dynamic array functions such as `FILTER`, `SORT`, and `XLOOKUP`.

## License

See [LICENSE](LICENSE) for details.
