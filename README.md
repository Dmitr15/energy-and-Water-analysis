# energy-and-Water-analysis
Dataset analysis using python, matplotlib, seaborn and sklearn.

Dataset: Energy_and_Water_Data_Disclosure_for_Local_Law_84_2017__Data_for_Calendar_Year_2016_.csv

Problem solved:

Predict the Energy Star Score of a building and understand which features have the strongest impact on it.

Data cleaning:

Replace "Not Available" with np.nan.
Change all columns to the correct type.

Get rid of missing data and outliers.

Plot graphs of variable dependencies, find dependencies.

Run all numeric types through the logarithm function.

Feature selection:

Keep all columns with a correlation coefficient of 0.6 or higher.

Delete all columns with the value na

Result evaluation:

Select the metric: mean absolute error (MAE)

To conduct training, you need to split the sample into training and testing

calculation formula mae = mean(modulus(y real - y predicted))

Try to train the model on models from sklearn and see mae for:

LinearRegression

SVR

RandomForestRegressor

GradientBoostingRegressor

KNeighborsRegressor
