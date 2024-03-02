## **Project description**

You work for the OilyGiant mining company. Your task is to find the best place for a new well.

Steps to choose the location:



* Collect the oil well parameters in the selected region: oil quality and volume of reserves;
* Build a model for predicting the volume of reserves in the new wells;
* Pick the oil wells with the highest estimated values;
* Pick the region with the highest total profit for the selected oil wells.

You have data on oil samples from three regions. Parameters of each oil well in the region are already known. Build a model that will help to pick the region with the highest profit margin. Analyze potential profit and risks using the _Bootstrapping_ technique.


### **Project instructions**



1. Download and prepare the data. Explain the procedure.
2. Train and test the model for each region: \
 2.1. Split the data into a training set and validation set at a ratio of 75:25. \
 2.2. Train the model and make predictions for the validation set. \
 2.3. Save the predictions and correct answers for the validation set. \
 2.4. Print the average volume of predicted reserves and model _RMSE. \
_ 2.5. Analyze the results.
3. Prepare for profit calculation: \
 3.1. Store all key values for calculations in separate variables. \
 3.2. Calculate the volume of reserves sufficient for developing a new well without losses. Compare the obtained value with the average volume of reserves in each region. \
 3.3. Provide the findings about the preparation for profit calculation step.
4. Write a function to calculate profit from a set of selected oil wells and model predictions: \
 4.1. Pick the wells with the highest values of predictions. \
 4.2. Summarize the target volume of reserves in accordance with these predictions \
 4.3. Provide findings: suggest a region for oil wells' development and justify the choice. Calculate the profit for the obtained volume of reserves.
5. Calculate risks and profit for each region: \
 5.1. Use the bootstrapping technique with 1000 samples to find the distribution of profit. \
 5.2. Find average profit, 95% confidence interval and risk of losses. Loss is negative profit, calculate it as a probability and then express it as a percentage. \
 5.3. Provide findings: suggest a region for development of oil wells and justify the choice.


### **Data description**

Geological exploration data for the three regions are stored in files:



* `geo_data_0.csv`. [download dataset](https://practicum-content.s3.us-west-1.amazonaws.com/datasets/geo_data_0.csv)
* `geo_data_1.csv`. [download dataset](https://practicum-content.s3.us-west-1.amazonaws.com/datasets/geo_data_1.csv)
* `geo_data_2.csv`. [download dataset](https://practicum-content.s3.us-west-1.amazonaws.com/datasets/geo_data_2.csv)
* _id_ — unique oil well identifier
* _f0, f1, f2_ — three features of points (their specific meaning is unimportant, but the features themselves are significant)
* _product_ — volume of reserves in the oil well (thousand barrels).

Conditions:



* Only linear regression is suitable for model training (the rest are not sufficiently predictable).
* When exploring the region, a study of 500 points is carried with picking the best 200 points for the profit calculation.
* The budget for development of 200 oil wells is 100 USD million.
* One barrel of raw materials brings 4.5 USD of revenue The revenue from one unit of product is 4,500 dollars (volume of reserves is in thousand barrels).
* After the risk evaluation, keep only the regions with the risk of losses lower than 2.5%. From the ones that fit the criteria, the region with the highest average profit should be selected.

The data is synthetic: contract details and well characteristics are not disclosed.
## Conclusion

### Data Preparation and Model Training

The geological exploration data for three regions were downloaded and prepared for analysis. Each dataset contained unique oil well identifiers and features representing points in the region. Linear regression models were trained and tested for each region using a 75:25 split between training and validation sets. Predictions were made for the validation set, and the average volume of predicted reserves and model RMSE were calculated for each region.

### Profit Calculation and Risk Assessment

Key values for profit calculation, including the budget for well development and revenue per barrel of raw materials, were stored in separate variables. The volume of reserves sufficient for profitable well development was compared with the average volume of reserves in each region. A function to calculate profit from a set of selected oil wells and model predictions was written. The wells with the highest predicted values were selected, and the target volume of reserves was summarized. Based on the findings, region 1 was suggested for oil wells' development due to its higher average profit and lower confidence interval range.

### Risk Evaluation and Region Selection

Using the bootstrapping technique with 1000 samples, the distribution of profit for each region was determined. The average profit, 95% confidence interval, and risk of losses were calculated for each region. Region 1 exhibited the highest average profit and the lowest risk of losses, making it the optimal choice for oil wells' development.

### Profits by regions
 <a href="url"><img src="conclusion04.png" height="auto" 
style="border-radius:20px"></a>
## Recommendations

1. **Further Analysis**: Conduct additional analysis to understand the geological characteristics and potential risks associated with each region in more detail.

2. **Optimization Strategies**: Explore optimization strategies to maximize profit margins and minimize risks in oil well development projects.

3. **Continuous Monitoring**: Regularly monitor and evaluate the performance of oil wells in Region 1 to ensure profitability and mitigate potential risks.

## Future Improvements

1. **Advanced Modeling Techniques**: Experiment with advanced modeling techniques, such as ensemble learning or neural networks, to potentially improve the accuracy and predictive power of the models.

2. **Enhanced Risk Assessment**: Develop more sophisticated risk assessment methods to better quantify and mitigate potential losses in oil well development projects.

3. **Exploratory Drilling**: Consider conducting exploratory drilling to gather additional data and insights into the geological characteristics of the selected region for further optimization of oil well development strategies.

By implementing these recommendations and pursuing future improvements, OilyGiant can enhance its decision-making process and optimize its oil well development projects for maximum profitability and success.

### Average Profit for each Region
 <a href="url"><img src="conclusion01.png" height="auto"  style="border-radius:20px"></a>
### 95% Confidence Interval Range for Each Region
 <a href="url"><img src="conclusion02.png" height="auto"  style="border-radius:20px"></a>
### Risk of Losses for Each Region
 <a href="url"><img src="conclusion03.png" height="auto"  style="border-radius:20px"></a>
