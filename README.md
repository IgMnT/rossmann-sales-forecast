# rossmann-prediction-app/rossmann-prediction-app/README.md

# Rossmann Prediction App

This project is a Flask application that predicts sales for Rossmann stores based on historical data and various features. It utilizes a pre-trained machine learning model to provide predictions through a Telegram bot interface.

## Project Structure

```
rossmann-prediction-app
├── rossmann
│   └── Rossmann.py
├── model
│   └── model_rossmann.pkl
├── parameter
│   ├── competition_distance_scaler.pkl
│   ├── competition_time_month_scaler.pkl
│   ├── promo_time_week_scaler.pkl
│   ├── store_type_scaler.pkl
│   └── year_scaler.pkl
├── handler.py
├── Procfile
├── requirements.txt
└── README.md
```

## Files Description

- **rossmann/Rossmann.py**: Contains the `Rossmann` class with methods for data cleaning, feature engineering, data preparation, and making predictions.
- **model/model_rossmann.pkl**: The serialized machine learning model used for making predictions.
- **parameter/**: Contains various scaler files used in data preparation.
- **handler.py**: Initializes the Flask application and defines the prediction endpoint.
- **Procfile**: Specifies the command to run the application on Railway.
- **requirements.txt**: Lists the dependencies required for the project.

## Setup Instructions

1. Clone the repository:
   ```
   git clone <repository-url>
   cd rossmann-prediction-app
   ```

2. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```

3. Run the application locally:
   ```
   python handler.py
   ```

## Deploying on Railway

To deploy this project on Railway, follow these steps:

1. Create a Railway account and log in.
2. Create a new project and select the option to deploy from a GitHub repository or upload your project files directly.
3. Ensure that your `requirements.txt` file is present to install the necessary dependencies.
4. Set the environment variables if needed (e.g., for any API keys).
5. Railway will automatically detect the `Procfile` and use it to start your application.
6. Once the deployment is complete, you will receive a URL to access your application.

## Usage

Once deployed, you can interact with the application through the Telegram bot. Send a message with the store ID to receive sales predictions for the next six weeks.