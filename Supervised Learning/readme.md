
# **Project description**

Beta Bank customers are leaving: little by little, chipping away every month. The bankers figured out it’s cheaper to save the existing customers rather than to attract new ones.

We need to predict whether a customer will leave the bank soon. You have the data on clients’ past behavior and termination of contracts with the bank.

Build a model with the maximum possible _F1_ score. To pass the project, you need an _F1_ score of at least 0.59. Check the _F1_ for the test set.

Additionally, measure the _AUC-ROC_ metric and compare it with the _F1_.


### **Project instructions**



1. Download and prepare the data. Explain the procedure.
2. Examine the balance of classes. Train the model without taking into account the imbalance. Briefly describe your findings.
3. Improve the quality of the model. Make sure you use at least two approaches to fixing class imbalance. Use the training set to pick the best parameters. Train different models on training and validation sets. Find the best one. Briefly describe your findings.
4. Perform the final testing.


### **Data description**

The data can be found in `/datasets/Churn.csv` file.[ Download the dataset.](https://practicum-content.s3.us-west-1.amazonaws.com/datasets/Churn.csv)

Features



1. _RowNumber_ — data string index
2. _CustomerId_ — unique customer identifier
3. _Surname_ — surname
4. _CreditScore_ — credit score
5. _Geography_ — country of residence
6. _Gender_ — gender
7. _Age_ — age
8. _Tenure_ — period of maturation for a customer’s fixed deposit (years)
9. _Balance_ — account balance
10. _NumOfProducts_ — number of banking products used by the customer
11. _HasCrCard_ — customer has a credit card
12. _IsActiveMember_ — customer’s activeness
13. _EstimatedSalary_ — estimated salary

Target



1. _Exited_ — сustomer has left