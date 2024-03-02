
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

# Conclusion

## Project Overview

Beta Bank faced the challenge of customer attrition and aimed to predict whether a customer would leave the bank soon. The project required building a model with a maximum possible F1 score of at least 0.59. Additionally, the AUC-ROC metric was used for evaluation and comparison with the F1 score.

## Project Execution

1. **Data Preparation**: The data from the `Churn.csv` file was downloaded and prepared. This involved examining the balance of classes and applying encoding to non-numerical columns using one-hot encoding (`get_dummies`).

2. **Initial Model Training**: The dataset showed an imbalance with the target variable, where the ratio of ones to zeros was approximately 1:4. A Decision Tree classifier was trained without addressing the class imbalance, and initial performance metrics were obtained.

3. **Improvement of Model Quality**:
   - Class Imbalance Fixes: Two approaches were used to address class imbalance: Random Undersampling and Synthetic Minority Over-sampling Technique (SMOTE).
   - Model Training and Validation: Different models were trained on training and validation sets, and their performance was evaluated. A Decision Tree classifier showed the best performance after balancing the data.
   - Final Testing: The best-performing model was tested on the test set, resulting in improved performance metrics.

## Findings

- Initial Model Performance:
  - F1-Score: 0.49386
  - ROC AUC: 0.68322
- Final Model Performance:
  - F1-Score: 0.59107
  - ROC AUC: 0.84034

The final model, a Decision Tree classifier trained after balancing the data, demonstrated improved performance compared to the initial model. The ROC curve plot comparison between the two models indicated that the Decision Tree model covered more area, indicating better overall performance.

## Recommendations

1. **Continuous Monitoring**: Regularly monitor customer behavior and retrain the model periodically to adapt to changing patterns.
2. **Further Experimentation**: Explore additional techniques for addressing class imbalance and model optimization to potentially enhance performance further.
3. **Customer Engagement Strategies**: Implement proactive customer engagement strategies to retain at-risk customers identified by the model.

## Future Improvements

1. **Ensemble Methods**: Experiment with ensemble methods such as Random Forests or Gradient Boosting to potentially improve predictive performance.
2. **Feature Engineering**: Explore additional features or feature transformations to capture more nuanced patterns in customer behavior.
3. **Hyperparameter Tuning**: Conduct more extensive hyperparameter tuning to fine-tune model performance and generalization capabilities.

By implementing these recommendations and pursuing future improvements, Beta Bank can better predict and mitigate customer attrition, ultimately improving customer retention and profitability.

