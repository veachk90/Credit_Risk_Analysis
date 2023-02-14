# Credit_Risk_Analysis

#### Overview
The goal of this analysis is to compare a variety of machine-learning algorithms to determine which produces the best model for predicting default risk in loan applications. That is, we want to build a model that can accurately predict whether a candidate will default on a loan based on the information provided in the application. In this case, we are provided with a set of labeled data from previous applications which we can use to train the model in what is known as supervised learning. 

#### Results
By far, the Easy Ensemble Classifier provided the best results. This is indicated by the high f1 score in conjunction with the highest accuracy of the inspected models. Easy Ensemble Classifier works by dividing the data into subsets such that the proportion of both classes of data is equal. These subsets are then used to train individual classifiers, one for each feature. In a boosted model, the results of a given classifier are passed to the next in the sequence until a final output is produced. This particular method is particularly effective in datasets wiht heavy imbalances, which is the case in this instance.


Easy Ensemble Classifier: balanced accuracy = 0.8733, precision = 0.99, recall = 0.90
![Easy Ensemble Classifier](https://github.com/veachk90/Credit_Risk_Analysis/blob/main/Screenshot%20(272).png)

Random Forest Classifier: balanced accuracy = 0.5049, precision = 0.99, recall = 0.99
![Random Forest Classifier](https://github.com/veachk90/Credit_Risk_Analysis/blob/main/Screenshot%20(273).png)

SMOTEENN: balanced accuracy = 0.6438, precision = 0.99, recall = 0.58
![SMOTEENN](https://github.com/veachk90/Credit_Risk_Analysis/blob/main/Screenshot%20(277).png)

Cluster Centroids: balanced accuracy = 0.5443, precision = 0.99, recall = 0.58
![Cluster Centroids](https://github.com/veachk90/Credit_Risk_Analysis/blob/main/Screenshot%20(276).png)

SMOTE: balanced accuracy = 0.6640, precision = 0.99, recall = 0.69
![SMOTE](https://github.com/veachk90/Credit_Risk_Analysis/blob/main/Screenshot%20(275).png)

Naive Random Oversampling: balanced accuracy = 0.6560, precision = 0.99, recall = 0.62
![Naive Random Oversampling](https://github.com/veachk90/Credit_Risk_Analysis/blob/main/Screenshot%20(274).png)

#### Summary
If one of the provided models had to be used to make a decision, the Easy Ensemble Classifier would be the best choice for the given data. None of the other models come close in terms of accuracy, and it demonstrates high average precision and recall. However, it should be noted that the precision when making predictions on high-risk applications is .05, which is terribly low. That is, in order to accurately predict the high-risk applications, it will also classify a relatively high number of low-risk applications as being at high risk of default. This could be costly in terms of requiring additional reviews for declined loan applications.

