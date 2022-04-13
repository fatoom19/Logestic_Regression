# Logistic Regression Model of Wine Quality Dataset

• About the model:
Logistic model in this assignment is to predict the quality of wine whether it’s good or bad. The
relationship between independent variables 'fixed acidity', 'volatile acidity', 'citric acid', 'residual sugar',
'chlorides', 'free sulfur dioxide', 'total sulfur dioxide', 'density', 'pH', 'sulphates', and 'alcohol', and the
dependent variable quality is that we use independent features to predict the quality of the wine
(dependent variable).

• Dataset:
The data is about wine quality and features that affect wine quality. Dataset has 1599 rows × 12 columns.
The source of the data is Kaggle.

• Data pre-processing
First step is cleaning and exploring dataset. Dataset has no null values, but there are duplicated
values. I dropped duplicates. After cleaning the dataset, I started exploring and visualizing the
dataset. The type of data is numeric, so I don’t need to transform them or using one hot vector.
Figure 1 shows part of code where I was trying to figure out which features have best correlation
with wine quality. As a result, alcohol and sulphates has best corralation more than others .

• Splitting the data:
Before starting to build the model, we can see that there are 6 types of quality. The quality
column represents a preference order, so I can split it into good and bad to help the model do
better performance. The quality three represents the worst quality and the quality 8 represent the
best quality. I split them into two values which is good quality and bad quality. The good quality
equal 1 and the bad quality equal 0. After that, I split the data into training dataset 80% and
testing dataset 20%.

• Applying the model:
I built the model using LogisticRegression(), and I trained it using the training dataset which is
80% of the data. Then I tested the model with the testing dataset which is the rest 20% of the
data. I created a data frame that has the actual value and the predictive values that I got from
testing the model in order to compare them. It looks good, but we can't make sure until
we evaluate the model.


• Prediction results and test scores:
I have started with the accuracy to evaluate the model, and I got 75% accuracy which is good.
However, accuracy alone is not enough, so I found the confusion matrix. The confusion matrix
results not bad. Then I found precision. High precision relates to the low false positive rate. Precision:
0.74 which is pretty good. Recall which relates to a low false negative rate equals 0.77 that is also
considered as good score.

• Metrics:
The confusion matrix results shows that the true negative equal 98, true positive 106, false positive 37, and
false negative 31.

• Conclusion:
After removing the duplicated values from the dataset and exploring data, I found that there are 6
quality degrees of wine. I classified them to bad and good. Then I split the dataset into 80%
training and 20% testing. Then I built the model to predict the target (“the quality of the wine”).
The results of evaluation the model shows that the model is working well to predict the quality of
the wine. Accuracy equals 0.75, precision equals 0.74, and recall equal 0.77. I also found the
confusion matrix that shows 98 true negative, 106 true positive, 37 false positive, and 31 false negative.
