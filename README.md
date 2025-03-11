#Day-Ahead Electricity Price Prediction

Overview

This repository contains a script for predicting day-ahead electricity prices using historical and predicted data. The prediction model is based on machine learning techniques and requires several input datasets.

Data Requirements

The script requires the following data files:

Actual Consumption 2015-2024-to dec 7 -11PM.xlsx - Historical electricity consumption data.

Actual Generation 2015-2024-to dec 7 -11PM.xlsx - Historical electricity generation data.

Weather_Data_2015_2024-to dec 7 -11PM.xlsx - Historical weather data.

Price_2015_2024-to dec 7 -11__ADDED MISSING PRICES PM.xlsx - Historical electricity prices.

Manual_Features.xlsx - Predicted data for electricity generation, consumption, and weather for the target prediction day (to be manually prepared for now).

Installation

Ensure you have the required Python libraries installed:
pip install xgboost scikit-learn matplotlib pandas numpy openpyxl

Usage

Step 1: Update File Paths

Open electricity_prediction.ipynb.

In CELL 2, update the data_dir variable with the path where the dataset files are stored.

Example:
data_dir = "path/to/your/dataset/files"

Step 2: Preprocess and Merge Data

Run CELL 4 to preprocess and merge all historical datasets into a single file.

Update merged_file_path for the output location.

Example:
merged_file_path = 'path/to/output/merged_data.xlsx'



Step 3: Prepare Manual Features

In CELL 9, update the path to the manually prepared Manual_Features.xlsx file.

Define the prediction date in the prediction_start_date variable.

Example:
manual_features_path = '/home/Desktop/Manual_Features.xlsx'
prediction_start_date = datetime(2025, 2, 18)

Step 4: Save Predictions

In CELL 10, specify the output path for the predicted prices.
csv_filename = "/home/Desktop/DS/Predicted_Prices_Feb_13_2025.csv"

Step 5: Run the Script

Execute each cell in order to preprocess data, generate features, train the model, and save the predicted prices.

Future Improvements
