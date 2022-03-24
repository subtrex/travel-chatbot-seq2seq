# Generative type Travel Chatbot using Seq2Seq model

A Generative type Travel Chatbot using Natural Language Processing and Seq2Seq (Encoder-Decoder) model, which can answer basic queries on Kolkata tourism. 

## Tech

Python | NLTK | TensorFlow | Keras

## Data

We made use of a custom dataset, consisting of 1084 question/answer pairs on various topics of Kolkata tourism. We stored the data in simple text files.

## Methodology

1 - Reading : We read the data from the text files and created 2 lists to store the questions in one, and the corresponding answers in the other one.  
2 - Preprocessing : We performed certain preprocessing steps on the lists, which included removal of punctuations (except comma because it helps to separate multiple proper nouns) -> removal of special characters -> changing all text to lower case -> tokenization -> stop words removal -> numeric and special characters removal -> POS tagging -> word stemming/lemmatization.  
3 - Train Test Split : We divided our dataset into training and testing data in 80:20 ratio.  
4 - Pipelines : We defined various pipelines i.e. sequentially applied a list of transforms and a final estimator. The basic structure of the pipelines are CountVectorizer -> TFIDFVectorizer -> ClassifierModel. Then we trained the pipeline on the training data and used the testing data for prediction results.
