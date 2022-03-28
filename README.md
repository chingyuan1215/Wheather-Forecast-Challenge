# Wheather-Forecast-Challenge

Project Goal: Use daily weather observation samples for training, and  to predict whether it will rain the next day.

# Steps of Analysis
#First: Data Preprocessing
  1. Dealing with missing values:
     Used sort_values() to calcluate the amount of missing values in each attribute.I would deal with missing values by filling the average of each        numeric column and filling the most frequent values of each categorical column.
     
  2. Dealing with unbalance dataset
     Our goal in this project is to predict weather it will rain tomorrow or not (attribute 23). I found that the training set is a unbalance dataset, which means that only 3175 numbers of observation in attribute 23 is YES, the rest of 13918 numbers of observation is NO. I would use Random Under-Sampling method to deal with this problem.
  
  3. Encoding categorical values
      The observations in attribute 22 and attribute 23 are YES and NO, I would replace NO to 0 and YES to 1 in order to build our training model. As for the attribute present the wind direction (attribute 8, attribute 10, attribute 11), I would use get_dummies menthod in Pandas to encoding categorical values.

  4. Normalization


  5. Dealing with outlier


  
#Second: Build Model
  1. Bulid ANN model
  2. Train the model
  3. Predict the result
