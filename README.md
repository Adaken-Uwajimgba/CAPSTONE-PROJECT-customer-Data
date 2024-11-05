## CAPSTONE-PROJECT
# PROJECT(2) TITLE:CUSTOMER DATA ANALYSIS

## OUTLINES
---
[PROJECT SUMMARY FOR CUSTOMER DATA BASED ON SUBSCRIPTION](#project-summary-for-customer-data-based-on-subscription)

[DATA SOURCES](#data-sources)

[ATTRIBUTE DESCRIPTIONS FOR CUSTOMER DATA ANALYSIS](#attribute-descriptions-for-customer-data-analysis)

[TOOLS USED](#tools-used)

[DATA CLEANING AND PREPARATION](#data-cleaning-and-preparation)

[EXPLORATORY DATA ANALYSIS](#exploratory-data-analysis)

[DATA ANALYSIS](#data-analysis)


### PROJECT SUMMARY FOR CUSTOMER DATA BASED ON SUBSCRIPTION
---
The goal of this Data Analysis is to appraise the Customer Data Analysis based on Subscription over a Specified Period of Time. The Dataset encompasses a detailed view of Customer Data, Subscription Types,Region, Subscription Renewals or cancelations and Revenue generated. The Customer Dataset provided will be used to assess Customer Behaviors by subscription(preferences,purchasing power e.t.c),determining Key trends in Subscription Renewal and cancellations

### DATA SOURCES
---
The Data source used for this Analysis is the Data customer.csv files and this is an open source Data that can be freely downloaded from any open source Platform such as [Kaggle](https://www.kaggle.com/datasets),[FRED](https://appsource.microsoft.com/en-us/product/office365/wa200003692?tab=overview) e.t.c

### ATTRIBUTE DESCRIPTIONS FOR CUSTOMER DATA ANALYSIS
---
  - CustomerID: Distinct identifier for each customer.
  - CustomerName: Name of the customer.
  - Region: Geographical Location where the customer is situated (e.g., East, South, West, North).
  - SubscriptionType: Type of subscription plan the Customer is on (e.g., Basic, Premium).
  - SubscriptionStart: Start date of the customer's subscription.
  - SubscriptionEnd: End date of the customer's subscription.
  - Canceled: Shows if the subscription was canceled (TRUE or FALSE).
  - Revenue: Revenue generated from the customer's subscription.
  - Subscription Duration: Duration (in days) of the subscription period

### TOOLS USED
---
1) Microsoft Excel(xlxs)
   - Data Cleaning
   - Pivot Tables
   - Analysis
   - Data Visualization.
2) Structured Query Language(SQL)
   - Quering Data
3) Power BI
   - Data Cleaning,
   - Data Visualization
   - For Reporting

### DATA CLEANING AND PREPARATION
---
In the Early Stages of the Data cleaning and preparations, we implemented the following actions:-
- i) Data loading and Inspection
- ii) Removal of Duplicates
- iii) Data cleaning and Formatting

### EXPLORATORY DATA ANALYSIS
---
EDA comprises of the exploring of this Data to give Answers to some questions such as;
- Retrieve the total number of customers from each region.
- Find the most popular subscription type by the number of customers.
- Find customers who canceled their subscription within 6 months.
- Calculate the average subscription duration for all customers.
- Find customers with subscriptions longer than 12 months.
- Calculate total revenue by subscription type.
- Find the top 3 regions by subscription cancellations.
- Find the total number of active and canceled subscriptions.

### DATA ANALYSIS
---
This is where we include some Basic lines of code/Queries or even some of the DAX expressions used during the Analysis;
```SQL
Select region, 
COUNT(*) AS total_customers 
from [dbo].[Lita_project 2-Customer Data]
GROUP BY Region
```
```SQL
Select TOP 1 Subscriptiontype,
COUNT(*) AS total_customers
From [dbo].[Lita_project 2-Customer Data]
Group by SubscriptionType
ORDER BY total_customers DESC
```
