<heading> A LightGBM based efficient Machine Learning model on Costa Rican Household Poverty Level Dataset.

Contributors - Abhinandan Mohanty, Mohammed Hadi Dadan, Jyotisman Rath
This is as a submission to BVEST Beat The Base Hackathon on 5th Nov 2020.
  
Background Info -
The dataset used here-in is available on Kaggle (https://www.kaggle.com/c/costa-rican-household-poverty-prediction/) as an old Machine Learning challenge. The primary objective is to use certain social and economic parameters provided to predict poverty on a household basis. The dataset is developed by IDB, the Inter-American Development Bank, with ain aim of establishing and making use of modern methods for properly identifying families at that need financial assitance or help.

Our approach to this ML problem was as follows -
1.	Understanding the problem and data descriptions
2.	Exploratory data analysis (EDA - cleaning of data)
3.	Selecting proper features/parameters (Feature Engineering)
4.	Model comparison and optimization
5.	Interpreting and presenting results

There are four data types associated with the variables in the data set:
1.	Boolean: Integer Boolean (0 or 1), Character Boolean (yes or no). Columns such as paredblolad, noelec, etc. <br>
2.	Float data type. For example, meaneduc, overcrowding, etc. <br>
3.	Integer data type. For example, age, rent, rooms, tamviv, etc. <br>
4.	Alpha-numeric. For example, Id, idhogar. <br>

Data Exploration and Data Cleaning
For an easy first step of data exploration, we can visualize the distribution of the labels for the training data (we are not given the testing labels).
Distribution of training labels.

Missing Values
A critical data cleaning operation for this data is handling missing values. To calculate the total and percent of missing values is simple in Pandas

Light Gradient Boosting Machine Implementation
This function implements training the gradient boosting machine with Stratified Kfold cross validation and early stopping to prevent overfitting to the training data (although this can still occur). The function performs training with cross validation and records the predictions in probability for each fold. To see how this works, we can return the predictions from each fold and then we'll return a submission to upload to the competition.



Model Optimization
Model optimization means searching for the model hyperparameters that yield the best performance — measured in cross-validation — for a given dataset.

Conclusions

It was indeed an interesting Machine Learning challenge. Provided the time constraints, the model seems to perform excellent, thanks to LightGBM. The notebook provided is the original code that inlcudes our work step-by-step. we think that other algorithms like XGBoost and Random Forest may help to improve overall accuracy but this is perfect for now. No doubt, such a challenge proves the efficacy of Machine Learning and AI as a tool in solving societal problems in reality.

