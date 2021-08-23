# Credit_Risk_Analysis

# Overview of the analysis:
Credit risk is very tough to predict. In this project, we want to take a look at how all the factors in our loan_stats csv help predict whether someone is low or high-risk status. One method that data scientists use for this type of issue is creating a model and then evaluating and training the models they create. In this specific project, we are using imbalanced-learn and scikit-learn libraries to build models and evaluate them using a resampling method. In the first couple of models, I oversampled the data using randomoversampler and smote algorithms and undersample the data with the clustercentroid algorithm. In the remaining models, I used a combination approach to over and undersample the data using smoteenn. Finally, I compared two machine learning models that minimize bias, balancedrandomforestclassifier, and easyensembleclassifier.

# Results:
Naive Random Oversampling results: Our accuracy score test is 67.7%, the precision for the high_risk has a very low positivity at 1% and the recall is 61% naive
![image](https://user-images.githubusercontent.com/82552594/130383879-8ce04cd3-c681-4e71-b1e5-382f790973db.png)

SMOTE oversampling results: the accuracy score is 66.3%, the precision for the high_risk loans has a low positivity again at 1% and recall is 66% overall smote
![image](https://user-images.githubusercontent.com/82552594/130384386-5b3977c7-6af8-4a85-90f0-a8869c91af3f.png)

Undersampling results: balanced accuracy score is 66.2% overall, the precision is at 99% and the recall is 41% undersampling
![image](https://user-images.githubusercontent.com/82552594/130384664-768fcffa-6759-4c5c-a86e-1ab0d2fe941e.png)

Combination(over and undersampling) results: balanced accuracy score is 54.7% the precision is 99% and the recall is 57% overall combination

Balanced Random Forest Classifier results: the accuracy score is 77.2% the precision is 99% and the recall is 88% random-forest

Easy Ensemble AdaBoost Classifier results: the accuracy score is 91.7% the precision is 99% and the recall is 94% ensemble

## Summary:
In the first four models, we undersampled, oversampled, and did a combination of both to try and determine which model is best at predicting which loans are the highest risk. In the next two models, we resampled the data using ensemble classifiers to try and predict which loans are high or low risk. In our first four models, our accuracy score is not as high as the ensemble classifiers and the recall in the oversampling/undersampling/mixed models is low as well. Typically in your models, you want a good balance of recall and precision which is why I recommend the ensemble classifiers over the first four models. It appears that the Easy Ensemble had the best balance of all the models because of its high accuracy score and a good balance of precision and recall scores.







