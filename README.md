# Sentiment Analysis Project

## Introduction
This project focuses on sentiment analysis using Arabic text data. The goal is to develop a model capable of classifying text into three sentiment categories: positive, negative, and neutral.

## Data Exploration
The project begins with exploratory data analysis to understand the dataset. Main issues identified include:
- Presence of English text
- Data imbalance
- Emojis between text
- Duplicated letters within words

## Data Preprocessing
To address the identified issues, several preprocessing steps are performed:
- Removing punctuation, emojis, and repeating characters
- Balancing target classes through oversampling
- Removing English text from the data
- Tokenization, removing stop words, and stemming

## Preparing Data for Training
The data is prepared for training by:
- Exploring different word vectorization techniques (Bag of Words, TF-IDF, word embedding)
- Choosing word embedding due to its suitability for deep learning models
- Applying tokenization and padding vectors with zeros

## LSTM Model
Long Short-Term Memory (LSTM) networks are chosen for sentiment analysis due to their ability to capture long-range dependencies in sequential data. The model architecture includes:
- Embedding layer for vectorizing text data
- LSTM layer with 15 neurons
- Output layer with softmax activation function for multiclass classification

## Model Performance
Different approaches are explored to improve model accuracy, including:
- Increasing the number of neurons (30 and 100)
- Balancing imbalanced data with weighted classes
However, these attempts resulted in overfitting. The best-performing architecture uses 15 neurons and employs oversampling to balance the underrepresented class.

## Results
The final model achieved the following accuracy:
- Training accuracy: 86.97%
- Test accuracy: 86.26%

## Conclusion
The project demonstrates the effectiveness of LSTM networks for sentiment analysis in Arabic text. Despite challenges such as data imbalance and overfitting, the model achieves satisfactory performance through careful preprocessing and model tuning.
