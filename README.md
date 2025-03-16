# CRM Sales Opportunities Analysis

## Introduction

Customer Relationship Management (CRM) systems are essential tools for managing interactions with customers and potential clients. This project focuses on analyzing a CRM dataset containing sales opportunities for a fictitious company that sells computer hardware. The objective is to gain insights into the performance of sales teams and agents, and determine which products have the highest success rates in sales deals.

By leveraging Exploratory Data Analysis (EDA), we aim to uncover key trends that can help improve sales strategies and decision-making.

## Dataset Overview

**File Name:** `CRM_Sales_Opportunities.csv`

**Data Source:** Maven Analytics (Fictitious dataset) [Link to data](https://app.mavenanalytics.io/datasets?search=CRM+Sales+Opportunities)


**Dataset Description:** The dataset contains sales pipeline data, including accounts, products, sales teams, and sales opportunities.

### Key Columns:

- **account**: Unique identifier for each client.
- **sales_team**: The sales team responsible for handling the opportunity.
- **sales_agent**: The specific agent assigned to the opportunity.
- **product**: The product associated with the opportunity.
- **opportunity_date**: Date when the opportunity was created.
- **closed_date**: Date when the opportunity was closed.
- **deal_stage**: Status of the opportunity (won, lost, etc.).

## Data Preparation and Cleaning

To ensure the data is clean and ready for analysis, the following preprocessing steps were performed:

### Data Cleaning

#### Handling Missing Values:
- Removed rows where `closed_date` was missing since they lack closure information.

#### Date Formatting:
- Converted `opportunity_date` and `closed_date` columns to datetime format to enable time-based analysis.

#### Data Merging:
- Merged multiple datasets on the `account` column.
- Eliminated duplicate columns such as `manager_x` and `manager_y` to retain only relevant information.

### Feature Engineering

#### Extracted Time-Based Features:
- Created `year` and `quarter` columns to facilitate quarterly trend analysis.

#### Created a Binary Win Column:
- Added a `Cdeal` column where `1` represents a won deal and `0` represents a lost deal.

## Exploratory Data Analysis (EDA)

EDA was performed to extract meaningful insights from the dataset.

### 1. Sales Team Performance

- **Metric Analyzed:** Win rate per sales team.
- **Formula:** `win_rate = wins / total_opportunities`
- **Visualization:** Bar plot comparing the win rates of different sales teams.
- **Insight:** Some teams perform significantly better than others, highlighting potential areas for improvement.

### 2. Sales Agent Performance

- **Metric Analyzed:** Individual agent win rates.
- **Method:**
  - Identified the top 5 agents with the highest win rates.
  - Sorted agents based on their success in closing deals.
- **Visualization:** Bar plot displaying the performance of top-performing agents.
- **Insight:** Helps in identifying the best sales agents and those who may require additional training.

### 4. Product Performance Analysis

- **Metric Analyzed:** Products with the highest number of won deals.
- **Method:**
  - Filtered data to include only won deals.
  - Grouped by product to count the number of successful sales.
- **Visualization:** Bar plot displaying the top-performing products.
- **Insight:** Identifies which products have the best sales success rates, helping refine sales strategies.

## Key Findings and Business Impact

### Sales Agent Performance Gaps:
- **Hayden Neloms** had the highest win rate (0.703947) with 152 oppprtunities, while **Lajuana Vencill** showed weaker performance with 231 oppprtunities and 0.549784 win rate (may need support), indicating the need for targeted training or sales process improvements.

### Top Sales Agents:
- The analysis identified top-performing agents who could be rewarded or used as benchmarks for training lower-performing agents.


### Best-Selling Products:
- **GTX Basic** had the highest win rate, making it a key product to focus on in marketing and sales strategies.

### Best-Selling Region:
- **The central region has the most wins with 1629 win** , making it a key region to focus on in marketing and sales strategies.

### Best-Selling Products:
- **The retail sector has the most wins with 799 win**, making it a key Sector to focus on in marketing and sales strategies.

## Technologies Used

This project was implemented using the following tools and technologies:

### Python Libraries:
- `pandas` for data manipulation and preprocessing.
- `matplotlib` and `seaborn` for data visualization.
- Jupyter Notebook / Google Colab for running analysis.

## Repository Structure

## Future Work (still working on it )

### Predictive Modeling:
- Build a machine learning model to predict the likelihood of winning an opportunity based on historical data.

### Sales Strategy Optimization:
- Identify patterns in lost deals to improve win rates.

### Automated Dashboard:
- Develop a **Power BI** or **Tableau** dashboard for real-time sales tracking.

## Conclusion

This project provided valuable insights into sales team performance, agent success rates, quarterly trends, and product performance. These findings can help businesses optimize their sales strategies, improve agent training, and allocate resources more effectively.
