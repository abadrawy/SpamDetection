# Spam Email Detection

In this project, the aim is to build classifers,to predict whether a new email is ham or spam, by learning from previously seen emails.


# Dataset
The dataset is compromised of both spam and ham emails (ham is the terminology used in literature for non-spam emails)
The dataset used is [Ling-Spam](http://csmining.org/ling-spam-datasets.html/), which is one of the standards for spam detection.

# Preprocessing
Read all the emails in the ten folders inside folder “bare”.

Save the labels (spam/not spam, or 0/1) of each email to a list, depending on if “spm” is in the title or not.

Split the emails and labels into 80% training and 20% testing.

Fit and transform the training emails and transform the testing emails using a CountVectorizer

# Scikit-Learn Classifiers
3 classifiers are configured and their results will be compared.

a) Multinomial Naive Bayes

b) K Neighbors Classifier

c) Random Forest Classifier

# Feature Extraction
Rather than using the whole text content of an email, some characteristic features can be extracted per email, that will be fed to the classifier.

These features are [1] :

a) F1: The number of sentences in an email.

b) F2: The number of verbs in an email.

c) F3: The number of words containing both numeric and alphabetical characters.

d) F4: The number of words in an email that are found in the spam list.

e) F5: The number of words in an email that have more than 3 syllables.

f) F6: The average number of syllables of words in an email.

g) F7: The number of spelling mistakes in an email.

# Comparing Classifiers

MultinomialNB
**Precision**  :  0.69189569143
**Recall**  :  0.733080808081
**F1_score**  :  0.70845763602


K-means
**Precision**  :  0.738331799231
**Recall**  :  0.711724386724
**F1_score**  :  0.723683959353


Random Forest
**Precision**  :  0.780027453672
**Recall**  :  0.715873015873
**F1_score**  :  0.741363907088

It is observed that the highest performing classifier is the Random Forest Classifier.

# Libraries
* sklearn
* nltk
* numpy
* glob
* pyphen
* enchant

# Reference
http://www.elg.uottawa.ca/~nat/Courses/csi5387_Winter2014/paper13.pdf
