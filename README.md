# Part A: Text Mining
A Support Vector Classifier to categorize Ham &amp; Spam messages.
This activity involves text mining on ‘SPAM text message 20170820 – Data’, a dataset available from Kaggle.
First step is to use pandas library to load the dataset in Jupyter notebook after importing pandas library, some libraries from nltk, some visualization
libraries and other useful libraries to deal with text data. Follows data exploration to understand the dataset, some manipulation to ease the process and visualization to further understand the dataset. The dataset has only two features which are spam and ham. I added another attribute ‘length’ to see if it provides any insights about the two major attributes. Spam messages appears to be longer compared to ham messages.
Next step is to carry preprocessing on the dataset using nltk and focusing only on the messages that are classified as spam. This involves converting all the spam text to lower case just to make the case insignificant and then tokenizing all the texts with word_tokenize() method, removing stopwords in the text using stopwords defined in nltk.corpus, stemming the remaining texts, and removing the punctuations and single character words because they convey less meaning.
Last step is to plot a color pallette of some of the words that are found in spam messages as shown in the notebook.
# Part B: Support Vector Classifier
After carrying text mining on ‘SPAM text message 20170820 – Data’ Kaggle dataset, the
next step follows constructing a Support Vector Classifier, seems relevant because I am
dealing with a binary dataset. I imported some libraries from sklearn to handle supervised
learning with SVC. With all the preprocessed text from both attributes in the dataset, I
carry more preprocessing using TfidfVectorizer class to convert them to a matrix of TF-
IDF features and with fit_transform() method to perform fit and transform on the text
data. Then split the data into 70% for training set and 30% for testing set.
Next is to create an object for SVC class by specifying kernel as sigmoid to provide a 2-
layer perception model. Then constructed the best fit hyperplane on the training set with
fit() method and tested the prediction on testing set using predict() method.
The accuracy of this model is established using the accuracy_score() function of the
sklearn.metrics package to calculate the accuracy score for the tested prediction against
the true labels. A classification report is used to measure the quality of predictions from
the Support Vector Classifier. The output are the individual percentages of the model’s
precision, accuracy, recall, f1-score and support. These metrics are calculated from the
true positive, true negative, false positive, and false negative. The accuracy of this model
is found to be 98%.
The challenges associated with this model includes:
1. Choosing the right kernel is not easy. The wrong kernel results to poor performance of the model.
2. SVM/SVC perform poorly in imbalanced data. The hyperplane may be skewed to the minority class when imbalanced data is used for training the model. Datapoints at the decision boundary of the hyperplane have a higher chance of being classified as negative.
3. The model is not suitable for large datasets as the complexity of SVM algorithm in
training is highly dependent on the size of the dataset. The larger the dataset, the
more time used in training and using the model. If the dataset is too large, it may
become infeasible due to computational cost.
4. The hyperplane produced by SVM and kernels is hard to understand by human
users.v. SVM only works in a real-valued space. A categorical attribute has to be
converted from categorical values to numeric attributes.
## Jupyter Notebook
[text mining and supervised learning.zip](https://github.com/SimonDouglas-bit/Text-Mining-and-SVC/files/9615493/text.mining.and.supervised.learning.zip)

## Dataset
[SPAM text message 20170820 - Data.csv](https://github.com/SimonDouglas-bit/Text-Mining-and-SVC/files/9615497/SPAM.text.message.20170820.-.Data.csv)

