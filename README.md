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

* imdb review logistic regression-CountVectorizer.ipynb: This notebook contains a logistic regression model trained to classify the movie review as positive or negative.

The vectorization method used is <strong>CountVectorizer</strong> 

CountVectorizer in brief is provides a simple way to both tokenize a collection of text documents and build a vocabulary of known words, but also to encode new documents using that vocabulary.

* imdb review logistic regression-TfIdf Vectorizer.ipynb: Notebook is similar to the above, but the vectorization used is <strong>TfIdf vectorizer.</strong>

TF-IDF is an abbreviation for Term Frequency-Inverse Document Frequency and is a very common algorithm to transform text into a meaningful representation of numbers. The technique is widely used to extract features across various NLP applications.




