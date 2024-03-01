# **Project description**

The data is stored in three files:



1. `gold_recovery_train.csv` — training dataset [download](https://practicum-content.s3.us-west-1.amazonaws.com/datasets/gold_recovery_train.csv)
2. `gold_recovery_test.csv` — test dataset [download](https://practicum-content.s3.us-west-1.amazonaws.com/datasets/gold_recovery_test.csv)
3. `gold_recovery_full.csv` — source dataset [download](https://practicum-content.s3.us-west-1.amazonaws.com/datasets/gold_recovery_full.csv)

Data is indexed with the date and time of acquisition (`date` feature). Parameters that are next to each other in terms of time are often similar.

Some parameters are not available because they were measured and/or calculated much later. That's why, some of the features that are present in the training set may be absent from the test set. The test set also doesn't contain targets.

The source dataset contains the training and test sets with all the features.

You have the raw data that was only downloaded from the warehouse. Before building the model, check the correctness of the data. For that, use our instructions.

## Conclusion

### Data Preparation

During the data preparation phase, the provided files were opened and examined for correctness. It was identified that there was a missing value in the `df_train` dataset. Additionally, the calculation of the recovery feature (`rougher.output.recovery`) was verified against the provided feature values, resulting in a negligible difference of 9.303415616264301e-15.

### Data Analysis

An analysis of the concentration of metals (_Au, Ag, Pb_) at different purification stages revealed significant changes, particularly in the concentration of gold. The particle size distribution of the feed in both the training and test sets was compared, and it was found that the distributions were evenly spread across both datasets.

An anomaly with a value of 0 was observed at all stages of purification, and it was deemed necessary to remove these anomalies. Missing values in all datasets were handled by filling them with the median value.

### Building the Model

A function was created to calculate the final SMAPE value for evaluation. Various models were trained and evaluated using cross-validation, with the Random Forest model with a depth of 3 identified as the best-performing model.

#### Summary:

We compared several models with Dummy Regressor (sMAPE=0.0779):

1) Linear regression: $sMAPE_{mean}\approx$0.0958

2) Decision tree regressor: $sMAPE_{mean}\approx$0.1440

3) Random forest regressor: $sMAPE_{mean}\approx$0.096

Linear regression and Random forest regressor have the best result according to the sMAPE.

### Overall

The SMAPE for the training data was found to be 7.49%, while the SMAPE for the test data was 13.99%. The lower SMAPE value for the training data indicates that the model performs better in predicting the target variable for the data it was trained on.

## Recommendations

1. **Further Analysis**: Explore additional features or refine existing ones to improve model performance further.
   
2. **Optimization**: Experiment with different hyperparameters and algorithms to find the optimal model configuration.
   
3. **Continuous Monitoring**: Regularly monitor model performance and retrain as necessary to adapt to changing data patterns and ensure continued effectiveness.
   
4. **Data Quality Assurance**: Implement robust data quality assurance measures to detect and handle anomalies and missing values effectively.

## Recommendations

1. **Further Analysis**: Explore additional features or refine existing ones to improve model performance further.
   
2. **Optimization**: Experiment with different hyperparameters and algorithms to find the optimal model configuration.
   
3. **Continuous Monitoring**: Regularly monitor model performance and retrain as necessary to adapt to changing data patterns and ensure continued effectiveness.
   
4. **Data Quality Assurance**: Implement robust data quality assurance measures to detect and handle anomalies and missing values effectively.

## **Project instructions**

1. Prepare the data

1.1. Open the files and look into the data.

Path to files:



1. _/datasets/gold_recovery_train.csv_
2. _/datasets/gold_recovery_test.csv_
3. _/datasets/gold_recovery_full.csv_

1.2. Check that recovery is calculated correctly. Using the training set, calculate recovery for the `rougher.output.recovery` feature. Find the _MAE_ between your calculations and the feature values. Provide findings.

1.3. Analyze the features not available in the test set. What are these parameters? What is their type?

1.4. Perform data preprocessing.

2. Analyze the data

2.1. Take note of how the concentrations of metals (_Au, Ag, Pb_) change depending on the purification stage.

2.2. Compare the feed particle size distributions in the training set and in the test set. If the distributions vary significantly, the model evaluation will be incorrect.

2.3. Consider the total concentrations of all substances at different stages: raw feed, rougher concentrate, and final concentrate. Do you notice any abnormal values in the total distribution? If you do, is it worth removing such values from both samples? Describe the findings and eliminate anomalies.

3. Build the model

3.1. Write a function to calculate the final _sMAPE_ value.

3.2. Train different models. Evaluate them using cross-validation. Pick the best model and test it using the test sample. Provide findings.

Use these formulas for evaluation metrics:

  <a href="url"><img src="moved__smape_1_1589900649.jpg " height="auto"  style="border-radius:20px"></a>
  <a href="url"><img src="moved_smape_1576239058_1589899769.jpg" height="auto"  style="border-radius:20px"></a>
