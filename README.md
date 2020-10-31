# Hello-World

Hi Everyone, 

I'm Anthony, 

With the rise of digital payments increasing everyday, we are on our way to a cashless society. In 2016, there were 482.6B credit card transactions. This however has created the issue of credit card fraud which has been on the rise. Credit card fraud losses in 2018 reached $27.85B and are projected to rise to $35.7B and $40.6B in the next 5 and 10 years respectively.

In order to detect and combat fraudulent credit card transactions, so that customers are not charged for items that they did not purchase, I'll be presenting various Credit Card Fraud Detection Models that include a baseline logistic regression,as well as a random forest, and a deep neural networks through Keras. 

The dataset is a September 2013 dataset of European cardholders. The data consists of 284807 rows and has 30 features. Our dataset is highly imbalanced, as we can see only 492 are actually fraudulent which represents 0.172% of the transactions. 28 of the features have already been transformed through PCA. The other features ‘Time’ and ‘Amount’ have not been transformed through PCA. Time variable indicates the amount of time in seconds that has occurred from each transaction to the first transaction and Amount variable indicates the transaction amount. ‘Class’ is the outcome and indicates 1 for fraud and 0 for not fraud.

The first step is to clean the data and then use PCA to reduce the dimensions of the dataset down to 24 features. Because the data is highly unbalanced, our model will show a high accuracy but that doesn't necessarily mean that our model is truly highly accurate. In order to solve this problem, we must reduce the sample numbers to 1000 non fraudulent cases so we are able to get a more balanced dataset. 

The Logistic Regression model gave a training accuracy of 0.9588 and a testing accuracy of 0.9709. Because of our imbalanced dataset we could not really rely on accuracy as a good measure in this case. I created a precision recall curve and calculated the f1 score and then did an ROC curve and got the AUC.

Deep Neural Network model using Tensorflow to identify the accuarcy of the model. Split the data into a training and testing set and normalize the data, as there are 30 variables in the table with different numeric columns. The goal of normalizatioin is to scale without distorting difference in the ranges of values. As previously mentioned, this dataset is a highly imbalanced dataset. We can see that there are only 492 fraudulent cases and 284807 non fraudulent cases. If we create a model using this dataset, our model will basically learn nothing. Therefore, we need to create a model with less no fraudulent cases than what we actually have and test it with our model. The model was built with hidden layers of 200, 120, and 55 and I used L1 regularization. 

Random Forest is a ml algorithm that uses supervised learning and can be used for classification and regression tasks. It gave a 96% accuracy rate. 

From the 3 models that we built: the logistic regression actually performed the best with an accuracy of 97%, vs a 93% in the DNN, and 96% in random forest model. DNN could have performed better if the data set was way bigger and introducing more feature engineering could work perfectly. The reason why we included the F1 scores below is because a high accuracy level itself does not determine the overall best performance of the model thus, we also need to look at the f1 scores.
