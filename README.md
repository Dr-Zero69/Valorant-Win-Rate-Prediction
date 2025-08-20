# Valorant-Win-Rate-Prediction
A machine learning project that analyzes player performance stats (KD, kills, deaths, assists, maps, agents) to predict win rate in Valorant.This project applies machine learning techniques to analyze player performance data (such as KD ratio, kills, deaths, assists, maps, and agents) in the game Valorant, with the goal of predicting a player’s win rate. The repository demonstrates the workflow from data preprocessing to model training, hyperparameter tuning, and evaluation.

Key Features
- Exploratory Data Analysis (EDA): Visualizations including bar plots, histograms, and correlation matrices to understand feature relationships.

- Feature Engineering: Handling categorical variables like agent names and map names.

- Modeling: Logistic Regression models (base and tuned) used for prediction.

- Hyperparameter Tuning: Comparison of base vs tuned models for performance improvement.

- Evaluation Metrics: Accuracy scores with clear visual comparisons.

Repository Structure

- Valorant_data_prediction_hyper_parameter.ipynb → Main notebook with EDA, preprocessing, modeling, and evaluation.

- README.md → Project documentation.


Installation & Requirements

- Clone the repository and install the required dependencies:

git clone https://github.com/Dr-Zero69/Valorant-Win-Rate-Prediction.git
cd Valorant-Win-Rate-Prediction

- Required libraries:
- numpy  
- pandas  
- matplotlib  
- seaborn  
- scikit-learn 


Results

The tuned Logistic Regression model achieved higher accuracy compared to the base model on both train and test sets.

Visualization shows that tuning improved performance by a noticeable margin.

Use Case

By analyzing performance metrics like kills, deaths, assists, and agent/map choices, this project highlights how data-driven insights can be applied to competitive gaming, helping players and analysts understand the factors influencing win rates.

Contributing

Contributions, issues, and feature requests are welcome. Feel free to fork the repo and submit a pull request :D
