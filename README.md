# Udacity-MLOps-Nanodegree-Projects
An overview of my submitted projects for Udacity's MLOps Nanodegree.

## Developed 4  Projects for Udacity's Machine Learning DevOps Nanodegree 

### Project 1: Predict Customer Churn with Clean Code [repo](https://github.com/ibrahim-sheriff/Predict-Customer-Churn-with-Clean-Code)

Implemented a machine learning model to identify credit card customers that are most likely to churn.  The project was focused mainly on refactoring existing notebook to follow best practices.

- The goal was to refactor to use clean code which includes
	- Writing clean, efficient and modular code
	- Writing documentation (docstrings and readme)
	- PEP8 style coding and linting using autopep8 and pylint
- Refactored to be production ready which includes
	- Cating errors (exception handling)
	- Code testing
	- Adding logging messages
- Learned how to use git and github from CLI and website
- Tools used: scikit-learn, matplotlib, seaborn, shap, autopep8, pylint, logging, git

### Project 2: Build a ML Pipeline for Short term Rental Prices in NYC [repo](https://github.com/ibrahim-sheriff/Build-a-ML-Pipeline-for-Short-term-Rental-Prices-in-NYC)

Working in a property management company for renting rooms and properties for short periods of time. Implement a ML model to estimate the price for a given property based on the price of similar properties.  The company receives new data in bulk every week. 

- Implement a clean, organized, reproducible, end-to-end machine learning pipeline
- Versioning data and artifacts (csv file, models) using Weights and biases
- Tracking experiments which includes pipelines, metrics and plots using Weights and Biases
- Building pipeline components in MLflow project where each component is in its own isolated environment
- Hydra and a config file was used to handle the many parameters of a ML pipeline
- Hydra sweeps used to perform for hyperparameters optimization
- Pytest was used to run determinstic and non-determinstic tests on data
- Using sklearn pipeline and Column transformer to build a pipeline model with feature preprocessing
- Using MLflow models to save the sklearn pipeline model
- Releasing the project on github using semantic version numbering
- Pipeline components includes
	- Data Collection
	- EDA
	- Data Cleaning and feature engineering
	- Data Segregation
	- Data validation for testing data 
	- Model training
	- Model validation
- Tools: mlflow, pytest, wandb, scikit-learn, pandas, hydra

### Project 3: Deploying a ML Model on Heroku with FastAPI [repo](https://github.com/ibrahim-sheriff/Deploying-a-ML-Model-on-Heroku-with-FastAPI)

Develop a classification model on publicly available Census Bureau data and deploying
the model using FastAPI and Heroku. 

- Train a simple ml model using scikiet learn
- Preparing model for production by evaluating on data and slices of data 
- Created a model card for the trained pipeline model
- Version control data and models using DVC with remote storage to AWS S3 bucket
- Testing data using great_expectations
- Testing API using FastAPI testclient
- Testing model and training 
- Running testing functions using pytest with a conftest file
- Deployed the model as an API using FastAPI with type hinting support
- Added examples to the FastAPI app documentation
- Implemented Continous integration using github actios that runs:
	- flake8 for linting
	- AWS credentials configuration
	- Pulling latest data and models using DVC
	- pytest for testing
- Implemented Continous deployment using Heroku
- Tools used: fastAPI, dvc, s3, github actions, Heroku, pytest, great_expectations, flake8

### Project 4: Dynamic Risk Assessment System [repo](https://github.com/ibrahim-sheriff/Dynamic-Risk-Assessment-System)

The company needs you to create, deploy, and monitor a risk assessment ML model that will estimate the 
attrition risk of each of the company's customers.

The following steps was implemented
- Data ingestion automatically check for new data that can be used for model training
- Compile all training data to a training dataset and save it 
- Write metrics related to the completed data ingestion tasks and save it
- Training a logistic regression model using scikit learn to predict attrition risk
- Scoring and saving the model metrics
- Deploying the model using a simple simulation of production environment
- Diagnostics 
	- Determine and save summary statistics related to a dataset
	- Determine missing percentage
	- Time the performance of data ingestion and model training steps
	- Check for dependency changes and package updates using pip-outdated
- Automatic reporting 
	- Generate a confusion matrix plot for the model
	- Generate a PDF document that report on model metrics, summary statistics, missing percentage, performance and dependency changes using reportlab
- Provide an API endpoint for scoring and diagnostics
- Process Automation create a script and cron job that automatically run all previous steps at regular intervals if model drift is detected
- Tools used: scikit-learn, pandas, flask, reportlab, cronjob
