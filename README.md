# module_2_project

Using the kings county housing data set, i completed a data analysis in order to make predictions about housing price. Initially i started off by looking through the data set, and completed a thorough clean, removing errors in the data and dealing with nan values. This initial clean brought down our housing entries from 21597 to 21419.

Following that i completed a train/test split, in order to avoid overfitting. I used the train data set to train and fit the model, then once the model was finalized, a model was ran on the test data set to check the preformance of the model.

Then i ran a correlation heatmap in order to see what variables had a good impact and correlation with the target variable, price. From the heatmap, the highest correlating variables with price was sqft_living, and others include grade,bathrooms, bedrooms and waterfront.

I formed the inital model using all the possible predictor variables, and recieved an r2 value of 0.645. We recieved multiple negative coefficients indicating that those predictor variables have a negative effect on the price, by bringing it down. So therefore, i firstly removed id, as it was not statistical useful to predict the price. In addition to that other variables were also removed due to multicollinearity.

So therefore using the top 5 correlated variables with price that i found from the correlation heatmap, i then formed an improved model. This model gave me an r2 of 0.584, which is moderately week. In this model we also recieved p-values of greater than 0.05 for the coefficients of condition and cond_2, and as a result of this they were removed as they were not statistically significant. I also ran a variance inflation factor test to multicollinearity with features, VIFs over 10 indicate multicollinearity, i recieved VIFs of over 10 with condition and all the predictors that were dummy variables of condition. In addition to this i also checked the heatmap again to further check for multicollinearity, and according to the results floors was collinear to sqft_living, and in addition to that bathrooms was also collinear to sqft_living. As a result of that due to their collienear relationships to sqft_living those variables were all removed.

After removing all of the unnessescary features, my predictor variables were narrowed down to sqft_living, grade and waterfront. A r2 0.570 which is slighly less than the previous results of the previous model. Our final test model gave an r2 of 0.575 which is a slight improvement. Although the r2 squared values recieved was moderately weak, this possible could be improved with access to other data such as when the house was sold, location and how far it is from certain locations.

Questions:

does grade have an effect on the housing price?
is there multicollinearity between the features?
what are the main factors that influence the price?
how does sqft_living, grade, and waterfront impact price?
how can the final model be improved further?