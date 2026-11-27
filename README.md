<p align="center">
  <img src="images/project-banner.png" alt="European Bank Customer Churn Analysis" width="100%">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Microsoft%20Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white" alt="Microsoft Excel">
  <img src="https://img.shields.io/badge/PivotTables-Data%20Analysis-0078D4?style=for-the-badge" alt="PivotTables">
  <img src="https://img.shields.io/badge/Correlation-Analysis-00A4EF?style=for-the-badge" alt="Correlation Analysis">
  <img src="https://img.shields.io/badge/Dashboard-Interactive-F2C811?style=for-the-badge" alt="Interactive Dashboard">
  <img src="https://img.shields.io/badge/Records-10%2C000-2EA44F?style=for-the-badge" alt="10,000 Records">
</p>

## Project Overview

This project analyses customer churn in a European bank using a dataset of **10,000 customer records**. The aim is to identify customer characteristics associated with churn and provide practical recommendations that can support customer-retention decisions.

The analysis was completed in **Microsoft Excel** using:

- Data cleaning and preparation
- PivotTables
- PivotCharts
- Correlation analysis
- Scatter plots and trendlines
- An interactive Excel dashboard

## Business Problem

Customer churn reduces revenue, weakens customer relationships, and can increase the cost of acquiring replacement customers. This project examines the bank's customer data to identify groups with higher churn rates and areas where targeted retention strategies may be most effective.

## Project Objectives

- Measure the bank's overall customer churn rate.
- Examine the relationship between customer age and churn.
- Examine the relationship between account balance and churn.
- Compare churn rates by number of banking products.
- Determine whether inactive customers are more likely to churn.
- Compare churn rates across France, Germany, and Spain.
- Present the results through PivotTables, charts, and an Excel dashboard.

## Research Questions

1. Does customer age have a relationship with customer churn?
2. Is there a relationship between customers' account balances and their likelihood of churning?
3. How does the number of banking products used by customers affect their churn rate?
4. Are inactive customers more likely to churn than active customers?
5. Does customer churn rate vary across geographical locations?

## Dataset Description

The cleaned dataset contains **10,000 customer records** and the following variables:

| Variable | Description |
|---|---|
| `CustomerId` | Unique customer identifier |
| `Surname` | Customer surname |
| `CreditScore` | Customer credit score |
| `Geography` | Customer country: France, Germany, or Spain |
| `Gender` | Customer gender |
| `Age` | Customer age |
| `Tenure` | Number of years the customer has stayed with the bank |
| `Balance` | Customer account balance |
| `NumOfProducts` | Number of banking products held |
| `HasCrCard` | Whether the customer has a credit card |
| `IsActiveMember` | Whether the customer is active |
| `EstimatedSalary` | Estimated annual salary |
| `Exited` | Churn indicator: 1 = exited, 0 = stayed |

Additional text-based fields were created to make the Excel analysis easier to interpret, including product-count labels, activity-status labels, and churn-status labels.

## Data Analysis Process

### 1. Data Preparation

- Reviewed the dataset for consistency and analysis readiness.
- Retained numeric churn values for correlation analysis.
- Created readable category labels such as `Exited`, `Stayed`, `Active`, and `Not Active` for PivotTables and charts.

### 2. Exploratory and PivotTable Analysis

PivotTables were used to calculate and compare churn percentages by:

- Number of banking products
- Customer activity status
- Geography

### 3. Correlation Analysis

Pearson correlation was used to measure the direction and strength of the relationship between:

- Age and churn
- Account balance and churn

Because churn is coded as a binary variable, these results are equivalent to point-biserial correlations. They show association, not causation, and should not be treated as a complete predictive model.

### 4. Data Visualisation

The workbook includes:

- Scatter plots with trendlines for age, balance, and churn
- Column and bar charts for group comparisons
- Pie charts for churn composition
- A consolidated Excel dashboard

## Key Findings

### Overall Churn

- **2,037 of 10,000 customers exited the bank.**
- The overall churn rate was **20.37%**, while **79.63%** of customers stayed.

### Age and Churn

