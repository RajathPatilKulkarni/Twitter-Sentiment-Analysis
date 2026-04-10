# Twitter Sentiment Analysis

## Introduction

This project performs **Twitter Sentiment Analysis** using Natural
Language Processing (NLP) and Machine Learning. Tweets are classified
into sentiment categories using preprocessing, vectorization, and
supervised learning.

This project was developed by **Rajath Patil Kulkarni**.

------------------------------------------------------------------------

## Features

-   Tweet preprocessing
-   Stopword removal
-   Tokenization
-   Text cleaning
-   Feature extraction
-   Machine learning model
-   Sentiment prediction

------------------------------------------------------------------------

## Technologies Used

-   pandas
-   sklearn

------------------------------------------------------------------------

## Installation

``` bash
pip install numpy pandas matplotlib seaborn scikit-learn nltk
```

------------------------------------------------------------------------

## Usage

Run the notebook:

``` bash
jupyter notebook Twitter_Sentiment_Analysis.ipynb
```

------------------------------------------------------------------------

## Workflow

1.  Load dataset\
2.  Clean tweet text\
3.  Remove stopwords\
4.  Tokenization\
5.  Feature extraction\
6.  Train model\
7.  Evaluate accuracy\
8.  Predict sentiment

------------------------------------------------------------------------

## Example Prediction

``` python
tweet = ["This is a great product"]
prediction = model.predict(tweet)
print(prediction)
```

------------------------------------------------------------------------

## Project Structure

    Twitter-Sentiment-Analysis/
    │── Twitter_Sentiment_Analysis.ipynb
    │── dataset.csv
    │── README.md

------------------------------------------------------------------------

## Author

**Rajath Patil Kulkarni**

------------------------------------------------------------------------

## License

MIT License
