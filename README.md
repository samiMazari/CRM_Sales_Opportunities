# CRM_Sales_Opportunities
B2B sales pipeline data from a fictitious company that sells computer hardware, including information on accounts, products, sales teams, and sales opportunities.

CRM Sales Opportunities Analysis

Introduction

This project aims to analyze a CRM dataset containing sales opportunities for a fictitious company selling computer hardware. The goal is to extract insights on the performance of sales teams, agents, quarterly trends, and the most successful products.

Data Used

File Name: CRM_Sales_Opportunities.csv

Key Columns:

account: Client identifier

sales_team: Assigned sales team

sales_agent: Responsible agent

product: Product involved

opportunity_date: Date of the opportunity

closed_date: Closing date

deal_stage: Opportunity status (won, lost, etc.)

Data Preparation

Cleaning and Transformation

Removed rows with missing closed_date.

Converted date columns (opportunity_date, closed_date) to datetime format.

Created new columns:

year and quarter for quarterly trends

win (1 if won, 0 otherwise) to facilitate analysis

Merged multiple datasets on the account column, removing duplicates (manager_x, manager_y).

Exploratory Data Analysis (EDA)

Sales Team Performance

Calculated win rate per team (win_rate = wins / total_opportunities).

Visualized using a bar plot.

Sales Agent Performance

Identified the top 5 agents with the highest win rate.

Displayed results using a bar plot.

Quarterly Trends

Analyzed the number of opportunities and win rate per quarter.

Visualized using a line chart.

Product Performance

Identified products with the highest number of won deals.

Sorted results and displayed using a bar plot.

Key Findings

Team X has the highest win rate, while Team Y is struggling.

Agent Z is the top performer, with a high win rate.

There is a rise in opportunities in Q2 each year.

Product A has the highest conversion rate in won deals.

Technologies Used

Python (Pandas, Matplotlib, Seaborn)

Jupyter Notebook / Google Colab for analysis

Markdown for documentation

Files

crm_sales_analysis.ipynb: Notebook containing Python code

crm_sales_report.md: Summary report in Markdown
