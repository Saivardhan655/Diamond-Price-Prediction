# Diamond Price Prediction

This project aims to predict the price of diamonds based on various features using machine learning models. The best performing regression model is selected for the prediction.

## Directory Structure
[web page]([web page url](http://diamond-price-prediction-env.eba-c3mqskt5.eu-north-1.elasticbeanstalk.com/))

## Project Components

- **data/**: Contains the raw, training, and testing datasets.
- **notebooks/**: Contains Jupyter notebooks for Exploratory Data Analysis (EDA) and model training.
- **src/**: Contains the source code for the project.
  - **components/**: Modules related to different components of the project.
  - **pipelines/**: Contains pipeline scripts for data ingestion, transformation, and prediction.
  - **exception.py**: Custom exceptions for the project.
  - **logger.py**: Logging setup for the project.
  - **utils.py**: Utility functions used across the project.
- **templates/**: HTML templates for the Flask web application.
  - **form.html**: The form for inputting diamond features.
  - **index.html**: The home page with a button to navigate to the prediction form.
- **application.py**: The main Flask application.
- **requirements.txt**: Python dependencies required for the project.
- **setup.py**: Setup script for the project.
- **.ebextensions/**: Configuration files for deploying the project on AWS Elastic Beanstalk.

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/diamond-price-prediction.git
cd diamond-price-prediction

python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python application.py
```
### 2.Deployment on AWS Elastic Beanstalk
```bash
eb init -p python-3.8 diamond-price-prediction --region <your-region>
eb create diamond-price-prediction-env
eb deploy
eb open
