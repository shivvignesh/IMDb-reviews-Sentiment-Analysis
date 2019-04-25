# IMDb movie reviews for Sentiment Analysis 

Movie Reviews are never direct statements Good/Bad, Awful/Awesome, Boring/Entertaining but are a bunch of sentences which kind of beat around the bush. Especially the reviews written by a movie critic are loaded with all fancy words which sometimes confuse a common man.The use of fancy words cannot differentiate between good review or a bad review with confidence, but always feels like it is somewhere in between.

## Install

This project requires python 3.6 or any other higher versions of python along with the following libraries installed:

* Numpy
* Pandas
* matplotlib
* scikit-learn
* Seaborn
* Keras
* nltk 
* re(Regular Expressions)

You also need a software to run this python notebook, "Jupyter Notebook". It is highly recommended that you install the Anaconda distribution of Python, which already has the above packages and more included.

## Description of the Dataset & Attribute information

IMDb reviews dataset can be found on kaggle https://www.kaggle.com/oumaimahourrane/imdb-reviews. The dataset contains 25k reviews (approx) & only two columns which are <strong>SentimentText</strong> and <strong>Sentiment</strong>. This contains 25k highly polar reviews for binary classification. The Sentiment column which contains the binary classified output for each review, 
* 1- positive review
* 0- negative review

## Description of the repository

The repository contains 4 notebooks

* imdb_reviews.ipynb: This notebook contains feature engineering and data visualization of the dataset. 

* imdb review logistic regression-CountVectorizer.ipynb: This notebook contains a logistic regression model trained to classify the movie review as positive or negative.

The vectorization method used is <strong>CountVectorizer</strong> 

CountVectorizer in brief is provides a simple way to both tokenize a collection of text documents and build a vocabulary of known words, but also to encode new documents using that vocabulary.

* imdb review logistic regression-TfIdf Vectorizer.ipynb: Notebook is similar to the above, but the vectorization used is <strong>TfIdf vectorizer.</strong>

TF-IDF is an abbreviation for Term Frequency-Inverse Document Frequency and is a very common algorithm to transform text into a meaningful representation of numbers. The technique is widely used to extract features across various NLP applications.

* imdb_review_Keras_(reduced_validation_loss).ipynb : Neural Network implementation of the dataset. 


## Brief on Feature Engineering for this dataset:
	
* Removing a particular pattern using Regular Expressions: Punctuations, numbers, brackets and other symbols are removed to reduce the size of the corpus, these dont play a significant role in the classification of the model. 

* Removing stop words: Stop words are natural language words which have very little meaning, such as "and", "the", "a", "an", and 	similar words. These are filtered out for data preprocessing, as these contain very little meaning they hardly or dont 		contribute to the prediction of the model, thus eliminating them is best.

* Tokenizing the Text : The text or the SentimentText is split into a Panda Series, where each review is split into an array of 	words. Tokenization is helpful in the process of Stemming and Lemmatization process. 

* Stemming: In linguistic morphology and information retrieval, stemming is the process of reducing inflected words to their word stem, base or root form

* Lemmatization: Lemmatisation in linguistics is the process of grouping together the inflected forms of a word so they can be analysed as a single item, identified by the word's lemma. For example, runs, running, ran are all forms of the word run, therefore run is the lemma of all these words.

* Removing words with less occurances: The words whose occurances are less than say 10, dont actually contribute to the 	prediction. These words could be a city, proper noun, items or entities. These dont really say good or bad but remain true to their native meaning. Removing these words from the corpus would reduce the size, greater computation speed, increase in accuracy. 
	
## Models trained on :
 
 Model|Accuracy
 -----|--------
Logistic Regression with CountVectorizer| 87.74%
Logistic Regression with TfIdfVectorizer| 87.52%
Neural Networks | 88.52%