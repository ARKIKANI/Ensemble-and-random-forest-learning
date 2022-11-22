# Ensemble-and-random-forest-learning

**Basic concept to understand the Ensemble and random forest**


# What is Ensemble learning?
Ensemble learning is one of the most powerful machine learning techniques that use the combined output of two or more models/weak learners and solve a particular computational intelligence problem. E.g., a Random Forest algorithm is an ensemble of various decision trees combined.


## Type of Ensemble technique
# 1) Voting

# 2) Bagging and pasting : 
Base model are same in bagging technique but dataset are subset(dataset can be with or without replacement) .
#Types of Bagging technique
**Pasting** is a type of bagging technique where you do row sampling like bagging but  without replacement. Almost this are same.
**Random Subspaces:** Here we do column sampling.
**random paches:** there we do both row and column sampling


**Bagging Tips**

- Bagging generally gives better results than Pasting
- Good results come around the 25% to 50% row sampling mark
- Random patches and subspaces should be used while dealing with high dimensional data
- To find the correct hyperparameter values we can do GridSearchCV/RandomSearchCV

# 3) Random forest: this is special bagging technique
# 4) Boosting 
# 5) Stacking
