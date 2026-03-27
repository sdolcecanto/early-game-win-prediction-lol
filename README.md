# Early-Stage Outcome Prediction Using Quantitative Match Features

## Overview

This project builds a classification model to predict final outcomes using only early-stage quantitative features (first 10–15 minutes of activity). The goal is to evaluate how strongly early performance metrics determine final results and to identify the most informative variables.

The dataset is derived from League of Legends matches, but the methodology is general and applicable to early-stage prediction problems.

---

## Objective

* Predict binary outcome (win/loss) from early-stage features
* Compare baseline and ensemble models
* Identify key drivers of prediction

---

## Dataset

The dataset consists of structured match-level observations at a fixed early timestamp.

Features include:

* Resource metrics (gold difference, experience difference)
* Performance indicators (kills, deaths)
* Objective control (towers, neutral objectives)
* Aggregated early-game statistics

---

## Methodology

### Data Preparation

* Data cleaning and preprocessing
* Handling missing values
* Feature selection and engineering
* Definition of early-stage cutoff window

---

### Modelling

The following models were implemented:

* Logistic Regression (baseline)
* Random Forest

Evaluation metrics:

* Accuracy
* Precision / Recall
* F1-score
* ROC-AUC

---

## Results

* Random Forest: 72.1% accuracy
* Cross-validated RF: 72.6%
* Tuned RF (best CV): 73.0%
* ROC-AUC: ~0.81

The model shows stable performance across cross-validation, indicating good generalization.

---

## Key Findings

* Early-stage features provide strong predictive power for final outcomes
* Resource-related variables (especially gold difference) are the most important predictors
* Global performance indicators outperform isolated event-based features

---

## Tech Stack

* Python
* pandas, numpy
* scikit-learn
* matplotlib / seaborn
