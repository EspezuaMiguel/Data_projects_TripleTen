# **Project description**

The Sure Tomorrow insurance company wants to solve several tasks with the help of Machine Learning, and you are asked to evaluate that possibility.



* **Task 1**: Find customers who are similar to a given customer. This will help the company's agents with marketing.
* **Task 2**: Predict whether a new customer is likely to receive an insurance benefit. Can a prediction model do better than a dummy model?
* **Task 3**: Predict the number of insurance benefits a new customer is likely to receive using a linear regression model.
* **Task 4**: Protect clients' personal data without breaking the model from the previous task.

It's necessary to develop a data transformation algorithm that would make it hard to recover personal information if the data fell into the wrong hands. This is called _data masking_, or _data obfuscation_. But the data should be protected in such a way that the quality of machine learning models doesn't suffer. You don't need to pick the best model, just prove that the algorithm works correctly.

**Project Instructions**



1. Load the data.
2. Check that the data is free of issues — there is no missing data, extreme values, and so on.
3. Work on each task and answer the questions posed in the project template.
4. Draw conclusions based on your experience working on the project.

There is some precode in the project template, feel free to use it, some precode needs to be finished first. Also, there are two appendices in the project template with useful information.


### **Data Description**

The dataset is stored in file `/datasets/insurance_us.csv`.[ You can download the dataset here.](https://practicum-content.s3.us-west-1.amazonaws.com/datasets/insurance_us.csv)



* **Features**: insured person's gender, age, salary, and number of family members.
* **Target**: number of insurance benefits received by an insured person over the last five years.

## Conclusion

### Data Preparation

The dataset was loaded and thoroughly checked to ensure it was free of any issues such as missing data or extreme values.

### Task Execution

#### Task 1: Finding Similar Customers
An algorithm was developed to identify customers similar to a given customer, aiding the company's marketing efforts.

#### Task 2: Predicting Insurance Benefit Eligibility
A prediction model was constructed to determine whether a new customer is likely to receive an insurance benefit. The model's performance was compared against a dummy model to evaluate its effectiveness.

#### Task 3: Predicting Number of Insurance Benefits
Using a linear regression model, the number of insurance benefits a new customer is likely to receive was predicted.

#### Task 4: Protecting Personal Data
A data transformation algorithm, known as data masking or data obfuscation, was developed to protect clients' personal data while ensuring the quality of machine learning models remains intact.

### Experimental Results

Empirical examination revealed that data obfuscation did not significantly affect the performance of the linear regression model. Both Manhattan and Euclidean distributions were utilized for neighborhood search, with similar results observed for scaled and unscaled data. Additionally, the k-NN algorithm exhibited better performance with scaled data, particularly with three neighbors.

### Recommendations

1. **Continuous Evaluation**: Regularly assess the performance of the developed models to ensure they remain effective over time.
   
2. **Enhanced Data Protection**: Further research and development should focus on improving data masking techniques to provide robust protection for clients' personal information.

3. **Model Optimization**: Explore optimization techniques to enhance the performance of machine learning models, particularly in scenarios where data privacy is a priority.

4. **Collaborative Efforts**: Foster collaboration between data scientists, cybersecurity experts, and domain specialists to develop comprehensive solutions that address both predictive accuracy and data privacy concerns.

## Future Improvements

1. **Advanced Data Masking**: Investigate advanced data masking techniques such as differential privacy and homomorphic encryption to provide stronger protection for sensitive information.

2. **Ensemble Modeling**: Implement ensemble modeling approaches to combine the predictions of multiple models, potentially improving predictive accuracy while preserving data privacy.

3. **Dynamic Privacy Controls**: Develop dynamic privacy controls that adapt to changing data privacy requirements and regulatory frameworks, ensuring compliance and data security.

4. **Explainable AI**: Incorporate explainable AI techniques to provide insights into model predictions while maintaining confidentiality, enabling stakeholders to understand and trust the model's decisions.

By addressing these recommendations and pursuing future improvements, Sure Tomorrow can continue leveraging machine learning to enhance its business operations while safeguarding customer privacy and data security.
