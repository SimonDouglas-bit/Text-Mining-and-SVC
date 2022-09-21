# Text-Mining-and-SVC
A Support Vector Classifier to categorize Ham &amp; Spam messages.
This activity involves text mining on ‘SPAM text message 20170820 – Data’, a dataset available from Kaggle.
First step is to use pandas library to load the dataset in Jupyter
notebook after importing pandas library, some libraries from nltk, some visualization
libraries and other useful libraries to deal with text data. Follows data exploration to
understand the dataset, some manipulation to ease the process and visualization to further
understand the dataset. The dataset has only two features which are spam and ham. I
added another attribute ‘length’ to see if it provides any insights about the two major
attributes. Spam messages appears to be longer compared to ham messages.
Next step is to carry preprocessing on the dataset using nltk and focusing only on the
messages that are classified as spam. This involves converting all the spam text to lower
case just to make the case insignificant and then tokenizing all the texts with
word_tokenize() method, removing stopwords in the text using stopwords defined in
nltk.corpus, stemming the remaining texts, and removing the punctuations and single
character words because they convey less meaning.
