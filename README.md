<b> Light GBM model-costarica
</br>

The Costa Rican Household Poverty Level Prediction challenge is a data science for good machine learning competition currently running on Kaggle. The objective is to use individual and household socio-economic indicators to predict poverty on a household basis. IDB, the Inter-American Development Bank, developed the problem and provided the data with the goal of improving upon traditional methods for identifying families at need of aid.
The general approach to a machine learning problem is:
1.	Understand the problem and data descriptions
2.	Data cleaning / exploratory data analysis
3.	Feature engineering / feature selection
4.	Model comparison
5.	Model optimization
6.	Interpretation of results
Data types of variables: There are four data types associated with the variables in the data set:
1.	Boolean: Integer Boolean (0 or 1), Character Boolean (yes or no). Columns such as paredblolad, noelec, etc.
2.	Float data type. For example, meaneduc, overcrowding, etc.
3.	Integer data type. For example, age, rent, rooms, tamviv, etc.
4.	Alpha-numeric. For example, Id, idhogar.
Data Exploration and Data Cleaning
For an easy first step of data exploration, we can visualize the distribution of the labels for the training data (we are not given the testing labels).
Distribution of training labels.
I’m using *statistical type *to mean what the data represents — for example a Boolean that can only be 1 or 0 — and *data type *to mean the actual way the values are stored in Python such as integers or floats. The statistical type informs how we handle the columns for feature engineering.
Missing Values
A critical data cleaning operation for this data is handling missing values. To calculate the total and percent of missing values is simple in Pandas
Light Gradient Boosting Machine Implementation
This functionimplements training the gradient boosting machine with Stratified Kfold cross validation and early stopping to prevent overfitting to the training data (although this can still occur). The function performs training with cross validation and records the predictions in probability for each fold. To see how this works, we can return the predictions from each fold and then we'll return a submission to upload to the competition.
Model Optimization
Model optimization means searching for the model hyperparameters that yield the best performance — measured in cross-validation — for a given dataset.

Conclusions
In this notebook, we went through a step-by-step implementation of an entire data science solution to a real-world problem. Machine learning is really just a series of steps, each simple by themselves, with the overall result often extremely powerful.
Our path was as follows:
1.	Understand the problem
2.	Exploratory Data Analysis
•	Deal with data issues
•	Fill in missing values
3.	Feature Engineering
•	Aggregate data
•	Feature selection in stages
4.	Model Selection
•	Try many different models to see which one is most promising
•	Feature selection can also come into play
5.	Model Optimization
•	Choose the best performing model and tune
6.	Implementing best model
7.	Investigate predictions
•	Identify model shortcomings
8.	Try new techniques
•	Experiment and learn!


An efficient classification model built on Costa Rica Housing Poverty data set.
