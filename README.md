# MOVIE-REVIEW-SENTIMENT-ANALYSIS

### DATASET

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


### LOGISTIC REGRESSION

1. Step1 Read the file and store them in the form of list .
2. Undergo cleaning and preprocess where we remove all the extra punctuations and symbols along with extra spaces(NLP task).
3. Vectorization is done to convert each review data into numeric data
4. Build logisticRegression classifier where the X and Xtest is the clean  data recieved after cleaning process && find the best c with high accuracy score.
5. Final model is then trained based on the c value obtained and print the words which are positive and negative based on the coeff value.
