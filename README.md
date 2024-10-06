**Brain Tumor Detection Using Deep Learning and Model Orchestration with MLflow**
Project Overview
This project aims to build a deep learning-based model for detecting brain tumors from MRI and CT images. Using Convolutional Neural Networks (CNNs), the model classifies brain scans as tumor or non-tumor. The project also integrates MLflow for efficient tracking and management of experiments, including logging metrics, visualizations, and model versions.

Key Features:
Deep Learning with CNN: A CNN model is trained to detect brain tumors from MRI/CT images.
MLflow Integration: MLflow is used for model orchestration, making it easy to manage and track various experiments, hyperparameters, and model versions.
Streamlit Web App: A simple web interface is provided using Streamlit, where users can upload images for tumor detection and view model predictions.
Modular Code Structure: The project follows the cookiecutter data science template, which ensures scalability and ease of collaboration.
Reports & Visualization: Generates comprehensive reports and visualizations, helping users understand model performance.
Project Structure

    ├── LICENSE
    ├── Makefile           <- Commands to automate tasks such as `make train` and `make data`.
    ├── README.md          <- You are reading this file.
    ├── data
    │   ├── external       <- Data from third-party sources.
    │   ├── interim        <- Intermediate transformed data.
    │   ├── processed      <- Final datasets for model training and testing.
    │   └── raw            <- Raw MRI/CT image data.
    │
    ├── docs               <- Project documentation.
    │
    ├── models             <- Trained models and model outputs.
    │
    ├── notebooks          <- Jupyter notebooks for exploration and analysis.
    │
    ├── references         <- External references such as papers and manuals.
    │
    ├── reports            <- Generated reports and visualizations.
    │   └── figures        <- Generated graphics.
    │
    ├── requirements.txt   <- Python package dependencies.
    │
    ├── setup.py           <- Makes the project pip-installable.
    ├── src                <- Source code for the project.
    │   ├── __init__.py    <- Makes src a Python module.
    │   ├── data           <- Scripts for data loading and processing.
    │   ├── features       <- Scripts for feature engineering.
    │   ├── models         <- Scripts for model training and prediction.
    │   └── visualization  <- Scripts for generating visualizations.
    │
    └── tox.ini            <- Configuration for running tests.
Getting Started
Prerequisites
Python 3.7+
Libraries listed in requirements.txt
Streamlit and MLflow for running the web app and managing experiments.
Installation
Clone the repository:

git clone use URL
cd brain-tumor-detection
Install dependencies:


pip install -r requirements.txt
Ensure the data is placed in the data/raw folder or update src/data/make_dataset.py to fetch the dataset.

Usage
1. Train the Model
You can train the model by running the following command:

bash
Copy code
python src/models/train_model.py
This will preprocess the data, train the CNN model, and log the results with MLflow.

2. Run the Streamlit App
To run the web app locally and test the model, use the following command:

streamlit run app/app.py
This will launch a browser interface where you can upload MRI/CT images and view predictions.

3. Use MLflow for Tracking
MLflow is integrated to track experiments. Start the MLflow UI with:


mlflow ui
Navigate to http://localhost:5000 to view logged experiments, parameters, and models.

Project Workflow
Data Loading & Preprocessing: Raw MRI/CT images are loaded and preprocessed for training.
Model Training: A Convolutional Neural Network (CNN) is used for classification of brain tumor images.
Model Orchestration: MLflow is used to track experiments, log model versions, and monitor performance.
Web App Interface: A simple interface using Streamlit allows users to upload images and get real-time predictions.
Future Enhancements
Implement transfer learning to improve model accuracy.
Expand the dataset to include more diverse image samples.
Improve the web interface with more functionalities.
Diagram
![image](https://github.com/user-attachments/assets/93fe5e62-7491-4a10-a582-4a9312757124)

Tumors types:
![image](https://github.com/user-attachments/assets/40e45a71-a0e8-467e-b815-66b761f3bc0d)

Screenshot:
![Screenshot 2024-05-07 141513](https://github.com/user-attachments/assets/74ab952d-aea3-46bd-ba71-1abb29a96d9b)

![Screenshot 2024-05-07 141858](https://github.com/user-attachments/assets/01a43073-6aca-43b0-8191-ba6ef226f2e8)

![Screenshot 2024-05-07 142105](https://github.com/user-attachments/assets/8a179141-8d78-45e1-b3fe-f1c696908033)

![Screenshot 2024-06-02 220502](https://github.com/user-attachments/assets/ed8cfca6-df1f-4f07-934f-ad14911cb4f2)



License
This project is licensed under the MIT License - see the LICENSE file for details.
