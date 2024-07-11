# Quora Question Pair Similarity

This project predicts the similarity between pairs of questions from Quora using various features such as token features, length features, fuzzy features, and Bag of Words (BoW) features. The models used include Random Forest and XGBoost, with Random Forest achieving higher accuracy.

## Table of Contents

- Introduction
- Installation
- Usage
- Features
- Preprocessing
- Feature Extraction
- Model Training


## Introduction

This project aims to build a machine learning model that determines whether two questions asked on Quora are similar. It utilizes both Random Forest and XGBoost models to predict question pair similarity, with Random Forest demonstrating superior accuracy.

## Dataset

The dataset used for this project can be accessed from (https://www.kaggle.com/datasets/kushalbarot/quora-train).
The real and whole dataset can be accessed from (https://www.kaggle.com/competitions/quora-question-pairs).



## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/quora-question-pair-similarity.git
    cd quora-question-pair-similarity
    ```

2. Create and activate a virtual environment:
    ```bash
    python -m venv env
    source env/bin/activate  # On Windows use `env\Scripts\activate`
    ```

3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. Load the necessary data files, including `cv.pkl` and `model.pkl`.
2. Preprocess the input questions.
3. Extract features using token features, length features, fuzzy features, and Bag of Words (BoW) features.
4. Train the Random Forest and XGBoost models.
5. Use the trained models to predict the similarity between question pairs.

## Features

- **Token Features:** Extracts common and unique tokens between the question pairs, along with common stopwords.
- **Length Features:** Calculates features based on the length of the questions and the longest common substring.
- **Fuzzy Features:** Uses fuzzy string matching techniques to assess similarity.
- **Bag of Words Features:** Uses a CountVectorizer to convert text into a vector representation.

## Preprocessing

The preprocessing steps include:
- Converting text to lowercase.
- Replacing special characters with their string equivalents.
- Expanding contractions.
- Removing HTML tags.
- Removing punctuation.

## Feature Extraction

The feature extraction process includes:
- Token features: Common non-stopwords, common stopwords, and token comparisons.
- Length features: Absolute length difference, average token length, and longest common substring ratio.
- Fuzzy features: Fuzzy matching ratios (QRatio, partial ratio, token sort ratio, token set ratio).
- BoW features: Vectorized representation of the text using CountVectorizer.

## Model Training

Train both Random Forest and XGBoost models using the extracted features. Random Forest has shown better accuracy for predicting question pair similarity in this project.
