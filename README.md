# Data Engineering Salary Insights Dashboard (2020-2025)

## Overview

This Power BI dashboard offers a dynamic and insightful analysis of Data Engineering pay rates over the period 2020 to 2025. The dashboard is designed to offer a thorough perspective on pay trends, the labor market, and the impact on pay of various factors like level of experience, work model, company size, and location. This dashboard is a critical tool for data professionals, recruiters, and businesses seeking to benchmark pay within the data engineering space.

## Data Source

The data source for the dashboard is the **"Data Eng Salary 2024"** dataset, which can be accessed through Kaggle:
[Data Engineering Salary 2024 Dataset](https://www.kaggle.com/datasets/zeesolver/data-eng-salary-2024)

## Power Query Transformations

The original data was rigorously cleansing and transforming with Power Query to ensure accuracy, consistency, and highest usability for visualization. Some of the transformations are as follows:

* **Standardizing Experience Levels:**
    * `SE` replaced with `Senior-level/Expert`
    * `MI` replaced with `Mid-level/Intermediate`
    * `EN` replaced by `Entry-level/Junior`
    * `EX` replaced by `Executive-level/Director`
* **Normalizing Employment Types:**
    * `FT` replaced by `Full-time`
    * `PT` replaced by `Part-time`
    * `CT` replaced by `Contract`
    * `FL` replaced by `Freelance`
* **Normalizing Company Sizes:**
    * `S` replaced by `Small`
    * `M` replaced with `Medium`
    * `L` replaced with `Large`
* **Converting `remote_ratio` to `work_model`:**
    * `100` replaced with `Remote`
    * `50` replaced with `Hybrid`
    * `0` replaced with `On-site`
* **Geographical Data Expansion:**
   * Country codes were replaced by full country names by merging with a lookup table that has `country code` and `country name` columns.             This makes the geography analysis more readable.
* **Data Type Corrections:** Made sure that all columns have the proper data types for accurate calculations and visualization (e.g., numbers for salaries, text for categories, dates for trends).

## Overview of Dashboard Pages

The dashboard is crafted into three main interactive pages, each showcasing other attributes of salary insights:

### 1. Jobs Salary Insights 2020-2025

This page presents a general overview of salary amounts and developments through time.

* **Key Performance Indicator (KPI) Cards:**
    * Number of Employees
    * Average Salary
    * Highest Salary Record
    * Lowest Salary Record
* **Bar Chart:** Salaries at different levels of experience.
* **Pie Chart:** Employees by work model (Remote, Hybrid, On-site).
* **Line Chart:** Salary levels over a period of time (Yearly or Quarterly average salary).
* **Slicers:** `Year`, `Employment Type`, `Company Size`

### 2. Job Role & Geographical Salary Analysis

The page delves into salary variations based on specific job roles and geographies.

* **Bar Chart:** The highest-paying job roles.
* **Table:** Displays extensive salary information like `Country`, `Job Title`, `Experience Level`, and `Average Salary`.
* **Map Chart:** Displays salary variation across countries, highlighting global pay differences.
* **Slicers:** `Company Location` (Country), `Job Title`, `Experience Level`

### 3. Company & Work Model Influence on Salaries

This page explores the influence of company size and work model arrangements on values of different job titles' salaries.

* **Column Chart:** Illustrates how work models (Remote, Hybrid, On-site) affect average salaries by company size (Small, Medium, Large).
* **Matrix Visual:**
    * **Rows:** `Job Title`
    * **Columns:** `Company Size`
    * **Values:** `Average Salary` (allowing for quick comparisons of average salaries by job title and company size).
* **Slicers:** `Year`, `Employee Residence` (Country), `Job Title`
