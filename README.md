# Health Risk Prediction with Ensemble Learning

## 📌 Project Overview

This project focuses on building a supervised machine learning system to classify individuals into **Healthy** and **Unhealthy** categories based on health, lifestyle, and medical-history features.

The main focus of this project is **Ensemble Learning**. Instead of relying on a single machine learning algorithm, multiple classification models are trained and evaluated, followed by an ensemble approach using a **Voting Classifier**.

The goal is to compare different models and understand whether combining multiple learners can provide a stronger and more reliable classification approach.

---

## 🎯 Problem Statement

A biomedical research institute wants to identify individuals who are generally healthy and those who may be at higher health risk.

The dataset contains health and lifestyle information collected from **9,800 individuals**. The task is to develop a machine learning classification model that predicts the health outcome of each individual.

The predictions can support:

- Selection of eligible participants for clinical trials
- Population stratification based on health risk
- Risk-based analysis and outcome comparison

---

## 📊 Dataset

The dataset contains a combination of numerical and categorical health indicators.

### Important Features

- Age
- BMI
- Blood Pressure
- Cholesterol
- Glucose Level
- Heart Rate
- Sleep Hours
- Exercise Hours
- Water Intake
- Stress Level
- Smoking
- Alcohol
- Diet
- Mental Health
- Physical Activity
- Medical History
- Allergies
- Blood Group
- Diet Type

### Target

The target variable represents the individual's health outcome:

- **Healthy**
- **Unhealthy**

---

## 🤖 Machine Learning Models

The following classification algorithms were implemented and evaluated:

1. Logistic Regression
2. K-Nearest Neighbors (KNN)
3. Random Forest
4. Gradient Boosting
5. Voting Classifier

---

## 🧠 Ensemble Learning

The key part of this project is the use of **ensemble learning**.

Individual models can have different strengths and weaknesses. Ensemble learning combines predictions from multiple models to potentially produce a more robust final prediction.

### Voting Classifier

A **Voting Classifier** is used to combine multiple machine learning models.

Conceptually:

```text
              ┌─────────────────────┐
              │ Logistic Regression │
              └──────────┬──────────┘
                         │
              ┌──────────▼──────────┐
              │        KNN          │
              └──────────┬──────────┘
                         │
              ┌──────────▼──────────┐
              │   Random Forest     │
              └──────────┬──────────┘
                         │
              ┌──────────▼──────────┐
              │ Gradient Boosting   │
              └──────────┬──────────┘
                         │
                         ▼
                ┌─────────────────┐
                │ Voting Classifier│
                └────────┬────────┘
                         │
                         ▼
                  Final Prediction
📈 Model Evaluation

The models were evaluated using classification performance metrics, with particular attention given to Recall.

Model	Recall
Logistic Regression	82.8%
KNN	88.3%
Random Forest	95.8%
Gradient Boosting	94.9%
Voting Classifier	93.07%

Based on Recall, Random Forest achieved the highest recall of 95.8% among the evaluated models.

The Voting Classifier also demonstrated strong performance, achieving a recall of 93.07%.
