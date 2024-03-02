![alt_text](introduction-to-machine-learning.png "image_tooltip")

# **Project description**

Mobile carrier Megaline has found out that many of their subscribers use legacy plans. They want to develop a model that would analyze subscribers' behavior and recommend one of Megaline's newer plans: Smart or Ultra.

You have access to behavior data about subscribers who have already switched to the new plans (from the project for the Statistical Data Analysis course). For this classification task, you need to develop a model that will pick the right plan. Since you’ve already performed the data preprocessing step, you can move straight to creating the model.

Develop a model with the highest possible _accuracy_. In this project, the threshold for _accuracy_ is 0.75. Check the _accuracy_ using the test dataset.


### **Project instructions**



1. Open and look through the data file. Path to the file:`datasets/users_behavior.csv` [Download dataset](https://practicum-content.s3.us-west-1.amazonaws.com/datasets/users_behavior.csv)
2. Split the source data into a training set, a validation set, and a test set.
3. Investigate the quality of different models by changing hyperparameters. Briefly describe the findings of the study.
4. Check the quality of the model using the test set.
5. Additional task: sanity check the model. This data is more complex than what you’re used to working with, so it's not an easy task. We'll take a closer look at it later.


### **Data description**

Every observation in the dataset contains monthly behavior information about one user. The information given is as follows:



1. `сalls` — number of calls,
2. `minutes` — total call duration in minutes,
3. `messages` — number of text messages,
4. `mb_used` — Internet traffic used in MB,
5. `is_ultra` — plan for the current month (Ultra - 1, Smart - 0).

## Conclusion

### Data Preparation

Upon reviewing the data file `users_behavior.csv`, we proceeded to split the dataset into training, validation, and test sets.

### Model Development

Various models were trained and evaluated with different hyperparameters to determine the model with the highest accuracy. The findings of the study revealed that altering hyperparameters led to variations in model performance, but no single combination consistently exceeded the predefined accuracy threshold of 0.75.

### Model Evaluation

The quality of the best-performing model was assessed using the test set. The accuracy of the model was compared against the predefined threshold, and while it did not consistently meet the target accuracy, it provided valuable insights into subscriber behavior and plan recommendation.

### Model Result Comparison

**Model Result Comparison Table Summary**

| Model                   | RMSE | Accuracy Score | Precision | Recall | F1-Score | ROC AUC |
|-------------------------|------|----------------|-----------|--------|----------|---------|
| Decision tree classifier| 0.461| 0.7869         | 0.7521    | 0.4489 | 0.5623   | 0.6920  |
| Random Forest Classifier| 0.473| 0.7760         | 0.6733    | 0.5153 | 0.5838   | 0.7028  |
| Logistic Regression     | 0.498| 0.7511         | 0.9285    | 0.1989 | 0.3277   | 0.5961  |

**Observations:**
- **Accuracy Score:** Decision tree classifier has the highest value followed by Random Forest classifier.
- **Precision:** Logistic Regression achieved the highest value, followed by Decision tree classifier.
- **Recall:** Random Forest classifier has the highest value, followed by Decision tree classifier.
- **F1-Score:** Random Forest classifier has the highest value, followed by Decision tree classifier.
- **ROC AUC:** Random Forest classifier has the highest value, followed by Decision tree classifier.

After evaluating the metrics table above, Random Forest Classifier performed better followed by Decision tree classifier.

### Additional Insights

- **Test Score Results:** Decision tree classifier had better results on average, followed by Random Forest Classifier.
- **Train Score Results:** Random Forest had the highest result on average.

## Recommendations

1. **Further Exploration:** Continue exploring different model architectures, hyperparameters, and feature engineering techniques to improve model performance and achieve the desired accuracy threshold.

2. **Data Enrichment:** Consider incorporating additional features or external data sources to enhance the predictive power of the model and capture more nuanced subscriber behavior patterns.

3. **Model Interpretability:** Invest in techniques for interpreting model predictions to gain deeper insights into the factors driving plan recommendation decisions.

4. **Continuous Evaluation:** Regularly evaluate model performance and refine the model based on feedback from real-world subscriber behavior to ensure ongoing effectiveness and relevance.

By implementing these recommendations, Megaline can develop a robust model for recommending plans to subscribers, thereby improving customer satisfaction and loyalty.
