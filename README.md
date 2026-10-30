# Companies in India – Data Analysis Using Python

## 📌 Project Overview

Choosing a company to work for is an important decision, especially for job seekers who want to understand the working environment, employee feedback, and career opportunities available in different organizations.

This project explores a dataset containing information about companies in India. Using Python, I aim to understand the available company information, explore employee ratings, and identify patterns in company reviews, salaries, job listings, and other workplace-related details.

The goal is to turn raw company data into meaningful insights that can help job seekers and other interested users better understand the companies represented in the dataset.

## 🎯 Project Objectives

The main objectives of this project are:

* Explore company ratings and understand how they vary across organizations.
* Identify companies with higher numbers of employee reviews.
* Examine the distribution of companies across different industries.
* Explore salary-related information available in the dataset.
* Analyze job listings, interview information, and employee benefits.
* Compare companies based on their available information.
* Identify data quality issues and prepare the dataset for analysis.
* Present findings through clear visualizations and summaries.

## 📂 Dataset Information

**Dataset Name:** Companies in India

**Source:** [Kaggle – Companies in India](https://www.kaggle.com/datasets/dhruvnegi2006/companies-in-india)

**File Format:** CSV

**Number of Records:** 10,000

**Number of Columns:** 11

### Dataset Columns

| Column              | Description                              |
| ------------------- | ---------------------------------------- |
| `name`              | Name of the company                      |
| `rating`            | Overall company rating                   |
| `company_type`      | Type or industry of the company          |
| `hq`                | Company headquarters and other locations |
| `number_of_reviews` | Number of reviews available              |
| `salaries`          | Number of salary-related entries         |
| `interviews`        | Number of interview-related entries      |
| `jobs`              | Number of job listings                   |
| `benefits`          | Number of benefits-related entries       |
| `photos`            | Number of company photos                 |
| `Unnamed: 0`        | Index column included in the dataset     |

*Note: The columns such as `salaries`, `interviews`, `jobs`, and `benefits` represent counts of available entries, not necessarily salary amounts or direct measurements of employee benefits.*

## 🛠️ Tools and Technologies

This project is being developed using Python and its data analysis libraries.

* **Python** – Main programming language
* **Pandas** – Data loading, cleaning, and manipulation
* **NumPy** – Numerical operations
* **Matplotlib** – Data visualization
* **Seaborn** – Statistical visualizations
* **Jupyter Notebook** – Analysis and documentation

## 🔍 Project Workflow

I will follow a structured data analysis process to understand the dataset and extract useful information.

### 1. Data Understanding

* Load the dataset into Python.
* Understand the number of rows and columns.
* Examine column names and data types.
* Explore sample records.
* Understand what each column represents.

### 2. Data Quality Assessment

* Check for missing values.
* Identify duplicate records.
* Examine inconsistent text values.
* Identify incorrect or unusual ratings.
* Check whether numerical information is stored in the correct format.

### 3. Data Cleaning and Preprocessing

* Remove unnecessary columns, if appropriate.
* Handle missing values.
* Remove duplicate records where necessary.
* Standardize company and industry names.
* Convert relevant columns into suitable data types.
* Clean numerical values containing suffixes such as `k` and `L`, where appropriate.

### 4. Exploratory Data Analysis (EDA)

Explore the dataset to answer questions such as:

* Which companies have the highest ratings?
* Which companies have the most employee reviews?
* Which company types are most common?
* How are company ratings distributed?
* Which companies have more job listings?
* How do reviews, salary entries, and interview entries vary across companies?
* Are there any noticeable patterns between company ratings and the number of reviews?

### 5. Data Visualization

Create visualizations to communicate the analysis clearly.

Planned visualizations include:

* Top-rated companies.
* Company distribution by type.
* Rating distribution.
* Companies with the highest number of reviews.
* Job listings across companies.
* Comparison of reviews, salaries, and interview entries.
* Relationship between company ratings and review counts.

### 6. Insights and Recommendations

* Summarize the important patterns identified during analysis.
* Highlight interesting observations about the companies.
* Explain what the findings may mean for job seekers.
* Mention data limitations that could affect interpretation.

## 📊 Expected Outcome

By the end of this project, I aim to develop a better understanding of the company information available in the dataset.

The analysis will help explore company ratings, industry distribution, review activity, job listings, and other available indicators. Visualizations and findings will be documented to make the information easier to understand.

## ⚠️ Dataset Limitations

A few limitations should be considered while interpreting the data:

* The dataset contains company-level information and may not represent every company in India.
* Ratings and review counts do not necessarily represent the experience of every employee.
* Salary-related values appear to represent the number of salary entries rather than actual salary amounts.
* Job listings and other counts may change over time.
* The dataset may contain missing, inconsistent, or outdated information.
* Relationships identified during analysis should not automatically be interpreted as cause-and-effect relationships.

## 📁 Project Structure

```text
Companies-in-India-Analysis/
│
├── Dataset/
│   └── companies_in_india.csv
│
├── Notebooks/
│   ├── 01_Data_Understanding.ipynb
│   ├── 02_Data_Quality_Assessment.ipynb
│   ├── 03_Data_Cleaning.ipynb
│   ├── 04_Exploratory_Data_Analysis.ipynb
│   ├── 05_Data_Visualization.ipynb
│   └── 06_Insights_and_Recommendations.ipynb
│
├── Visualizations/
│
├── README.md
└── requirements.txt
```

## 🚀 Project Status

**Status:** In Progress

This project is being developed step by step, starting with understanding the dataset and assessing its quality, followed by data cleaning, exploratory analysis, visualization, and insight generation.

---

*This project is part of my continuous learning journey in Python and Data Analytics. My focus is on developing practical analytical skills and learning how to turn raw data into meaningful business insights.*

