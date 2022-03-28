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
     Since the values represented by different fields of the training data will affect model training, such as temperature, rainfall, average atmospheric pressure and relative humidity cloumns. I would nomalized these values during data preprocessing to avoid a single attribute affects the result.

  5. Dealing with outlier
    This step will modify the outliers in the dataset, I set the upper bound of the data to 75% and the lower bound to 25%. Therefore, if the value is not between 25%~75%, the data with be replaced with its upper or lower limits.

  
#Second: Build Model
  1. Bulid ANN model
  2. Train the model
  3. Predict the result
