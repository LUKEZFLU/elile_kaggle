# elile_kaggle_part1

This repo serves for Web team's Kaggle Challenge Part 1

## Team:

- Zefan Lu
- Reem Abdulhameed
- Annusa Shanneb
- Shobhit Verma
- Weichen Zhang

## Conclusions:

- Part 1

- Regarding panel maintenance, one potential solution is to monitor the difference between the daily yield (within a specific time interval) and the radiation levels. We can establish a default threshold; if the difference exceeds this threshold, it indicates that the panel may require cleaning or possibly repairs. (check q2_panel_cleaning.ipynb)

- Based on their extremely high R2 values (about 99%), all three models demonstrate excellent data fitting. The percentage of the dependent variable's volatility that can be predicted based on the independent variables is shown by this score. The Random Forest Model has the lowest MSE value. Regarding the prediction of the future data, the Random Forest Model is a better choice.

- Part 2

- Random breaks in the time series data that are designed to simulte missing values proved to be detrimental to the prediction performance. This is because some of these values (included in the test and validation set) were local minimums or maximums i.e. outliers. Absence of these values in the training data meant that the model could not pick up the patterns in solar energy output in some cases.

- The state-of-the-art Torch Vision Transformer significantly improved MSE by 2 orders of magnitude over the previous best model (10^5 to 10^3).
