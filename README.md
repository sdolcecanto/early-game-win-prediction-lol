# Early Game Win Prediction in League of Legends
## Overview

This project builds a machine learning model to predict the outcome of a League of Legends match using only early-game data (first 10–15 minutes). The objective is to evaluate how well early performance determines match results and to identify the most relevant features influencing victory.

## Objective
- Predict match outcome (win/loss) from early-game features
- Compare different classification models
- Identify the key variables driving predictions

## Dataset

The dataset contains structured match data extracted from League of Legends games. Each observation represents a match at a fixed early-game timestamp.

Main features include:
- Gold difference
- Kills and deaths
- Towers destroyed
- Neutral objectives (e.g., dragons, heralds)
- Other early-game performance indicators

## Methodology

### Data Preparation
- Cleaned and structured raw data
- Handled missing values
- Selected and engineered relevant features
- Defined early-game cutoff window

### Modelling
The following models were trained and compared:

- Logistic Regression (baseline)
- Random Forest

Model performance was evaluated using:

- Accuracy
- Precision and recall
- F1-score
- Confusion matrix

# Results

Model performance (accuracy):

- Random Forest: 72.1%    
- Cross-validated RF: 72.6%    
- Tuned RF (CV best): 73.0%   (AUC ≈ 0.81)

A confusion matrix and feature importance plot are included in the notebook for further analysis.

# Key Findings

The best-performing model (Random Forest) achieved approximately 72–73% accuracy, with consistent performance across cross-validation, indicating stable generalization. The AUC value 0.81 indicates good discriminative ability, suggesting that the model is able to distinguish between wins and losses effectively.

Gold difference was the most important predictor of match outcome, followed by experience difference, suggesting that overall resource advantage is more informative than isolated events such as kills.

## Tech Stack
- Python  
- pandas, numpy  
- scikit-learn  
- matplotlib / seaborn  