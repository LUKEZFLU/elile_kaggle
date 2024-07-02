# Toy Project Submission for Web Dev Team

This repo serves for Web team's submissions for Part 1 and Part 2 of the Kaggle project.

## Team:

- Zefan Lu
- Reem Abdulhameed
- Annusa Shanneb
- Shobhit Verma
- Weichen Zhang

## Conclusions:

## Part 1

- Regarding panel maintenance, one potential solution is to monitor the difference between the daily yield (within a specific time interval) and the radiation levels. We can establish a default threshold; if the difference exceeds this threshold, it indicates that the panel may require cleaning or possibly repairs. (check q2_panel_cleaning.ipynb)

- Based on their extremely high R2 values (about 99%), all three models demonstrate excellent data fitting. The percentage of the dependent variable's volatility that can be predicted based on the independent variables is shown by this score. The Random Forest Model has the lowest MSE value. Regarding the prediction of the future data, the Random Forest Model is a better choice. (linearModelTest.ipynb, DecisionTreeRegressor.ipynb, and randomForest.ipynb)

## Part 2

- The existing RNN code was written in Keras and outdated. Several changes were made to ensure the code runs as expected:

  - Changing the outdated optimizer Adaboost to Adamax
  - Correcting the minimum error value for Grid Search
  - Removing the outdated AdaBoost model in Keras
  - Installing the scikeras module for KerasClassifier

- Random breaks in the time series data that are designed to simulate missing values proved to be detrimental to the prediction performance. This is because some of these values (included in the test and validation set) were local minimums or maximums i.e. outliers. Absence of these values in the training data meant that the model could not pick up the patterns in solar energy output in some cases.

- This issue can be rectified by merging the three datasets and splitting the new dataset into train, test and split sets to retain the temporal sequences.

- The state-of-the-art Temporal Fusion Transformer significantly improved MSE by 2 orders of magnitude over the previous best model (10^5 to 10^3).
