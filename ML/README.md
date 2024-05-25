# Event Classification Using Logistic Regression

## Overview

This project aims to classify event types based on various parameters such as region, date, actors involved, and fatalities. The dataset contains records of different events, and the goal is to predict the type of event (e.g., Shelling/artillery/missile attack, Air/drone strike) using logistic regression.

## Dataset

The dataset used in this project is `cleaned_data.csv`, which includes the following columns:

- `event_date`: Date of the event
- `region`: Region where the event occurred
- `actor1`: First actor involved in the event
- `actor2`: Second actor involved in the event
- `fatalities`: Number of fatalities
- `event_type`: Type of the event (target variable)

## Feature Engineering

The following steps were taken to preprocess the data:

- Converted `event_date` to datetime format and extracted day, month, and year.
- Encoded categorical variables `region`, `actor1`, and `actor2` using `LabelEncoder`.

## Model

A logistic regression model was used to classify the event types. The model was trained and tested on the dataset, and its performance was evaluated using various metrics.

## Installation

To run this project, ensure you have Python installed along with the following packages:

- pandas
- scikit-learn

These packages can be installed using pip.

## Usage

1. Load the data from `cleaned_data.csv`.
2. Perform feature extraction and encoding.
3. Select features and the target variable.
4. Split the data into training and test sets.
5. Train the logistic regression model on the training data.
6. Make predictions on the test data and evaluate the model's performance.

## Performance

The model achieved an accuracy of approximately 98.68%. However, other metrics such as precision, recall, and F1-score indicated varying performance across different event types:

- High precision and recall for "Explosions/Remote violence"
- Lower performance for "Riots" and "Violence against civilians"

## Conclusion

The model demonstrates strong predictive capability for certain event types but faces challenges with others. Further refinement and exploration of alternative approaches are recommended to improve overall performance.
