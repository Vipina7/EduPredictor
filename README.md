# EduPredict: Student Performance Predictor

EduPredict is a Flask-based web application designed to predict the math scores of students based on demographic and socio-economic data. This project focuses on understanding and analyzing factors influencing academic performance.

The application is built on a machine learning pipeline, enabling accurate predictions and providing insights into how different variables affect student outcomes.
## Project Structure

The project is organized as follows:

```
Math Score Predictor/
|
|-- src/
|   |-- components/
|   |   |-- data_loader.py        # Script for loading and preparing data
|   |   |-- model_trainer.py      # Script for training the model
|   |   `-- prediction.py         # Script for making predictions
|   |
|   |-- utils.py                  # Utility functions
|   |
|-- templates/
|   |-- home.html                 # Frontend template for user interface
|
|-- app.py                        # Main script to run the web app
|-- requirements.txt              # Required Python dependencies
|-- README.md                     # Project documentation (this file)
|-- model.pkl                     # Pre-trained machine learning model
|
`-- data/
    |-- dataset.csv               # Dataset used for training
    `-- sample_input.csv          # Sample input for predictions
```
## Dataset
The model was trained on a publicly available dataset that contains information about students' scores in math, reading, and writing, along with demographic and socio-economic attributes.

Attributes Used:
- Gender
- Race/Ethnicity
- Parental Education Level
- Lunch Type
- Test Preparation Status

Target Variable:
- Math Score

## Technology Stack

Backend: Flask (Python)
Frontend: HTML
Machine Learning: Scikit-learn, Pandas, NumPy, Pickle
Model Evaluation: Cross-validation, GridSearchCV
Environment: Virtual Environment (venv), pip
Version Control: Git, GitHub

## Features

- **Data Loading and Cleaning:** Handles raw data and prepares it for model training.
- **Model Training:** Trains a machine learning model to predict math scores using linear regression.
- **Prediction Interface:** Provides a simple interface to make predictions based on new input data.
- **Deployment Ready:** Includes a Flask app for local deployment of the model.

## Machine Learning Models Evaluated
Several regression models were tested to identify the best-performing model:

**Linear Regression**
- Simple and interpretable.
- Performed adequately but showed higher mean squared error compared to other models.
  
**Decision Tree Regressor**
- Capable of capturing non-linear relationships.
- Tended to overfit the data.

**Random Forest Regressor**
- Robust and less prone to overfitting.
- Achieved high accuracy with moderate computational cost.

**Gradient Boosting Regressor**
- Offered superior performance with optimal hyperparameter tuning.
- Selected as the **final model** for its balance of accuracy and generalizability.

**CatBoost Regressor**
- Specialized for categorical data handling.
- Performed well but had higher computational costs compared to Gradient Boosting.

**AdaBoost Regressor**
- Combined multiple weak learners to improve accuracy.
- Results were good but slightly less consistent than Gradient Boosting.

## How to Use

### Prerequisites
Ensure you have the following installed:
- Python 3.8+
- pip (Python package installer)

### Running the Application
To start the Flask app:
```bash
python app.py
```
This will launch the application on `http://127.0.0.1:5000`. You can use the web interface to input data and see predictions.
