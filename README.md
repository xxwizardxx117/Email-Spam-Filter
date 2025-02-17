# Coders Cave - DataScience (Project 1)

Here we made a email spam filter using ***logistic regression***. Data set used is from [Kaggle](https://www.kaggle.com/). We have only used ***email.csv*** file to do spam filtering. training and testing scores have been used to estimate the correctness of the results.
<u><h3><b> Pipeline</h3></b></u>

1. Imported `numpy`, `pandas` and various parts of `sk-learn` to use `logistic regression` and `metrics` for evaluation.

2. Loaded the email dataset into a pandas DataFrame.

3. In the data set we discover that **category** Column is a string value. So we used `One-Hot-Encoding` to convert the values into binary which model understands better than string values. Similarly we see **Message** . column that contains email-text has `stop-words` and is in string format. So here we convert this text data to numerical data using a vectorizer (either `CountVectorizer` or `TfidfVectorizer`) where stop-words parameter is set to `english` language and `lowercase` option is set to `True`.

4. Now as are data is in a desired format we split the dataset into training and testing sets to evaluate the model's performance. We do this using `test_train_split()` function provided by Sk-learn.

5. Now we make a `Logistic Regression Model` and train this using the train data using `fit()` function. Next after training we use the test data using `predict()`function to generate predictions. Results of both of these processes are stored in some variable.

6. Finally using `metrics` from sk learn actual predictions are compared with training predictions and `Training Accuracy` is generated. Similarly we do it for test data where `Predicted Values` are compare with test data actual prediction.

Result : The accuracy of the model on the training data was `` and on testing data it was ``.

<BR>
<BR>
<BR>

# Extended Extra Implementation/Learning

This code further has been expanded to learning of working of **perceptron**. Instead of using logistic regression we try to use a perceptron on same train test data to predict whether mail is ham or spam. 

We have made 2 models of perceptron :

1. This is a simple perceptron without any loss optimization.
2. This is a perceptron which uses `L1`/`L2` regularization for loss optimization.

Finally we also have tried to make the function where user can enter a mail and model will predict whether its ham or spam.
