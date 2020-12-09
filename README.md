# Dual stage attention based RNN
 The implementation is based on the paper [A Dual-Stage Attention-Based Recurrent Neural Network for Time Series Prediction](https://arxiv.org/abs/1704.02971).



 ### Model:
 
 
The paper here proposes a novel method of capturing both the long term dependancies as well as important hidden variables from the input data.

The neural network here consists of two parts: input attention mechanism and temporal attention mechanism. 

•	In input attention mechanism the network layers try to capture only the most important hidden variables at each time step before feeding that data into the encoder LSTM network. 

•	In temporal attention mechanism the relevant encoder hidden states that are extracted across all time steps are retrieved from the LSTM encoder and integrated with the hidden state of the LSTM decoder. The network layers then try to capture the important hidden variables from the encoder and decoder combined. 

### Environment:
Code has been developed using python 3.6, PyTorch library version:1.3

### Dataset details:
The dataset used as part of our implementation is a subset of NASDAQ 100 dataset. This dataset has stock prices and index prices for 81 major corporations. These prices are recorded for a total of 105 days starting from July 26, 2016 till December 22, 2016. There are 390 data points recorded for each day, except for November 25, where we have 210 data points and 180 data points for December 22. The missing values in our dataset have been imputed by linearly interpolated values.
