# LITA-Customer-Data-Project
Data Analysis and Visualization of a Customer Data.

### Project Title- Customer Data Analysis and Visualization.
---

### Project Overview
This Analysis aims to extract key information from the Data and provide insights on the Customer Data. With the use of the analysis we seek to gain insights in the performance of the Subscription types it's popularity among the  Customers and with the insights gotten we would be able to make reasonable decisions which will helps us to tell compelling stories around the data.

### Data Source
This data is an Excel Form which has been shared as part of my portfolio project at Ladies in Tech Africa.

### Tools Used
- Ms Excel for;
  1. Data cleansing
  2. Analysis and
  3. Visualization 
- SQL- Structured Query Language for Querying and Analysis 
- Power BI for Analysis and the creation of dashboards and reports
- GitHub for building portfolio

### Data Cleaning and Preparations
In the initial phase we make us of the Microsoft Excel to;
  - Load and inspect the data,
  - Use of certain Excel Functions to calculate metrics and draw out values from the data which are essential,
  - Cleaning and Formatting of the data.

### Exploratory Data Analysis 
In our Exploration of the Customer Data we seek to gain insights and answer some questions such as;
- To understand Customer behavior 
- To track Subscription types
- And identify key trends in Cancellations and Renewals.

### Data Analysis 
This is where we include some Excel functions, some basic likes of code and even some DAX functions and also making use of the Calculated column function in Power BI. Below we shall be making use of each tool to analyze our Customer Data.
1. Ms Excel-
In using Microsoft Excel in the analysis of the Customer Data we have been able to make use of some Excel Functions in getting new insights into our data such as;
```
=SUM(F2-E2)
```
This function was used to calculate the subscription of the customers with the use of the column 'Subscription Start's and ' Subscription End' to achieve the desired result. 


2. SQL- Structured Query Language-
The SQL is used for storing and arranging data and allows it's users to query the database through the use of English-like statements known as a Query.
With the use of such queries we have been able to answer some questions which provides us key insights into the Customer Data. Here are some queries used to extract information from the data.
- To find the Total number of customers per region we made use of the below code
```
select COUNT (CustomerId)as TotalCustomer, Region from Customer_Table
group by Region
```
- From the table we want to extract the Number of customers who cancelled their subscription within 6 months and the below code was used to get this insight
```
select CustomerName from Customer_Table
where Canceled = 1
and DATEDIFF(month, SubscriptionStart, SubscriptionEnd)<=6
```
- To getting to know what are the total revenue accrued by each Subscription type the qury code use is listed below
```
select SUM(Revenue)as TotalRevenue, (SubscriptionType) from Customer_Table
group by SubscriptionType
```
- Thrpugh the use of a particular query we have been able to gain insights as ti what the most popular subscription type is 
```

```
- The next insights extracted was the average subscription duration of all customers
```

```
- Also the customers with subscriptions longer than 12 months was pulled out with the use if this query
```

```
- Also with the use if SQL we were able to know The top 3 Regions who had the highest Cancellations
```

```
- And lastly we were able to extract the active subscriptions and the cancelled subscriptions through the use of an SQL code
```

```

3. Power BI-
The use of DAX Functions to calculate measures which were applied to the data enabled us to be able to visualize it effectively and tell us more about the Customer Data 
