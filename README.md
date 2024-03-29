# Energy_Demand_Forecasting
Time Series Regression Prediction on Energy Demand of an Industrial Facility

Summary of Results:
A LSTM model obtained a Mean Squared Error of 9.106 on a test dataset of 196 rows (containing 96 forecasted times per row).
The Augmented Dickey Fuller test indicated that the boxcox transformed data had the most correlation between the USAGE_KWH values.
The language used was python version 3.6.4. Keras version 2.2.4 was used to apply LSTMs, while scikit-learn version 0.19.1 version statsmodels version 0.9.0 were used for classical algorithms and statistical tests.

It is recommended to use JupyterNotebooks to see the returned values from each cell. Google Colaboratory can be used to run the code on a GPU (useful for the LSTM model). 

Files:
Included is four files of code and a .sav file for a linear regression model prototype and a random forest regressor. To load the linear regression model and random forest regressor, the pickleshare library version 0.7.4 is needed. The LSTM model was not saved because of its enormous file size. A user running the LSTM.ipnyb code can save the model and use it.

The first set of code includes the data visualization & analyses, which uses numpy version 1.14.2, pandas version 0.22.0, and matplotlib version 2.2.2, along with various miscellaneous libraries.
The AD Fuller test was used to statistically validate the stationarity of the USAGE_KWH. The coint-johanson test was used to validate the stionarity for the entire, multivariate dataset.

The second set of code includes the experimentation with classical trend prediction algorithms. These all performed poorly. Because there are 4 versions of the data (original dataset and 3 transformed datasets), most algorithms were applied to each dataset (and the appropriate inverting was applied). Only on the VAR, VARMAX, Simple Exponential Smoothing, and Exponential Smoothing algorithms were only applied to the original dataset only (to reduce redundancy).

The third set of code includes the successful model (using a LSTM Deep Learning framework). 

The fourth set of code includes a successful model (a linear regression model with a MSE of 14.7). An .sav file is included where the weights are saved.
Also a random forest regressor was attempted, but the mean squared error was 20.07. An .sav file is included where the weights are saved.

Future steps include testing the dataset on more Linear, NonLinear, and Ensemble Machine Learning models (such as Ridge Regression, KNearest Neighbors, Support Vector Machines, and Gradient Boosting).
