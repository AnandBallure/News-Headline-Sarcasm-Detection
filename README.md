# News-Headline-Sarcasm-Detection

## Data Collection
- Downloaded the JSON file from kaggle.


## Cleaning and Transforming
- First lower-casing all the words in the dataset.
- Removing punctuations from all of the corpus.
- Tokenizing words using the *word tokenizer* from *NLTK*.
- Segregating the English stopwords using the *NLTK.Corpus library*.
- Using the *WordCloud* library to generate a wordcloud of the most frequent words labelled as *Sarcasm* in the entire dataset.


![](https://github.com/AnandBallure/News-Headline-Sarcasm-Detection/blob/main/wordcloud.png)



## Preprocessing
- Using the *Tokenizer* from the *tensorflow.keras* library to tokenize each word and get the sequence of numbers for each corpus.
- As all of the sentences are not of same length, each sentence is *post-padded* i.e., with 0's at the end.



## Train/Test Split
- Train and test sets were created using the *train_test_split* from *Sklearn*.
- Target is a binary classification column with 0 meaning *Not Sarcastic* and 1 meaning *Sarcastic*.



## Training 
- Created sequential neural networkes with 1 input layer, 1 output layer and 3 dense layers.
- Additionally, created 1 *embedded layer* to make appropriate relations between the words in the *n-dimentional* vector space and improve model performance.
- Model was set to monitor the *validation loss* for the training set with 100 epochs and was to impliment *early stopping* when there was no improvement in the validation_loss for 3 consecutive epochs. 
- The weights were also adjusted with the best validation score.



## Results
- Model performed quite well in detecting sarcasm considering *"sarcasm is quite easy to detect."*
- Achieved an accuracy of 87.11% and AUC of 0.94.


![](https://github.com/AnandBallure/News-Headline-Sarcasm-Detection/blob/main/sarcasm-cmx.png)


- Classification report: 

![](https://github.com/AnandBallure/News-Headline-Sarcasm-Detection/blob/main/clr.jpg)
