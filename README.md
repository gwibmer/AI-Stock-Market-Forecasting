# Stock Market Index Price Prediction

### Final Project for Introduction to Deep Learning Course at University of South Florida
### Team Members: Jun Kim, Gerardo Wibmer Gonzalez, Paul-Ann Francis, Tahsun Rahman Khan

## Overview
This project aims to predict the closing prices of stock market indices using deep learning models built with Python and TensorFlow. We have developed a two-model approach to achieve this goal. The first model (Model 1) predicts the closing price using four input features (Open, High, Low, and Volume) for a specific date. The second model (Model 2) predicts the future values of each feature based on their respective historical data. By combining the predictions from these two models, we can estimate the closing price for any given day.

Although our project focuses on predicting the S&P 500 index prices, the code can be easily modified to predict the prices of any stock.

## Data
The data used in this project consists of daily stock market index prices, including Open, High, Low, Close, and Volume. We have used the historical price data of the S&P 500 index, obtained from Yahoo Finance, to train, validate, and test our models.

## Approach
1. Preprocessing: The raw data is preprocessed to create a windowed dataset, which includes the necessary features and target variables.
2. Model Training: We train separate instances of Model 2 for each feature (Open, High, Low, and Volume) using their historical data. This results in four different models that predict future values for each feature. Then, we train Model 1 using the combined features from Model 2's predictions.
3. Hyperparameter Tuning: We used grid search to find the best hyperparameters for our models. The optimal hyperparameters and their corresponding performance metrics are stored in CSV files under the hyperparameters/ directory.
4. Prediction: We input the predicted values of Open, High, Low, and Volume from Model 2 into Model 1 to predict the closing price for any given day.

## Repository Structure
- models/: Contains the saved deep learning models (Model 1 and Model 2 instances) for each feature.
- hyperparameters/: Contains CSV files with the optimal hyperparameters and their corresponding performance metrics, obtained through grid search.
- notebooks/: Contains Jupyter notebooks for data preprocessing, model training, and evaluation.
- README.md: Provides an overview of the project, including the approach, data, and repository structure.

## Dependencies
- Python 3.8 or higher
- datetime
- matplotlib
- NumPy
- pandas
- scikit-learn
- TensorFlow
- Keras
- yfinance

## License
This project is licensed under the Apache License 2.0. See LICENSE file for details.