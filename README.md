### LITA Customer Subscription 


## Project Overview

Project Title: Customer Segmentation for a Subscription Service
  This project aimed to analyze customer data for a subscription service, identifying key customer segments, sunscription trends, and cancellation patterns to support data-driven business decisions

# Objective:
  To analyze subscription data to identify customer segments, trends in subscription renewals and cancellations, and insights into the most profitable subscription types
  
# Data Source: Microsoft Excel

## Tools Used

#Microsoft Excel for data analysis (pivot tables, calculations, visualizations)

#SQL for querying the data and insights

#Power BI for creating a dynamic dashboard

## Data Analysis Process
  Data Cleaning: Removing duplicates, Handling missing values and ensuring data types are correct
  Data Transformation: Combining data from multiple tables, Calculating derived metrics (e.g., subscription duration, revenue), Converting raw data into actionable insights

# Excel Analysis:

  I Analyze Customer Data Using Pivot Tables to Find Subscription Patterns and average subscription duration
  
  <img width="922" alt="Customercapture" src="https://github.com/user-attachments/assets/ebf2fb51-15a0-49b4-bc04-52fdcca6a6cd">


  # SQL Queries

  ...............Retrieve the Total Number of Customers from Each Region................
~~~sql
  SELECT Region, COUNT(CustomerID) AS TotalCustomers
FROM Customers
GROUP BY Region

.................Most Popular Subscription Type by Number of Customers...........

SELECT SubscriptionType, COUNT(CustomerID) AS CustomerCount
FROM Subscriptions
GROUP BY SubscriptionType
ORDER BY CustomerCount desc
LIMIT 1

............... Customers Who Canceled Their Subscription Within 6 Month...............

SELECT CustomerID, SubscriptionType, SubscriptionStartDate, CancellationDate
FROM Subscriptions
WHERE DATEDIFF(MONTH, SubscriptionStartDate, CancellationDate) <= 6


.................Average Subscription Duration for All Customers..................

SELECT AVG(DATEDIFF(MONTH, SubscriptionStartDate, SubscriptionEndDate)) AS AvgSubscriptionDuration
FROM Subscriptions

 ...............Customers with Subscriptions Longer Than 12 Months.........................

 SELECT CustomerID, SubscriptionType, SubscriptionStartDate, SubscriptionEndDate
FROM Subscriptions
WHERE DATEDIFF(MONTH, SubscriptionStartDate, SubscriptionEndDate) > 12

................Total Revenue by Subscription Type.......................

SELECT SubscriptionType, SUM(Revenue) AS TotalRevenue
FROM Subscriptions
GROUP BY SubscriptionType

....................Top 3 Regions by Subscription Cancellations..................

SELECT Region, COUNT(CustomerID) AS Cancellations
FROM Subscriptions
WHERE SubscriptionStatus = 'Cancelled'
GROUP BY Region
ORDER BY Cancellations desc
LIMIT 3

....................Total Number of Active and Canceled Subscriptions....................

SELECT SubscriptionStatus, COUNT(CustomerID) AS TotalSubscriptions
FROM Subscriptions
GROUP BY SubscriptionStatus


## PowerBI

![image](https://github.com/user-attachments/assets/97ef30b2-1907-451b-9083-3dd67bb28546)



# Reflection:

  This project deepened my skills in customer segmentation and provided hands-on experience with Power Bi, reinforcing my ability to derive insights that support business decision


Project Summary



Key Insights







# Soft Skills and Learning Experience



  
  
