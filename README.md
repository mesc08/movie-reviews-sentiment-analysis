# MOVIE-REVIEW-SENTIMENT-ANALYSIS

## DATASET

This project contains an example sentiment analysis project that utilizes the IMDb movie review dataset found here: [IMDb Movie Reviews](http://ai.stanford.edu/~amaas/data/sentiment/)

After downloading:-
As the dataset is split evenly with 25k reviews intended for training and 25k for testing your classifier. Moreover, each set has 12.5k positive and 12.5k negative reviews.
IMDb lets users rate movies on a scale from 1 to 10. To label these reviews the curator of the data labeled anything with ≤ 4 stars as negative and anything with ≥ 7 stars as positive. Reviews with 5 or 6 stars were left out. Movies datas are merged into common directory in the form of two text files acting as labels.
```
1. gunzip -c aclImdb_v1.tar.gz | tar xopf -
2. cd aclImdb && mkdir movie_data
3. sh
4. for split in train test; do for sentiment in pos neg; do for file in $split/$sentiment/*; do cat $file >> movie_data/full_${split}.txt; echo >> movie_data/full_${split}.txt;    done; done; done;
5.exit
```
## APROACH

### LOGISTIC REGRESSION

```MODEL ACCURACY ACHIEVED: 87.93```
### STEMMING

```MODEL ACCURACY ACHIEVED:85.79```
### BASELINE

```MODEL ACCURACY ACHIEVED:87.93```
### LEMMANTIZATION

```MODEL ACCURACY ACHIEVED:87.78```
### NGRAM

```MODEL ACCURACY ACHIEVED:```
### REMOVING STOP WORDS

```MODEL ACCURACY ACHIEVED:89.76```
### USING WORD COUNT

```MODEL ACCURACY ACHIEVED:88.196```
### TFIDVECTORIZER

```MODEL ACCURACY ACHIEVED:88.24```
### SVM

```MODEL ACCURACY ACHIEVED:89.76```
### FINAL MODEL

```MODEL ACCURACY ACHIEVED:89.932```

## TECHNOLOGY USED:
Jupyter Labs, scikit-learn, numpy, pandas

## LANGUAGE USED:
Python

## ENVIRONMENT
Anaconda
