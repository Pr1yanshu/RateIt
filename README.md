# RateIt
A simple Recommender system that predicts the ratings of the movies that will be given by users(a brief implementation of Stacked Auto Encoders-SAE)
## Architecture
The architecture of the model is simply of a Stacked auto encoder which is built using pytorch framework.
## Dataset
The datasets i have provided are in two folders.The first one named 'ml-1m' is solely for the visualisation of the structure of data that i have used.I have used the
second one for training purposes and restructured it such that each row correspond to user(observations) and columns correspond to the ratings(observed values) given 
by the users for corresponding movies(The ith row and jth column element represent the ratings given by the ith person to the jth movie).U can import
your own data set but make sure its in proper format.There are some ratings(elements) that are zeroes in the datset which corresponds to the movies
that users haven't watched amd these are the we can predict.so make sure the values to be predicted are zeroes initially.
## Training
Run the ae.py file and it will train the model.
## Predicting the ratings
Save the object instance of the model class on which training was done.To predict the values,simply pass the input tensor to this object instance.It will return
the predicted values even for those which the users havent watched yet!
