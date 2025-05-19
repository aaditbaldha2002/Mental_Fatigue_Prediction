# Mental_Fatigue_Prediction
An ML Project which uses the dataset of the keyboard typing feature values to predict whether the typist is experiencing mental fatigue or not

# Keystroke Dynamics Benchmark Dataset

This repository contains the **benchmark dataset** and supporting materials for the paper:

> *Comparing Anomaly-Detection Algorithms for Keystroke Dynamics*  
> by Kevin Killourhy and Roy Maxion  
> Published in: DSN 2009, IEEE

## 🔍 Overview

This dataset was developed to support reproducible research in **keystroke biometrics**, an area that explores identifying users based on their typing rhythms. It includes typing data from 51 subjects typing a strong password `.tie5Roanl` 400 times each, under controlled conditions.

The dataset has been used to evaluate 14 anomaly detection algorithms, such as:
- Scaled Manhattan
- One-Class SVM
- Mahalanobis Distance
- Neural Networks
- Fuzzy Logic
- k-Means Clustering

The evaluation aims to differentiate between legitimate and impostor typing behaviors for access-control and intrusion detection systems.

---

## 📂 Contents



---

## 📈 Dataset Description

- **Subjects**: 51 typists from a university population
- **Password**: `.tie5Roanl` (10 characters, strong)
- **Sessions**: 8 per subject, 50 repetitions per session
- **Total Samples**: 20,400 entries (400 per subject)
- **Features**:  
  - `H.key` — Hold time of key  
  - `DD.key1.key2` — KeyDown-KeyDown time  
  - `UD.key1.key2` — KeyUp-KeyDown time  
- **Columns**: 34 per row (subject, session, repetition + 31 timing features)

Each row represents one password typing attempt and its timing profile.

---

## 🚀 Getting Started

### Requirements

- [R](https://www.r-project.org/) (tested on 4.x)
- R Packages: `ROCR`

### Run Evaluation

```R
# Load evaluation script
source("scripts/evaluation-script.R")

