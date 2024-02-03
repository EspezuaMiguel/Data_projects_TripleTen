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
