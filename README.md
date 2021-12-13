# Credit_Risk_Analysis

Using the dataset from LendingClub, we will be creating multiple dataset & analyzing them to predict credit risks.
we'll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, we will use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once done, evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.


# Results

## naive random oversampling algorithm

The algorithm resulted in a balanced accuracy score of 0.64. 
Precision score = 1.0, for low risk and extremely low for predicting high risk.
Recall scores were 0.66, and 0.62 for high/low

![naive random](https://user-images.githubusercontent.com/89154507/145740025-d3456158-4880-435e-bbbd-4af2fea5abc7.jpg)


## SMOTE algorithm

The algorithm resulted in balanced score of 0.65.
Precision score was also 1.0, same with above.
Recall scores were 0.61 and 0.69 for high/low

![smote](https://user-images.githubusercontent.com/89154507/145740330-2cb09786-d3cd-4529-913a-8b6c7f414fb1.jpg)


## Cluster Centroids 

The algorithm has balanced accuracy score of 0.55.
The precision score for high/low was also same as the previous two algorithms.
The recall scores were 0.67 and 0.42 for high/low.

![clustr](https://user-images.githubusercontent.com/89154507/145740628-1e44cd30-a352-4e54-80ba-fcac0553aacf.jpg)

## SMOTEENN algorithm

The balance was 0.62.
Precision score was also same as above, 1.0 for high and low.
The recalls were 0.64 and 0.60 for high/low

![SMOTTEE](https://user-images.githubusercontent.com/89154507/145740949-2d2ece49-a6c2-4ce5-8688-a8059d301e31.jpg)



## Balanced Random Forest Classifier

The balanced accuracy score was 0.79.
Precision score was 1.0 for low risk, but the high risk prediction had extremely low value of 0.09.
The recall scores were 0.70 and 0.84 for high/low risk stats. 

![Balanced Random Forest Classifier](https://user-images.githubusercontent.com/89154507/145741147-929a4505-57f7-49a8-937e-fa027e9b6635.jpg)


## Easy Ensemble Classifier

The Easy Ensemble Classifier resulted in a resulted in a balanced accuracy score of 0.93. 
Precision scores were the same as forest classifier.
The recall scores were 0.92 / 0.94 for high/low risk stats.
![Easy Ensemble Classifier](https://user-images.githubusercontent.com/89154507/145741254-8b008176-5bd4-4ceb-9f1e-fe6230864a42.jpg)


# Summary

The Cluster Centroids algorithm yielded the lowest accuracy score of 0.55. The precision score for predicting the high risk was low for all models except for the two resampling algorithms, which had extremely low high (0.09) risk. The Easy Ensemble Classifier had the highest recall rate of 0.92 / 0.94. 
The most reasonable selection would be to use the Easy Ensemble Classifier which has the highest balanced score of 0.93. When the company use the Easy Ensemble Classifier, they should be aware that the high risk stat is extremely low (0.09) which implicates the high risk classification is not very reliable. 

