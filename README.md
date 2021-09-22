# NY-Stock-Exchange-Prediction
XGboost, LSTM, LR Models for NY Stock exchange prediction

# Author
Jiajin Chen

# Objecive

The primary goal of this study is to develop models for New York Stock Exchange price prediction, and obtain a best model with the lowest mean-square error. This study will use three methods to develop these models, namely Linear
Regression, XGBoost and LSTM. Establishing a reasonable stock price prediction model can grasp the rhythm of the stock market to a certain extent, and
provide a reference for investors in buying and selling transactions. Although
the stock price prediction based on machine deep learning has a significant effect on the stock market, it is actually necessary to consider more complex data
such as buying points, trading volume, historical prices, and K-lines. This also
requires a deep understanding of the stock financial market and mathematical
models. But to some extent, stock price prediction cannot completely predict
the market trend. This is because the market is jointly determined by all participants, which is also called game theory.

## Description

###  Previous work on data pre-processing techniques
Information leaking: Data pre-processing techniques cannot apply to the whole dataset, as it could lead to information leaking. As a result, the outcome after information leaking would outperform the actual outcome. Therefore, the dataset needs
to be splitted into train and test set first, normalization or standardization techniques could be implemented on data.

### XGBoost
Extreme Gradient Boosting (XGBoost) is an algorithm based on the Gradient
Boosting Decision Tree (GBDT) (Friedman, 2001).
The usual features pre-processing techniques used in XGBoost is standardization, standardScaler. That is determining the mean and standard deviation of each feature, subtracting the mean from each feature and dividing the values
by corresponding standard deviation.However, in this study, the preprocessing technique chosen is the minmaxscaler.The scaler would be implemented on all data of open price, close price, high
price, low price and volume.

### LSTM
The stock price has great volatility and randomness, thus, the closing price cannot be derived simply according to a functional relationship(Wang, JianZhou, et al., 2011). Because of its strong learning ability for hidden information in data, neural network is widely used in various fields, especially the field of
stock price prediction. The Recurrent Neural Network (RNN) solves the difficult problem of traditional neural network in processing time series by adding connections between hidden layers. However, during the processing of a long
time sequence, the gradient of the loss function of RNN will exponentially vanish or explode over time, resulting in long training time for the model and low accuracy (Sherstinsky, 2020).
The Long Short-Term Memory (LSTM) network is improved on the basis of RNN, which solves the problem of gradient vanishing and explosion, and realizes the function of maintaining memory in long-sequence training by adding
memory units (Zaremba, Wojciech, et al., 2014). The emergence of LSTM makes time series forecasting more efficient. Kim, Ha Young, and Chang Hyun Won
(2018) as well as Chen, Shun, and Lei Ge (2019) have already applied LSTM to stock price predictions.
This study on LSTM mainly uses the data of the previous 50 days to predict the data of the next day, and adds a Dropout layer to prevent data overfitting.




### Methods
SVM machine learning algorithm was chosen to train and predicted the data. This is a good classification model by applying hyperplanes to the dataset for my dataset with a high accuracy of 72%. 


## Getting Started

### Programming language
* Python 3
* Version: 3

### Dependencies: Libraries to use 

* pandas
* math
* matplotlib.pyplo
* keras version 2.4.3
* tensorflow version 2.3.1
* xgboost version 1.2.1
* sklearn.preprocessing
* MinMaxScaler


### Installing

* To run algorithm1 XGBoost.ipynb, users need to install
pip and xgboost in Anaconda Prompt using the following code:

```bash
python −m pip install -U pip
pip install xgboost
```


## Author

Jiajin Chen;


