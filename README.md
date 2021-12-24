# Time-Series-Forecasting

Learning to store information over long time intervals using recurrent backpropagation requires a very lengthy time, owing to insufficient, fading error backflow. To circumvent this, the researcher devised a Long Short-Term Memory (LSTM) network. Here in this code, I demonstrate how to use LSTMs to forecast stock open prices for a specific company.

This system is built on Miniconda and Python (3.7.11). Keras(2.2.4-tf) and TensorFlow(2.1.0) are employed as deep learning platforms.

Yahoo Finance is used to gather Google stock price data. The information covers the period from August 31, 2011, through August 30, 2021. There are a total of 2517 rows.

The opening price (Open) of a company is the initial transaction price per share when the market begins on a trading day. In univariate time series forecasting, there is only one value used. 

The Open variable dataset must then be turned into a time series data set for our time series. Assume the array is [t1 t2 t3 t4 t5 t6], and two-time step will be used as input. 
Then output will be t3 for the time step of t1 and t2. The output for t2 and t3 input will be t4. As a result, the time step sets are {(t1, t2), (t2, t3), (t3, t4), (t4, t5)}, while the output set are {t3, t4, t5, t6}. For converting our dataset in time series, create dataset method is used. Three LSTM layers and one dense layer is used to create model. ReLU is used as an activation function in the first and second LSTM layers. Mean squared error set as loss function and Adam is set as optimizer.
