# **Project description**

Rusty Bargain used car sales service is developing an app to attract new customers. In that app, you can quickly find out the market value of your car. You have access to historical data: technical specifications, trim versions, and prices. You need to build the model to determine the value.

Rusty Bargain is interested in:



* the quality of the prediction
* the speed of the prediction
* the time required for training


### **Project instructions**



1. Download and look at the data.
2. Train different models with various hyperparameters (You should make at least two different models, but more is better. Remember, various implementations of gradient boosting don't count as different models.) The main point of this step is to compare gradient boosting methods with random forest, decision tree, and linear regression.
3. Analyze the speed and quality of the models.

Notes:



* Use the _RMSE_ metric to evaluate the models.
* Linear regression is not very good for hyperparameter tuning, but it is perfect for doing a sanity check of other methods. If gradient boosting performs worse than linear regression, something definitely went wrong.
* On your own, work with the LightGBM library and use its tools to build gradient boosting models.
* Ideally, your project should include linear regression for a sanity check, a tree-based algorithm with hyperparameter tuning (preferably, random forrest), LightGBM with hyperparameter tuning (try a couple of sets), and CatBoost and XGBoost with hyperparameter tuning (optional).
* Take note of the encoding of categorical features for simple algorithms. LightGBM and CatBoost have their implementation, but XGBoost requires OHE.
* You can use a special command to find the cell code runtime in Jupyter Notebook. Find that command.
* Since the training of a gradient boosting model can take a long time, change only a few model parameters.
* If Jupyter Notebook stops working, delete the excessive variables by using the `del` operator:
* Copy codePYTHON


```
 del features_train

```



### **Data description**

The dataset is stored in file `/datasets/car_data.csv`.[ download dataset](https://practicum-content.s3.us-west-1.amazonaws.com/datasets/car_data.csv).

**Features**



* _DateCrawled_ — date profile was downloaded from the database
* _VehicleType_ — vehicle body type
* _RegistrationYear_ — vehicle registration year
* _Gearbox_ — gearbox type
* _Power_ — power (hp)
* _Model_ — vehicle model
* Mileage — mileage (measured in km due to dataset's regional specifics)
* _RegistrationMonth_ — vehicle registration month
* _FuelType_ — fuel type
* _Brand_ — vehicle brand
* _NotRepaired_ — vehicle repaired or not
* _DateCreated_ — date of profile creation
* _NumberOfPictures_ — number of vehicle pictures
* _PostalCode_ — postal code of profile owner (user)
* _LastSeen_ — date of the last activity of the user

**Target**

_Price_ — price (Euro)


# Conclusion

## Project Overview

Rusty Bargain, a used car sales service, aimed to develop an app to attract new customers by providing them with the market value of their cars. The project involved building a model to determine the value of cars using historical data on technical specifications, trim versions, and prices.

## Project Execution

1. **Data Exploration**: The dataset containing information such as vehicle type, registration year, gearbox type, power, model, mileage, registration month, fuel type, brand, repair status, and other features was downloaded and explored.

2. **Model Training**: Different models with various hyperparameters were trained, including linear regression for a sanity check, decision tree, random forest, LightGBM with hyperparameter tuning, and CatBoost. These models were trained to compare their performance in terms of prediction quality and speed.

3. **Model Evaluation**: The Root Mean Square Error (RMSE) metric was used to evaluate the models' prediction quality. The time required for training each model was also analyzed to assess the speed of prediction.

## Findings

An alternative approach to gradient boosting can enhance the efficiency of model training and yield superior RMSE scores compared to Linear Regression. Random Forest is not a viable option due to the extensive time required to identify optimal hyperparameters and subsequently train the model. In terms of both training speed and quality, LightGBM demonstrated the most impressive performance.

## Recommendations

1. **Model Selection**: Based on the findings, it is recommended to use LightGBM for model deployment due to its superior performance in terms of both prediction quality and training speed.

2. **Further Exploration**: Explore additional hyperparameter tuning techniques and model architectures to further improve prediction quality and speed.

3. **Data Enhancement**: Consider collecting additional data or refining existing features to enhance the accuracy of the model predictions.

## Future Improvements

1. **Advanced Modeling Techniques**: Experiment with advanced modeling techniques, such as ensemble learning or neural networks, to potentially improve prediction quality and speed.

2. **Automated Hyperparameter Tuning**: Implement automated hyperparameter tuning algorithms to streamline the model development process and optimize performance.

3. **Real-Time Data Updates**: Incorporate mechanisms for real-time data updates to ensure that the model reflects the latest market trends and fluctuations.

By implementing these recommendations and pursuing future improvements, Rusty Bargain can enhance its app's functionality and provide customers with accurate and efficient car valuation services.

### Model Performance Comparison


<table>
  <tr>
   <td>Model
   </td>
   <td>RMSE - the quality of the prediction
   </td>
   <td>the time required for training
   </td>
  </tr>
  <tr>
   <td>LightGBM parameter 1
   </td>
   <td>1652.48
   </td>
   <td>41.8 sec
   </td>
  </tr>
  <tr>
   <td>LightGBM parameter 2
   </td>
   <td>1649.50
   </td>
   <td>29 sec
   </td>
  </tr>
  <tr>
   <td>CatBoost
   </td>
   <td>1734.55
   </td>
   <td>2min 12s
   </td>
  </tr>
  <tr>
   <td>RandomForest Parameter 1
   </td>
   <td>2840.62
   </td>
   <td>6min 2s
   </td>
  </tr>
  <tr>
   <td>RandomForest Parameter 2
   </td>
   <td>3426.50
   </td>
   <td>36.8 s
   </td>
  </tr>
</table>
