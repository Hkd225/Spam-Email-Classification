Spam Email Classification and Machine Learning Model Benchmarking using Spambase Dataset (Ensemble Methods, SVM, & Neural Networks) - Project by Muhammad Auffa Hakim Aditya

=============================================================================
SPAM EMAIL CLASSIFICATION & MACHINE LEARNING MODEL BENCHMARKING
By Muhammad Auffa Hakim Aditya
=============================================================================

This project presents a comprehensive Machine Learning benchmarking study for Spam Email Classification using the well-known Spambase dataset. The primary objective is to compare the performance of various classical and ensemble Machine Learning algorithms in detecting spam emails based on structured, frequency-based features.

PROJECT OBJECTIVES
-----------------------------------------------------------------------------
- Load and explore the Spambase dataset programmatically using kagglehub.
- Perform comprehensive data preprocessing and feature scaling.
- Train multiple Machine Learning classification models for benchmarking.
- Compare model performance using Accuracy Scores and Classification Reports.
- Save all trained models and preprocessing objects for future deployment and testing.

DATASET INFORMATION
-----------------------------------------------------------------------------
- Source: Kaggle
- Dataset Name: Spambase (Original source: UCI Machine Learning Repository)
- Features: 57 continuous features
- Target: Binary (0 = Not Spam, 1 = Spam)

Dataset Characteristics:
The dataset relies on structured text characteristics rather than raw text, including:
- Word frequency features: e.g., "free", "money", "credit"
- Character frequency features: e.g., !, $, #
- Capital letter run-length statistics: Average, longest, and total run lengths.

FEATURE ENGINEERING & PREPROCESSING
-----------------------------------------------------------------------------
These features are crucial for capturing common spam patterns, such as excessive promotional words, aggressive punctuation, and abnormal capitalization.

Data Preprocessing Pipeline:
1. Train-Test Split: 80% Training Data / 20% Testing Data (random_state = 42 for reproducibility).
2. Feature Scaling: Applied MinMaxScaler to normalize all continuous features into a [0, 1] range, ensuring distance-based algorithms perform optimally.

MODEL EXPERIMENTS & EVALUATION
-----------------------------------------------------------------------------
The following models were trained using the exact same scaled dataset to ensure a fair and rigorous benchmark:
- Logistic Regression
- Random Forest
- XGBoost
- Support Vector Machine (SVM)
- Decision Tree
- K-Nearest Neighbors (KNN)
- Gradient Boosting
- AdaBoost
- Naive Bayes
- MLP Neural Network

Evaluation Metrics: Models are ranked primarily based on Accuracy Score, supplemented by the Classification Report (Precision, Recall, F1-Score) to handle any class imbalances.

MODEL SAVING & DEPLOYMENT
-----------------------------------------------------------------------------
All trained models are serialized and saved in the saved_models/ directory using the .joblib format (Scikit-learn compatible). 
- [model_name].joblib (Trained classifiers)
- scaler.joblib (MinMaxScaler object)

This approach ensures seamless deployment, strict reproducibility, and easy future inference testing.

PIPELINE OVERVIEW
-----------------------------------------------------------------------------
Dataset Download -> Data Exploration -> Train-Test Split -> Feature Scaling -> Model Training -> Accuracy Evaluation -> Model Saving

INSTALLATION & HOW TO RUN
-----------------------------------------------------------------------------
1. Clone the repository:
   git clone https://github.com/YOUR_USERNAME/spam-email-classification.git
   cd spam-email-classification

2. Install required dependencies:
   pip install -r requirements.txt

3. Run the Notebook/Script:
   Execute the main Python script or open the Jupyter Notebook to start the training and benchmarking process.

Main libraries used: pandas, scikit-learn, xgboost, kagglehub, joblib

KEYWORDS
-----------------------------------------------------------------------------
Supervised Learning | Spam Detection Systems | Model Benchmarking | Ensemble Learning | Classification Optimization | Machine Learning Deployment | Python
