# Sentiment-Analysis
Sentiment Analysis of CoronaVirus Tweets using Bidirectional LSTM approach.
Classified tweets in 5 categories :-
1. Extremely Positive
2. Positive
3. Neutral
4. Negative
5. Extremely Negative

The dataset used to perform Sentiment analysis is publicly available on Kaggle website.
The same can be downloaded from https://www.kaggle.com/datatattle/covid-19-nlp-text-classification.

This Dataset contain 4 columns :-
1. Location
2. TweetAt
3. OriginalTweet
4. Sentiment

Steps :-
1. Run Preparing_dataset.ipynb
2. Run Pre-processing_dataset.ipynb
3. Run Training_using_bidirectional_LSTM.ipynb

Methedology :-
The dataset is prepared and extracted only Original Tweets and Sentiments for analysis.

Then the text in the Original Tweets are pre-processes and cleaned.

In pre-processing :-
a) All the letters are converted in Lower case letters.
b) Expanding of contractions has been done for our model to learn better from the data.
For expanding of contactions Google News Vector dictionary has been used.
It can be downloaded from https://code.google.com/archive/p/word2vec/
c) Removed special characters and numbers using String library.
d) Removed extra spaces from the text.

After Pre-processing of the text, the data is splitted into Data(Tweets) and labels(Sentiments).

Now to feed the data to the model, we need to convert the words in the sentences into numbers.
Tokenization has to be performed on the sentences.
Tokenization of the sentences is done using Keras preprocessing library.

Then to make the length of all the sentences equal. We Pad all the sentences to a particular length.
Padding is done using Keras preprocessing library.

Then, to feed the Sentiments to the model. We One-Hot Encode the Sentiments using keras.to_utils library.

Then we made an Embedding layer using pre-trained GLoVe library.
Sentences are needed to pass from this layer before entering any other layer.

