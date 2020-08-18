# LSTM-based-Indian-stock-Market-prediction
I was keen to observe time series prediction models and tried my hands on with LSTM based stock market predicition.
Used Pandas datareader for fetching stock prices.
This is the most basic form of stock market prediction. 
The more the data Involved the better the results.
I have taken this for Infosys stock from 2012 to 2020

for any other stock, search yahoo finance for ticker name of the stock replace it in the code and train the model for your choice of stock

It has different sections in the process
1. Importing libraries and installation
2. Data frame definition(date, columns, shape)
3. Different metric plotting(rolling mean, closing, 7 day plot)
4. Data preprocessing (Noralization, scaling)
5. Division into 60 time steps for 1 prediction  (1-60 predict 61, 2-61 predict 62 and so on for entire data set to train your model)
6. Model definition using scikit learn. (Optimizer- Adam)
7. Compile the model and run the epochs for training.
8. Prepare test set for dates that you have the data for (you can do it by dividing training set into 80-20 but i prefer to do it for 2 weeks of latest data,
                                                        (so keep changing the dates for 2 weeks before and after to make ur model learn the basic and the most recent)
9. Fetch the predicted stock price and get a list of future values.
10. plot the graph for visualisation of predicted vs real(its erroneous for 1st day with huge value but that is to be ignored, as it overlaps with datas to make ungapped graph)
11. measure Root mean square error(loss), the closer it is to 0, the better your model behaves.

![result of prediction](snapshot.jfif)


NOTE: I dont suggest trading or using this model to work in the stock market,as it does not take into account most of the other features. The model just accounts on the basis of Close price, which is not the only parameter that should be involved(Close price is the stable price each day, as the opening price for the following day can be greater than previous day's closing which would give gaps into our data if accounted simultaneously). Accuracies with 7-13 RMSE are pretty common with this model. There are many more fututre studies that I will be coding or updating this with more principles and parameters in the Portfolio domain. Any people who want to add any functionality or suggest any cahnges are most welcome. Any usage of this coding repository will be appreciated if you can tag me in the place you want to publish this. Also, i have gone through a lot of tutorials and this is a compilation of all of them that I have read.

Tag me here or you can just put an appreciation in DM-LinkedIn Url:
www.linkedin.com/in/adityaabothra
