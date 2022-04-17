The goal of this project was to see if I can predict the playstyle of tennis players (aggressive, defensive, etc..) based on their match statistics and physical attributes (height, weight). For more information on this project, see the PDF document in this folder which gives background and explains results.

Code:

Data Wrangling and Imputation:
1) Cleaned and organized multiple dataframes of player statistics in a per match format into a single dataframe containing average match statistics for        each player
2) Identified multiple highly correlated columns so chose LASSO regression for feature selection and to impute some data missing in a column (this column was a percentage, so see the paper for more information)
3) Used LASSO regression for feature selection and to impute missing data from a feature

Unsupervised Learning:
1) Used PCA to reduce the dataset from 14 features to 5 features while preserving roughly 80% of the variance in the features
2) Performed hierarchical clustering using various linkage methods and projected groupings on the first two principal components
3) Checked within groups to understand the extent to which the data contains the structure necessary for the project

Supervised Learning:
1) Fit a variety of models to predict player style based off of match statistics and physical characteristics (separately)
  a) SVM//
  b) Random Forest
  c) Neural Network (very small becuase I only had around 300 observations)
  d) KNN
3) In the case of predicting playstyle from physical characteristics, there wasn't enough data for models to perform well enough. To identify whether the models would perform better under a more straightforward setting that requires less data, I simplified the problem to binary classification (see paper for more information) and reran models including a logistic regression model
