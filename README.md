# Ensemble-and-random-forest-learning

**Basic concept to understand the Ensemble and random forest**


# What is Ensemble learning?
Ensemble learning is one of the most powerful machine learning techniques that use the combined output of two or more models/weak learners and solve a particular computational intelligence problem. E.g., a Random Forest algorithm is an ensemble of various decision trees combined.


## Type of Ensemble technique
# 1) Voting :  
Voting and bagging are similar in that they decide on the final result by combining multiple algorithms, but are different in terms of data sampling method. The diagram below may be able to explain their differences effectively.

# 2) Bagging and pasting : 
Base model are same in bagging technique but dataset are subset(dataset can be with or without replacement).

#Types of Bagging technique

**Pasting** is a type of bagging technique where you do row sampling like bagging but  without replacement. Almost this are same.
**Random Subspaces:** Here we do column sampling.
**random paches:** there we do both row and column sampling


**Bagging Tips**

- Bagging generally gives better results than Pasting
- Good results come around the 25% to 50% row sampling mark
- Random patches and subspaces should be used while dealing with high dimensional data
- To find the correct hyperparameter values we can do GridSearchCV/RandomSearchCV

Diffrence between voting and bagging learning

![image](https://user-images.githubusercontent.com/110124468/203420388-43dd541b-6796-4b65-837b-3b0d1cf353bc.png)


# 3) Random forest: 
This is special bagging technique  but has collection of decision trees.

Why use Random Forest?
Below are some points that explain why we should use the Random Forest algorithm:

It takes less training time as compared to other algorithms.
It predicts output with high accuracy, even for the large dataset it runs efficiently.
It can also maintain accuracy when a large proportion of data is missing.

Why use Random Forest?

Below are some points that explain why we should use the Random Forest algorithm:

- It takes less training time as compared to other algorithms.
- It predicts output with high accuracy, even for the large dataset it runs efficiently.
- It can also maintain accuracy when a large proportion of data is missing.

![image](https://user-images.githubusercontent.com/110124468/203657715-1da84b82-bbba-4bfb-9e9d-b4f69b9f1c08.png)


Advantages of Random Forest
- Random Forest is capable of performing both Classification and Regression tasks.
- It is capable of handling large datasets with high dimensionality.
- It enhances the accuracy of the model and prevents the overfitting issue.



# Out of bag(OOB) Evaluation

New training sets for multiple decision trees in Random Forest are made using the concept of Bootstrapping, which is basically random sampling with replacement.

![image](https://user-images.githubusercontent.com/110124468/203660377-2c2a6d4a-7514-45e3-9a92-5d26ae64671d.png)

While making the samples, data points were chosen randomly and with replacement, and the data points which fail to be a part of that particular sample are known as OUT-OF-BAG points.

# Out-of-Bag Score (OOB_Score)

Where does OOB_Score come into the picture?? OOB_Score is a very powerful Validation Technique used especially for the Random Forest algorithm for least Variance results.

Note: While using the cross-validation technique, every validation set has already been seen or used in training by a few decision trees and hence there is a leakage of data, therefore more variance.
But, OOB_Score prevents leakage and gives a better model with low variance, so we use OOB_score for validating the model.


Let’s understand OOB_Score through an example:

Here, we have a training set with 5 rows and a classification target variable of whether the animals are domestic/pet?

![image](https://user-images.githubusercontent.com/110124468/203660803-1d1abe52-fea5-4b53-b10f-599a9c247da8.png)

Out of multiple decision trees built in the random forest, a bootstrapped sample for one particular decision tree, say DT_1 is shown below

Here, Rat and Cat data have been left out. And since, Rat and Cat are OOB for DT_1, we would predict the values for Rat and Cat using DT_1. (Note: Data of Rat and Cat hasn’t been seen by DT_1 while training the tree.)


![image](https://user-images.githubusercontent.com/110124468/203660846-9055b49a-f7e3-414c-bd11-5cb5971f7e7a.png)

Say 3rd, 7th, and 100th decision trees also had Rat as an OOB datapoint, which means “Rat” data wasn’t seen by any of them, before predicting the value for Rat.

So, we recorded all the predicted values for “Rat” from the trees DT_1, Dt_3, DT_7, and DT_100.

And saw that aggregated/majority prediction is the same as the actual value for “Rat”.
(To Note: None of the models had seen data before, and still predicted the values for a data point correctly)

![image](https://user-images.githubusercontent.com/110124468/203660961-427cfdf5-efce-4559-92b5-fcce96750ea9.png)

Similarly, every data point is passed for prediction to trees where it would be behaving as OOB and an aggregated prediction is recorded for each row.

Note: The OOB_score is computed as the number of correctly predicted rows from the out-of-bag sample.

OOB Error is the number of wrongly classifying the OOB Sample.

![image](https://user-images.githubusercontent.com/110124468/203661053-986352bf-509c-478f-9bc9-e74a7346e035.png)


 Advantages of using OOB_Score:
No leakage of data: Since the model is validated on the OOB Sample, which means data hasn’t been used while training the model in any way, so there isn’t any leakage of data and henceforth ensures a better predictive model.
Less Variance :  [More Variance ~ Overfitting due to more training score and less testing score]. Since OOB_Score ensures no leakage, so there is no over-fitting of the data and hence least variance.
Better Predictive Model: OOB_Score helps in the least variance and hence it makes a much better predictive model than a model using other validation techniques.
Less Computation: It requires less computation as it allows one to test the data as it is being trained.


 Disadvantages of using OOB_Error :
Time Consuming:  The method allows to test the data as it is being trained, but the overall process is a bit time-consuming as compared to other validation techniques.
Not good for Large Datasets: As the process can be a bit time-consuming in comparison with the other techniques, so if the data size is huge, it may take a lot more time while training the model.
Best for Small and medium-size datasets: Even if the process is time-consuming, but if the dataset is medium or small sized, OOB_Score should be preferred over other techniques for a much better predictive model.


End Notes !!
Random Forest can be a very powerful technique for predicting better values if we use the OOB_Score technique. Even if OOB_Score takes a bit more time but the predictions are worth the time consumed in training the random forest model with the OOB_Score parameter set as True.


# Feature Importance

Feature importance is a score between 0 and 100 assigned to each column (or feature), telling how powerful is that feature in predicting the target variable. Note that we also require that the sum of all features should be 100. 

In short ,Feature Selection


# 4) Boosting 

1- Week Learner : In the model the accuray of our model is less . we can say that near 50 %.
2) Decision stumps: this is actully a week learner like max_depth in DT is 1.
3) 1 and -1 , instead 1 or 0

Stagewise
1) Adaboost: ( Additive methods)

upsampling  increate the importance




























=
# 5) Stacking
