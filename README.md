<h1 align="center">
             Stress-Prediction
</h1>

## Context 

We live in an era where there is a surplus of information flowing in every second. Sometimes this leads to stress. ☹️
Too much stress can negatively impact our health and may lead to headaches, high blood pressure, heart problems, diabetes, skin conditions, asthma, arthritis, depression, and anxiety.

## Data

A dataset of lengthy multi-domain social media data for identifying stress from five different categories of Reddit communities.

## Data Preprocessing & Cleaning

- Text Normalization

We began by normalizing the text data as it contains special character, numerical values and unnecessary spaces.
We used the regex library to remove repaeated characters, punctauation, numerical values, non-english words and also converted the text to lower case.

- Lemmatization

Lemmatization is a process in natural language processing (NLP) that involves reducing words to their base form, or lemma.
For example, the lemma of the word "jumps" is "jump," and the lemma of the word "running" is "run."
Lemmatization is often used as a preprocessing step in NLP tasks, such as text classification, because it can help reduce the dimensionality of the data by reducing the number of variations of a word that need to be considered.
lemmatization can also improve the performance of a text classification model by allowing it to generalize better to new examples.In this data, we have used the 'WordNetLemmatizer' from the nltk library to perform lemmatization.

- Stop Words Removal

Stop words are common words in a language that are not considered to have much meaning and are usually removed from texts before processing. These words include articles, conjunctions, and prepositions, as well as some pronouns and verb forms. For example, in the English language, common stop words include "a," "an," "and," "the," "but," "or," and "of."
Stop words are often removed from texts as a preprocessing step because they do not contribute much to the meaning of a sentence and can often increase the dimensionality of the data unnecessarily. Removing stop words can help reduce the size of the dataset and make it easier to process, as well as improve the performance of certain NLP tasks, such as text classification or information retrieval.
However, some stop words are really crucial for model and for that we have searched the data set for commom potential stop words.Using the commom potential stop words we have manually selected the stop words and added to our stop words list.

- Tokenization

Tokenization is the process of breaking a stream of text up into words, phrases, symbols, or other meaningful elements, known as tokens. The tokens can then be used for various natural language processing (NLP) tasks such as information retrieval, language translation, and text classification.
Tokenization is necessary for many NLP tasks because it allows the computer to analyze and understand the structure and meaning of the text. For example, in order to perform sentiment analysis on a piece of text, it is necessary to first tokenize the text so that the computer can determine which words are positive, negative, or neutral. 
we have implemented this by using 'Tokenizer' from the keras library.

- Padding
Padding is a technique used in natural language processing (NLP) to handle sequences of text that have different lengths. It involves adding a special character, known as a padding token, to the end of shorter sequences so that all sequences have the same length.
Padding is necessary because many NLP models, such as neural networks, require input data to have a fixed size. For example, if you are training a model to classify text as positive or negative, you might need to feed it a batch of text sequences that are all the same length. However, the text sequences in your dataset may not all be the same length, so you need to pad the shorter sequences with padding tokens to make them the same length as the longest sequence in the batch.

## Libraries Used

1.ScikitLearn
2.Pandas
3.Numpy
4.Keras
5.NLTK
6.Tensorflow
7.Matplotlib
8.Regex

## Features Selected :
1. Text
2. Label - Stress (0) or No stress (1)

## Model Used 

For this project, we have used the LSTM (Long Short-Term Memory) Model. It is a type of recurrent neural network (RNN) that is well-suited for text classification tasks. RNNs are a type of neural network that process sequential data, such as text, by looping over the sequence and processing each element one at a time while maintaining an internal state that encodes information about the past elements in the sequence. LSTMs have been widely used for text classification tasks because they can effectively process and classify long sequences of words, even when those words are highly dependent on each other. This makes them well-suited for tasks like sentiment analysis, where the overall sentiment of a piece of text may be influenced by words that appear earlier in the sequence.


