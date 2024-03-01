#**AN OVERVIEW OF CUSTOMER CHURN**

Customer churn, also known as customer attrition, referred to the phenomenon where customers or subscribers discontinued their association with a particular company or service. This metric held significant importance as retaining existing customers proved to be more cost-effective than acquiring new ones, as it eliminated the expenses associated with sales and marketing. Customer retention was particularly advantageous as it signified that a company had already established trust and loyalty among its customer base.

In the telecommunications industry, it was crucial for companies to accurately predict which customers were at a high risk of churning.

There were several methods available to calculate this metric, such as measuring the total number of customers lost, determining the percentage of customers lost in relation to the company's overall customer count, evaluating the value of recurring business lost, or assessing the percentage of recurring value lost. However, in the context of this dataset, customer churn was defined as a binary variable for each individual customer, and the objective was not to calculate the churn rate. Instead, the aim was to identify and quantify the factors that influenced the churn rate.

This project was considered relatively straightforward and suitable for beginners, as it involved a smaller number of variables. While it may not have been an ideal scenario for implementing neural networks due to the limited number of training examples, it could still serve as a valuable tool for understanding the fundamentals of neural networks.

In the rapidly evolving telecommunications industry, it was imperative for companies to adapt quickly and stay attuned to the ever-changing preferences of consumers and market trends. One of the key challenges faced by telecommunications providers globally was the phenomenon of "customer churn", which occurred when customers chose to discontinue using a company's services. For businesses, comprehending and reducing churn was crucial for ensuring sustained profitability and expansion.

This endeavor delved into a comprehensive undertaking to forecast and comprehend customer churn through the utilization of machine learning. By harnessing the power of data, we uncovered valuable insights that could inform effective strategies for customer retention.



# Project Summary: Churn Prediction

In the churn prediction project, a model was developed, which involved data transformation, preprocessing, and feature analysis. It was found that recent clients exhibited a propensity to churn, potentially influenced by external market factors. Additionally, the incorporation of a new feature, namely "days," had a significant impact on the model's performance. Subsequently, multiple models were constructed, including Linear Regression (LR), Decision Tree, and Gradient Boosting (GB) based on CatBoost. The AUC scores for the test data are as follows:

| Model         | AUC Score Test |
| ------------- | -------------- |
| LR            | 86.00%         |
| Decision Tree | 87.00%         |
| GB (CatBoost) | 93.00%         |

Moreover, the type of internet service and payment method were identified as additional factors associated with churn.

## Future Improvements

Moving forward, there are several avenues for future improvement:

1. **Feature Engineering**: Incorporate more granular features to capture subtle nuances in customer behavior.
2. **Advanced Techniques**: Explore advanced techniques such as ensemble learning or deep learning architectures to enhance predictive accuracy.
3. **Deeper Analysis**: Conduct further analysis on the identified factors to understand their underlying mechanisms and causal relationships with churn.
4. **Continuous Monitoring and Refinement**: Ongoing monitoring and refinement of the model with new data will be crucial to ensure its continued effectiveness in predicting churn in the dynamic telecommunications landscape.


##**Project Description**

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
