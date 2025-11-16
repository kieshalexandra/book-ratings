# Comparing K-Nearest Neighbors and Decision Trees for Predicting Top-Rated Books

This repository contains the implementation for Assignment 2 from COMP20008 – Elements of Data Processing, The University of Melbourne. The project explores the Book-Crossing dataset to build a predictive model that determines whether a user is likely to give a book a top rating. The code focuses on data preprocessing, exploratory data analysis, and machine learning, comparing the performance of K-Nearest Neighbors (KNN) and Decision Trees.

# 📁 Repository Structure
```
├── A2 README.txt                    # Original instructions / assignment notes
├── BX-Books.csv                     # Book metadata
├── BX-NewBooks.csv                  # Not used in this project
├── BX-NewBooksRatings.csv           # Not used in this project
├── BX-NewBooksUsers.csv             # Not used in this project
├── BX-Ratings.csv                   # User-book ratings
├── BX-Users.csv                     # User demographic data
├── README.md                        # Project documentation (this file)
└── a2.py                            # Main script for analysis and modelling
```

# 🔍 Project Overview
### Goal
To compare the performance of KNN and Decision Tree classifiers in predicting whether a user will give a book a top rating.

This question supports the broader goal of helping an online bookstore understand rating behaviours and improve recommendation strategies.

### Dataset
The project uses three key datasets from the Book-Crossing collection:
- BX-Books.csv — Book metadata (ISBN, title, author, year)
- BX-Users.csv — Demographic information (age, location)
- BX-Ratings.csv — User–book rating interactions

# 🧼 Data Preprocessing

The script (a2.py) performs several cleaning and transformation steps, including:
- Handling missing or implausible user demographic data
- Filtering inconsistent book metadata
- Merging book, user, and rating datasets
- Creating a binary classification target (Top-Rated vs Not Top-Rated)
- Preparing features for modelling (encoding, scaling where needed)

# 📊 Exploratory Data Analysis (EDA)

The analysis includes:
- Distribution of ratings
- Patterns across age groups
- Popular authors / books
- Visualisations (histograms, bar charts, etc.)
- Summary statistics and insights into user behaviour

# 🤖 Machine Learning Models

Two supervised learning models were implemented:
**1. K-Nearest Neighbors (KNN)**
- Instance-based learning
- Sensitive to feature scaling
- Evaluated using k-value tuning

**2. Decision Tree Classifier**
- Rule-based model
- Naturally interpretable
- Captures non-linear relationships

Both models were trained to predict whether a rating falls into the top-rated category. They were then evaluated on key evaluation metrics susch as accuracy, precision, recall, F1-Score, and confusion matrix.

# ▶️ Running the Code
Install dependencies
```
pip install pandas numpy scikit-learn matplotlib seaborn
```

Execute the script
```
python a2.py
```

The script will load datasets, preprocess the data, run both models, and output results.

# Key Findings
1. KNN Outperforms Decision Trees Across Most Metrics
2. Decision Trees Still Provide Valuable Insights
3. The Dataset Is Imbalanced, Affecting Model Performance