- The correlation between age and churn was **r = 0.2853**.
- This indicates a **weak-to-moderate positive association**.
- Older customers showed a greater tendency to churn, although age alone does not determine whether a customer will leave.

### Account Balance and Churn

- The correlation between account balance and churn was **r = 0.1185**.
- This represents a **very weak positive association**.
- Customers who stayed had an average balance of approximately **72,745.30**.
- Customers who exited had an average balance of approximately **91,108.54**.
- The difference was approximately **18,363.24**, suggesting the bank was losing customers with comparatively high balances, even though balance alone had limited predictive strength.

### Number of Banking Products

| Number of products | Churn rate |
|---|---:|
| 1 | 27.72% |
| 2 | 7.58% |
| 3 | 82.71% |
| 4 | 100.00% |

Customers with **two products** had the lowest churn rate. Customers with **three or four products** recorded extremely high churn rates. The four-product result should be interpreted carefully because this is a small customer group.

### Customer Activity Status

| Activity status | Churn rate |
|---|---:|
| Active | 14.27% |
| Not Active | 26.85% |

Inactive customers were substantially more likely to churn than active customers, highlighting the importance of customer engagement.

### Geography

| Geography | Churn rate |
|---|---:|
| France | 16.16% |
| Germany | 32.44% |
| Spain | 16.67% |

Germany recorded the highest churn rate, at approximately twice the rate observed in France and Spain.

## Recommendations

1. **Prioritise inactive customers:** Use personalised communication, service reminders, and relevant offers to re-engage inactive customers before they churn.
2. **Develop an older-customer retention programme:** Review service accessibility, support quality, digital-banking experience, and relationship-management needs for older customers.
3. **Protect high-balance relationships:** Assign proactive retention triggers for high-balance customers, including relationship-manager outreach and service-quality reviews.
4. **Investigate the three- and four-product segments:** Review product suitability, pricing, service complexity, and possible cross-selling pressure. The small four-product segment should be examined at customer level before drawing broad conclusions.
5. **Conduct a Germany-specific review:** Analyse service issues, complaints, product pricing, and customer expectations in Germany to understand the unusually high churn rate.
6. **Extend the analysis:** Use logistic regression or a classification model in a future phase to assess the combined effect of several variables and evaluate predictive performance.

## Workbook Structure

The Excel workbook contains the following worksheets:

- `RESEARCH QUESTIONS`
- `EUROPEAN BANK_CLEANED`
- `CORRELATION ANALYSIS`
- `ANALYSIS - PIVOT TABLE & CHARTS`
- `INTERPRETATION`
- `EXECUTIVE SUMMARY`
- `DASHBOARD`

## Repository Structure

```text
European-Bank-Customer-Churn-Analysis/
├── README.md
├── data/
│   └── European_Bank_Customer_Churn_Cleaned.xlsx
├── analysis/
│   └── European_Bank_Churn_Analysis.xlsx
└── images/
    └── churn_dashboard.png
```

> Before publishing the repository, remove or anonymise any personal information and confirm that the dataset licence permits public redistribution.

## How to Use the Project

1. Download the Excel workbook from the `analysis` folder.
2. Open it with Microsoft Excel.
3. Review the `EXECUTIVE SUMMARY` worksheet for the main conclusions.
4. Open the `DASHBOARD` worksheet for the visual summary.
5. Review the PivotTables and correlation worksheets for the supporting analysis.

## Limitations

- The analysis identifies associations and does not establish causation.
- Correlation values involving a binary churn variable should be interpreted cautiously.
- The analysis is mainly descriptive and does not control for interactions among customer characteristics.
- Very small product groups, especially customers with four products, may produce unstable percentages.
- The dataset covers only the variables and period included in the workbook.

## Tools Used

- Microsoft Excel
- PivotTables and PivotCharts
- Pearson/point-biserial correlation
- Scatter plots and trendlines
- Excel dashboard

## Author

**Olayemi Kareem**  
Data Analysis Course Project

## Acknowledgement

This project was completed as part of a data-analysis course project using a European Bank customer-churn dataset.


