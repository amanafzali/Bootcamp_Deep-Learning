# Deep-Learning

![picture](https://github.com/amanafzali/Bootcamp_Deep-Learning/blob/main/Pictures/Deep-Learning-blog.png?raw=true)


In this assignment, I used deep learning recurrent neural networks to model bitcoin closing prices. One model will use the FNG indicators to predict the closing price while the second model will use a window of closing prices to predict the nth closing price.

The following steps were performed:

1. Prepare the data for training and testing
2. Build and train custom LSTM RNNs
3. Evaluate the performance of each model

# Prepare the data for training and testing

For the Fear and Greed model, I used the FNG values to try and predict the closing price.
For the closing price model, I used previous closing prices to try and predict the next closing price.
For each model used 70% of the data for training and 30% of the data for testing.
Applied a MinMaxScaler to the X and y values to scale the data for the model.
Finally, reshape the X_train and X_test values to fit the model's requirement of samples, time steps, and features. (example: X_train = X_train.reshape((X_train.shape[0], X_train.shape[1], 1)))

# Build and train custom LSTM RNNs

In each Jupyter Notebook, created the same custom LSTM RNN architecture. In one notebook, I fit the data using the FNG values. In the second notebook, I fit the data using only closing prices.
Used the same parameters and training steps for each model. This is necessary to compare each model accurately.

# Evaluate the performance of each model

Finally, used the testing data to evaluate each model and compare the performance.

    Which model has a lower loss?
    A: LSTM RNN Closing price has lower Loss.
    Which model tracks the actual values better over time?
    A: Both models tracks almost the same but RNN Closing price does slightly better.
    Which window size works best for the model?
    A: Window size 10 works better.