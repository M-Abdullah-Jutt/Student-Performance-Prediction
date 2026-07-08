# Student Performance Prediction

A Machine Learning web application that predicts a student's math score based on their demographic information and academic background.

## 🌟 Overview

This project uses a trained machine learning model to forecast academic success. Users can input a student's gender, ethnicity, parental education level, lunch type, and test preparation course status to receive an instant score prediction. 

The application features a modern, glassmorphic UI and is fully integrated with a CI/CD pipeline for automated deployment to Azure App Service.

## 🚀 Technologies Used

- **Backend:** Python, Flask, Gunicorn
- **Machine Learning:** Scikit-Learn, CatBoost, XGBoost, Pandas, Numpy
- **Frontend:** HTML5, CSS3 (Custom Glassmorphism UI)
- **Deployment:** Azure App Service (Linux), GitHub Actions (CI/CD)

## 💻 Running Locally

### Prerequisites
- Python 3.9+ 
- pip (Python package manager)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/M-Abdullah-Jutt/Ml_Project.git
   cd Ml_Project
   ```

2. Create and activate a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   # On Windows:
   venv\Scripts\activate
   # On macOS/Linux:
   source venv/bin/activate
   ```

3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Run the Flask application:
   ```bash
   python app.py
   ```

5. Open your browser and navigate to:
   `http://127.0.0.1:5000`

## ☁️ Azure Deployment

This project is configured for continuous deployment using GitHub Actions. 

Any push to the `main` branch will automatically trigger the `.github/workflows/main_student-performance-prediction-3.yml` workflow, which:
1. Provisions a Python 3.11 environment.
2. Installs dependencies.
3. Zips the source code.
4. Deploys the artifact to Azure App Service using ZipDeploy.

*Note: The Azure App Service relies on Oryx to build the environment on the server side using the custom `startup.txt` command.*
