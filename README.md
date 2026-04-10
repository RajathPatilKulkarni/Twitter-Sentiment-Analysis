# Twitter Sentiment Analysis

## Introduction

This project performs **Twitter Sentiment Analysis** using Natural
Language Processing (NLP) and Machine Learning techniques. The model
classifies tweets into sentiment categories by cleaning text data,
removing noise, converting text into numerical features, and training a
supervised machine learning classifier.

The dataset used in this project is:

    twitter_training.csv

This project demonstrates a complete NLP pipeline from raw tweets to
sentiment prediction.

------------------------------------------------------------------------

## Table of Contents

-   Installation
-   Dataset
-   Features
-   Technologies Used
-   Data Preprocessing
-   Feature Engineering
-   Model Training
-   Evaluation
-   Prediction
-   Project Structure
-   Troubleshooting
-   Author
-   License

------------------------------------------------------------------------

## Installation

Install required libraries:

``` bash
pip install numpy pandas matplotlib seaborn scikit-learn nltk
```

------------------------------------------------------------------------

## Dataset

File used:

    twitter_training.csv

Dataset contains:

-   Tweet text
-   Sentiment label

Example:

    Tweet,Sentiment
    "I love this!",Positive
    "This is bad",Negative
    "Not sure about this",Neutral

Place dataset in project root directory.

------------------------------------------------------------------------

## Features

-   Twitter text preprocessing
-   Lowercase normalization
-   Stopword removal
-   Punctuation removal
-   Tokenization
-   Stemming / Lemmatization
-   Feature extraction (TF-IDF / CountVectorizer)
-   Machine learning classification
-   Sentiment prediction
-   Model evaluation

------------------------------------------------------------------------

## Technologies Used

-   Python
-   Pandas
-   NumPy
-   Scikit-learn
-   NLTK
-   Matplotlib
-   Seaborn
-   Jupyter Notebook

------------------------------------------------------------------------

## Data Preprocessing

The following preprocessing steps are applied:

1.  Load dataset
2.  Clean tweet text
3.  Convert to lowercase
4.  Remove punctuation
5.  Remove stopwords
6.  Tokenization
7.  Stemming / Lemmatization
8.  Remove extra whitespace

Example:

``` python
def clean_text(text):
    text = text.lower()
    text = re.sub(r'[^a-zA-Z]', ' ', text)
    tokens = text.split()
    return " ".join(tokens)
```

------------------------------------------------------------------------

## Feature Engineering

Text is converted into numerical features using:

-   Count Vectorizer or
-   TF-IDF Vectorizer

Example:

``` python
from sklearn.feature_extraction.text import TfidfVectorizer

vectorizer = TfidfVectorizer()
X = vectorizer.fit_transform(text)
```

------------------------------------------------------------------------

## Model Training

Dataset is split into training and testing sets:

``` python
from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)
```

Train model:

``` python
model.fit(X_train, y_train)
```

------------------------------------------------------------------------

## Evaluation

Model performance is evaluated using:

-   Accuracy Score
-   Confusion Matrix
-   Classification Report

``` python
from sklearn.metrics import accuracy_score

accuracy = accuracy_score(y_test, y_pred)
print(accuracy)
```

------------------------------------------------------------------------

## Prediction

Predict sentiment for new tweet:

``` python
tweet = ["This product is amazing"]
prediction = model.predict(tweet)
print(prediction)
```

------------------------------------------------------------------------

## Project Structure

    Twitter-Sentiment-Analysis/
    │── Twitter_Sentiment_Analysis.ipynb
    │── twitter_training.csv
    │── README.md

------------------------------------------------------------------------

## Troubleshooting

### NLTK stopwords missing

``` python
import nltk
nltk.download('stopwords')
```

### Punkt tokenizer error

``` python
nltk.download('punkt')
```

------------------------------------------------------------------------

## Author

Rajath Patil Kulkarni

------------------------------------------------------------------------

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
