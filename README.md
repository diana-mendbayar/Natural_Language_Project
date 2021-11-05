
This project consists of three notebooks. 
In the end, it gets the description from dataset and 
predict its industry using different classificaiton models. All predictions are in clean_set.csv

The first notebook focuses on cleaning the dataset:
1. created regex to remove phone numbers from dataset, 
   and numbers are non US and US, so area code can be variety.
2. created functions to remove punctutation, numbers, and urls.
3. used snowball stemmer and lemmatizer
4. created stopwords

The second notebook is for training tfdif vectors and using LDA to predict the industry
1. made the cleaning(preprocessing) more generalized, it used a function to apply all dataset
2. copied preprocessed data to new column to access easier
3. used vectorizers, such as count, hashing, and tfdif and
   looking at the result, decided to go with tfdif vectorizer
4. implementing Latent Dirichlet Allocation (LDA) model to predict the industry was hard,
   because we didn;t know how to use the data for prediciton

The third notebook is for training tfdif vectors using KMeans to predict the industry, 
and word repsentation model:
1. KMeans was hard at first, because again we didn't know how to use the vectorized data for prediciton
2. made embeddings representation of each industry using spacy to find the closest industry of given description