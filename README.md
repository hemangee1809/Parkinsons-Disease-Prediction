# Parkinson's Disease Predictionan 

end-to-end machine learning pipeline built to predict the health status of subjects using biomedical voice measurements. This project evaluates and benchmarks multiple classification algorithms to accurately detect Parkinson's disease based on vocal frequencies, amplitude variations, and nonlinear dynamical complexity measures.  

** Project Overview **

Vocal impairment is one of the earliest signs of Parkinson's disease. This project demonstrates a structured data science workflow, utilizing automated Exploratory Data Analysis (EDA), data cleaning, feature visualization, multi-model benchmarking, and final model serialization for production-ready inference.

** Key Technical Achievements **

Automated Data Profiling: Leveraged ydata-profiling to generate high-level data summaries and distribution reports.

Feature Correlation Mapping: Built custom visualization heatmaps to evaluate the collinearity of multi-frequency voice metrics.

6-Classifier Benchmarking: Implemented, optimized, and compared Logistic Regression, Random Forest, Decision Tree, Naïve Bayes, KNN, and SVM.

Medical Domain Metrics: Evaluated models using Recall (to minimize false negatives in diagnosis) and Cohen's Kappa Score (to verify predictive agreement beyond pure chance).

Model Pipeline Serialization: Saved the trained production model into a pickle (.pkl) format for easy deployment and direct script inference.

** Dataset & Attribute Information **

The pipeline utilizes the parkinsons.data file, where the target label is status:

1 — Subject has Parkinson's disease

0 — Healthy subject

** Attribute Definitions **

name - ASCII subject name and recording number (dropped during preprocessing)

MDVP:Fo(Hz) - Average vocal fundamental frequency

MDVP:Fhi(Hz) - Maximum vocal fundamental frequency

MDVP:Flo(Hz) - Minimum vocal fundamental frequency

MDVP:Jitter(%), MDVP:Jitter(Abs), MDVP:RAP, MDVP:PPQ, Jitter:DDP - Frequency variations

MDVP:Shimmer, MDVP:Shimmer(dB), Shimmer:APQ3, Shimmer:APQ5, MDVP:APQ, Shimmer:DDA - Amplitude variations

NHR, HNR - Noise-to-tonal component ratios in the voice

RPDE, D2 - Nonlinear dynamical complexity measures

DFA - Signal fractal scaling exponent

spread1, spread2, PPE - Nonlinear variations in fundamental frequency

** Tech Stack & Libraries **

Language:PythonData
Manipulation: Pandas, NumPyData 
Profiling: ydata-profiling (formerly pandas-profiling) 
Data Visualization: Matplotlib, Seaborn
Machine Learning Framework: Scikit-LearnModel
Persistence: Pickle

** How To Run This Project **
1. Clone the Repository
   git clone https://github.com/your-username/Parkinsons-Disease-Prediction.git
   cd Parkinsons-Disease-Prediction
   
2. Install Dependencies
   pip install ydata-profiling matplotlib seaborn scikit-learn
   
3. Execution Pipeline
Open the project file inside a Jupyter Notebook or execution environment and run the segments sequentially

4. Direct Model Inference (Production Testing)
You can instantly load the saved production model (deploy_SVM.pkl) to make diagnostic predictions on a dataset without running the entire training script again
