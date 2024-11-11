## CAPSTONE-PROJECT
# PROJECT(2) TITLE:CUSTOMER DATA ANALYSIS BASED ON SUBSCRIPTION

## OUTLINES
---
[SUMMARY](#summary)

[INTRODUCTION](#introduction)

[DATA DESCRIPTION](#data-description)

[PROCEDURES](#procedures)

[EXPLORATORY DATA ANALYSIS](#exploratory-data-analysis)

[DATA ANALYSIS](#data-analysis)


### SUMMARY
---
This Project appraises the Customer Data Analysis based on Subscription over a Specified Period of Time. The Dataset encompasses a detailed view of Customer Data, Subscription Types,Region, Subscription Renewals or cancelations and Revenue generated. The Customer Dataset provided will be used to assess Customer Behaviors by subscription(preferences,purchasing power e.t.c),determining Key trends in Subscription Renewal and cancellations

### INTRODUCTION
---
#### Problem Statement
We are addressing the issue of comprehending Customer Behavior in terms of preferences, location and any like factors that contribute to the choices they make pertaining to their Subscription type, subscription Duration.

#### Aims
- To understand Customer Behavior
- To Monitor and categorise the different types of subscription plans being used by each customer.
- To analyze patterns and behaviors related to how customers renew or cancel their subscriptions.

### DATA DESCRIPTION 
---
#### Data Sources
The Data source used for this Analysis is the Data customer.csv files and this is an open source Data that can be freely downloaded from any open source Platform such as [Kaggle](https://www.kaggle.com/datasets),[FRED](https://appsource.microsoft.com/en-us/product/office365/wa200003692?tab=overview) e.t.c

#### Data Attributes
  - CustomerID: Distinct identifier for each customer.
  - CustomerName: Name of the customer.
  - Region: Geographical Location where the customer is situated (e.g., East, South, West, North).
  - SubscriptionType: Type of subscription plan the Customer is on (e.g., Basic, Premium).
  - SubscriptionStart: Start date of the customer's subscription.
  - SubscriptionEnd: End date of the customer's subscription.
  - Canceled: Shows if the subscription was canceled (TRUE or FALSE).
  - Revenue: Revenue generated from the customer's subscription.
  - Subscription Duration: Duration (in days) of the subscription period

### PROCEDURES
---
#### Tools Used
1) Microsoft Excel(xlxs)
   - Data Cleaning
   - Pivot Tables
   - Analysis
   - Data Visualization.
2) Microsoft SQL Server([SMSS)](https://www.microsoft.com/en-us/sql-server/sql-server-2022)
   - Quering Data and preprocessing
3) Power BI([Download Here)](https://www.microsoft.com/en-us/download/details.aspx?id=58494)
   - Data Cleaning,
   - Data Visualization
   - For Reporting

#### DATA CLEANING AND PREPARATION
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
#### Using SQL for the Customer Data Analysis![Screenshot (27)](https://github.com/user-attachments/assets/2a73224d-b485-4b4d-a3e6-0d4c39571dfd)

Below are the uploaded Screenshots for the Queries we ran  while exploring this Dataset.
First we create our Database
```SQL
CREATE DATABASE Lita_PROJECT 2-Customer Data
```
- Query 1;Retrieve the total Number of Customers from each region
![Screenshot (28)](https://github.com/user-attachments/assets/93946424-6fa7-4e98-855d-ef601e1c2160)

- Query 2;Find the most Popular Subscription type by the number of customers
![Screenshot (29)](https://github.com/user-attachments/assets/5a05f02e-5027-4628-85d8-dfe1ea1be3a0)

- Query 3;Find Customers who canceled their subscription within 6 months

- Query 4;Calculate the average subscription duration for customers
![Screenshot (30)](https://github.com/user-attachments/assets/13982e60-cbca-4d5a-bea8-6f93ca4f2f07)



