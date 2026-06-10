# Student Performance Indicator

A Flask-based machine learning web app that predicts a student's math score from exam and background details such as reading score, writing score, gender, lunch type, parental education level, and test preparation status.

## Live Demo

[Open the deployed app](https://student-performance-project-irol.onrender.com)

## Project Overview

This project is an end-to-end machine learning pipeline built around the Student Performance dataset. It includes data ingestion, preprocessing, model training, prediction logic, and a deployed web interface.

The app takes user input from a form, transforms the data using a saved preprocessing pipeline, loads the trained model, and returns the predicted math score.

## Features

- Student math score prediction through a web form
- Flask web application
- Data ingestion and train-test split pipeline
- Data preprocessing with scikit-learn pipelines
- Trained model and preprocessor saved as pickle artifacts
- Render deployment configuration

## Tech Stack

- Python
- Flask
- pandas
- NumPy
- scikit-learn
- CatBoost
- XGBoost
- dill
- Gunicorn
- Render

## Project Structure

```txt
.
├── app.py
├── artifacts/
│   ├── model.pkl
│   └── preprocessor.pkl
├── notebook/
│   └── data/
├── src/
│   ├── components/
│   │   ├── data_ingestion.py
│   │   ├── data_transformation.py
│   │   └── model_trainer.py
│   ├── pipeline/
│   │   └── predict_pipeline.py
│   ├── exception.py
│   ├── logger.py
│   └── utils.py
├── templates/
│   ├── home.html
│   └── index.html
├── render.yaml
├── requirements.txt
└── setup.py
```

## Run Locally

Clone the repository:

```bash
git clone https://github.com/Kushagra976/mlproject.git
cd mlproject
```

Create and activate a virtual environment:

```bash
python -m venv venv
venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the Flask app:

```bash
python app.py
```

Open the app in your browser:

```txt
http://localhost:5000
```

## Deployment

This project is deployed on Render using Gunicorn.

Render settings:

```txt
Build Command: pip install -r requirements.txt
Start Command: gunicorn app:app
```

The deployment configuration is also included in `render.yaml`.

## Author

Kushagra Gaur
