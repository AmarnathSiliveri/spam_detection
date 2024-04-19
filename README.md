# Spam Comment Detection

## Overview

This repository contains code for a  **spam comment detection** using a machine learning model called **Bernoulli Naive Bayes**. The detector reads comments from CSV files, preprocesses the data, and trains the model to classify comments as either **"Spam"** or **"Not Spam"**. Users can input a comment, and the detector will predict whether it's spam or not.

## Usage

### Reading Data:
The detector reads comments from five CSV files named `Youtube01-Psy.csv`, `Youtube02-KatyPerry.csv`, `Youtube03-LMFAO.csv`, `Youtube04-Eminem.csv`, `Youtube05-Shakira.csv`. which contain comments from various YouTube videos.

### Concatenating Data:
All comments are merged into a single DataFrame for easier processing.

### Preprocessing:
Only the **"CONTENT"** and **"CLASS"** columns are selected from the DataFrame. The **"CLASS"** column indicates whether a comment is spam (1) or not spam (0). The class labels are mapped to human-readable terms: **"Spam Comment"** and **"Not Spam"**.

### Model Training:
The data is split into training and testing sets. Text data is converted into numerical features using **CountVectorizer**, which converts each comment into a vector of word counts. A **Bernoulli Naive Bayes** model is trained on the training data to learn patterns in the comments.

### Prediction:
A function called `predict_spam` takes a comment as input and predicts whether it's spam using the trained model. The input comment is converted into numerical features using **CountVectorizer**, fed to the model, and the prediction is returned.

### User Interaction:
Users can enter a comment, and the detector will predict whether it's spam or not.

## Requirements

- Python 3
- pandas
- numpy
- scikit-learn

---

###

---
### Bernoulli Naive Bayes

**Bernoulli Naive Bayes** is like a specialized version of the Naive Bayes classifier, specifically designed for situations where our features (the things we're using to make predictions) are either there or not there—binary, in other words. 

Imagine you're dealing with text data, like comments on YouTube videos. Bernoulli Naive Bayes comes in handy for tasks like spam detection. Here's how it works:

Let's say we're trying to decide whether a comment is spam or not. The classifier looks at each word in the comment and asks, "Is this word present in our list of spammy words?" If it is, it counts it as a '1' (present); if not, it's a '0' (absent).



> Despite its simplicity, Bernoulli Naive Bayes tends to do a pretty good job, especially when you're dealing with a ton of words—like in big batches of comments.

###
---
![OUTPUT](https://github.com/SilverStark18/spam_detection/blob/main/spam_detection_output_image.png)




