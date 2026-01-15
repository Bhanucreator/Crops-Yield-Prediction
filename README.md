# Crop Yield Prediction

This project is a machine learning application that predicts crop yield quality. The prediction is categorized into four classes: "Poor", "Average", "Good", and "Very Good". The model is trained on a dataset containing information about the state, season, crop type, area, and rainfall.

## Project Structure

```
CropYieldPredictor/
|-- CropYield_prediction.ipynb
|-- Dataset.csv
|-- Inference File.ipynb
|-- model/
|   |-- crop_labels.pkl
|   |-- KNeighborsClassifier_model.pkl
|   |-- season_labels.pkl
|   |-- state_labels.pkl
|-- README.md
```

## How It Works

### 1. Data Preprocessing and Feature Engineering
- The `CropYield_prediction.ipynb` notebook loads the `Dataset.csv` file.
- It cleans the data and performs label encoding on categorical features like `State`, `Season`, and `Crop`. The label mappings are saved as `.pkl` files in the `model/` directory.

### 2. Model Training
- The notebook uses K-Means clustering to create yield quality labels (Poor, Average, Good, Very Good).
- A K-Nearest Neighbors (KNN) classifier is trained on the preprocessed data to predict these labels.
- The trained KNN model is saved as `KNeighborsClassifier_model.pkl` in the `model/` directory.

### 3. Inference
- The `Inference File.ipynb` notebook is used for prediction.
- It loads the saved model and label encoders.
- It takes user input for `State`, `Season`, `Crop`, `Area`, and `Rainfall`.
- It preprocesses the input and uses the trained model to predict the crop yield quality.

## How to Use

1.  **Run the training notebook:**
    Open and run the `CropYield_prediction.ipynb` notebook to train the model and generate the necessary model files.

2.  **Run the inference notebook:**
    Open and run the `Inference File.ipynb` notebook. You will be prompted to enter the required details to get a prediction.

## Models
- **K-Means Clustering**: Used to generate the target labels for the classification task.
- **K-Nearest Neighbors (KNN)**: The final classification model used for prediction.
