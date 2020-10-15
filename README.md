# Sentiment-Analysis
Sentiment Analysis of CoronaVirus Tweets using Bidirectional LSTM approach.<br />
Classified tweets in 5 categories :-<br />
1. Extremely Positive
2. Positive
3. Neutral
4. Negative
5. Extremely Negative<br /><br />

The dataset used to perform Sentiment analysis is publicly available on Kaggle website.<br />
The same can be downloaded from https://www.kaggle.com/datatattle/covid-19-nlp-text-classification.<br /><br />

This Dataset contain 4 columns :-<br />
1. Location<br />
2. TweetAt<br />
3. OriginalTweet<br />
4. Sentiment<br /><br />

Steps :-<br />
1. Run Preparing_dataset.ipynb<br />
2. Run Pre-processing_dataset.ipynb<br /><br />
3. Run Training_using_bidirectional_LSTM.ipynb<br /><br />

Methedology :-<br />
The dataset is prepared and extracted only Original Tweets and Sentiments for analysis.<br /><br />

Then the text in the Original Tweets are pre-processes and cleaned.<br /><br />

In pre-processing :-<br />
a) All the letters are converted in Lower case letters.<br />
b) Expanding of contractions has been done for our model to learn better from the data.<br />
For expanding of contactions Google News Vector dictionary has been used.<br />
It can be downloaded from https://code.google.com/archive/p/word2vec/<br />
c) Removed special characters and numbers using String library.<br />
d) Removed extra spaces from the text.<br /><br />

After Pre-processing of the text, the data is splitted into Data(Tweets) and labels(Sentiments).<br /><br />

Now to feed the data to the model, we need to convert the words in the sentences into numbers.<br />
Tokenization has to be performed on the sentences.<br />
Tokenization of the sentences is done using Keras preprocessing library.<br /><br />

Then to make the length of all the sentences equal. We Pad all the sentences to a particular length.<br />
Padding is done using Keras preprocessing library.<br /><br />

Then, to feed the Sentiments to the model. We One-Hot Encode the Sentiments using keras.to_utils library.<br /><br />

Then we made an Embedding layer using pre-trained GLoVe library.<br />
Sentences are needed to pass from this layer before entering any other layer.<br /><br />

Then we will build out Sequential model based on Bidirectional LSTM using Keras framework.<br /><br />

Then will be compile our built model.<br />
Loss      = "Categorical Cross Entropy"<br />
Optimizer = "Adam"<br /><br />

Finally, we will train our model.<br /><br /><br />


The results are shown below :-<br />

<img src="https://github.com/gearhead0909/Sentiment-Analysis/blob/master/Accuracy.png" alt="alt text" width="500" height="300"><br /><br />
<img src="https://github.com/gearhead0909/Sentiment-Analysis/blob/master/Loss.png" alt="alt text" width="500" height="300"><br /><br />

Achieved an accuracy of 72%
