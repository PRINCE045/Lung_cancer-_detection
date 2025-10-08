Lung Cancer Detection Analysis
This repository contains a data analysis and machine learning project focused on predicting Lung Cancer based on a survey dataset of various symptoms and risk factors.

🚀 Project Overview
The goal of this project is to explore a dataset related to lung cancer, perform data preprocessing, visualize relationships between features, and build a classification model to predict the presence of lung cancer.

The primary steps involved are:


Data Loading and Exploration: Understanding the structure and initial characteristics of the dataset .




Data Preprocessing: Handling categorical features (like 'GENDER' and 'LUNG_CANCER') using Label Encoding and scaling numerical features using StandardScaler .



Exploratory Data Analysis (EDA): Visualizing feature distributions and correlations .






Model Training: Training a Logistic Regression and a Support Vector Classifier (SVC) model .




Model Evaluation: Assessing model performance using key classification metrics (Accuracy, Precision, Recall, F1-score) and a Confusion Matrix .





💾 Dataset Details
The dataset contains 309 entries and 16 columns.


Features
The dataset includes the following columns:





Column Name	Data Type	Non-Null Count
GENDER	object (later encoded to int64)	
309 

AGE	int64	
309 

SMOKING	int64	
309 

YELLOW FINGERS	int64	
309 

ANXIETY	int64	
309 

PEER PRESSURE	int64	
309 

CHRONIC DISEASE	int64	
309 

FATIGUE	int64	
309 

ALLERGY	int64	
309 

WHEEZING	int64	
309 

ALCOHOL CONSUMING	int64	
309 

COUGHING	int64	
309 

SHORTNESS OF BREATH	int64	
309 

SWALLOWING DIFFICULTY	int64	
309 

CHEST PAIN	int64	
309 

LUNG CANCER	object (Target, later encoded to int64)	
309 


Export to Sheets
🛠️ Setup and Dependencies
This project requires Python and the following libraries:

pandas

matplotlib

seaborn

scikit-learn (sklearn)

You can install the necessary packages using pip:

Bash

pip install pandas scikit-learn matplotlib seaborn
📊 Exploratory Data Analysis (EDA)
Key steps in the EDA included:

Target Imbalance: A countplot showed a higher count for LUNG_CANCER=1 compared to LUNG_CANCER=0.


Age Distribution: The age distribution was visualized using a histogram.



Correlation Heatmap: A correlation heatmap of numerical features was generated.

🧠 Machine Learning Models and Results
The dataset was split into training and testing sets with a test_size of approximately 20% (X_train shape: (247, 15), X_test shape: (62, 15)) .

1. Logistic Regression
The model was trained on scaled features (X_train_scaled, X_test_scaled) .

Metric	Score
Accuracy	
0.9677 


Precision	
0.9833 


Recall	
0.9833 

F1-score	
0.9833 


Export to Sheets
2. Support Vector Classifier (SVC)
The SVC model was trained and evaluated .

SVC Performance Scores

Test Score (Accuracy): 96.77% 



Train Score: 85.02% 


Confusion Matrix (SVC)
The confusion matrix on the test set was:


( 
0
0
​
  
2
60
​
 )




True Negatives (No Cancer, Predicted No): 0 



False Positives (No Cancer, Predicted Yes): 2 



False Negatives (Cancer, Predicted No): 0 



True Positives (Cancer, Predicted Yes): 60 


Classification Report (SVC)
Class	Precision	Recall	F1-Score	Support
0 (No Cancer)	
0.00 


0.00 


0.00 


2 

1 (Cancer)	
0.97 


1.00 


0.98 


60 


Accuracy	-	-	
0.97 


62 



Export to Sheets

