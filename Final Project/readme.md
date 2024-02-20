AN OVERVIEW OF CUSTOMER CHURN

Customer churn, also known as customer attrition, refers to the phenomenon where customers or subscribers discontinue their association with a particular company or service. This metric holds significant importance as retaining existing customers proves to be more cost-effective than acquiring new ones, as it eliminates the expenses associated with sales and marketing. Customer retention is particularly advantageous as it signifies that a company has already established trust and loyalty among its customer base.

In the telecommunications industry, it is crucial for companies to accurately predict which customers are at a high risk of churning.

There are several methods available to calculate this metric, such as measuring the total number of customers lost, determining the percentage of customers lost in relation to the company's overall customer count, evaluating the value of recurring business lost, or assessing the percentage of recurring value lost. However, in the context of this dataset, customer churn is defined as a binary variable for each individual customer, and the objective is not to calculate the churn rate. Instead, the aim is to identify and quantify the factors that influence the churn rate.

This project is considered to be relatively straightforward and suitable for beginners, as it involves a smaller number of variables. While it may not be an ideal scenario for implementing neural networks due to the limited number of training examples, it can still serve as a valuable tool for understanding the fundamentals of neural networks.

In the rapidly evolving telecommunications industry, it is imperative for companies to adapt quickly and stay attuned to the ever-changing preferences of consumers and market trends. One of the key challenges faced by telecommunications providers globally is the phenomenon of "customer churn", which occurs when customers choose to discontinue using a company's services. For businesses, comprehending and reducing churn is crucial for ensuring sustained profitability and expansion.

This endeavor delves into a comprehensive undertaking to forecast and comprehend customer churn through the utilization of machine learning. By harnessing the power of data, we uncover valuable insights that can inform effective strategies for customer retention.

**Project Description**

The **telecom operator Interconnect** would like to forecast the churn of their clients.

**Business Problem Statement**: The company wants to forecast which users are planning to leave

**Business Value**: To ensure loyalty, those who are going to leave, will be offered with promotional codes.

Churn (or churn rate) is number of customers disconnecting their service over a given time period

In term of a machine learning problem our goal is to classify each client into one of two groups:



* Loyal customers who won’t churn
* Customers who will churn in the future

**Dataset**

The data consists of files obtained from different source:



* Contract.csv - contract information
* Personal.csv - The client’s personal data
* Internet.csv - information about Internet services
* Phone.csv - Information about telephone services

The customerID column contains a unique code assigned to each client.

**Target** is in the EndDate column.
