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






# 3) Random forest: this is special bagging technique
# 4) Boosting 
# 5) Stacking
