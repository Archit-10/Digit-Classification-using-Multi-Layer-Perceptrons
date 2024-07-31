# Digit-Classification-using-MLP

This project involves performing digit classification using a Multi-layer Perceptron (MLP). The MLPClassifier from sklearn is used to train the model and evaluate its performance on the provided datasets.
Dataset

The dataset contains images of digits for training and testing purposes. The images are in grayscale and the task is to classify each image into one of the 10 digit classes (0-9). The datasets can be downloaded from here.
Steps to Complete the Project
1. Load Dataset

    Data Loading: Load the training and test sets from the provided files. Ensure the data is in a format suitable for training the MLP model.

2. Train MLP Model

    Model Training: Use the MLPClassifier from sklearn to train the model on the training set.
    Hyperparameter Tuning: Explore different hyperparameters (e.g., number of hidden layers, number of neurons, activation functions) to optimize model performance.

3. Evaluate Model

    Accuracy: Report the accuracy of the model on the test sets.
    Other Metrics: Evaluate other interesting metrics such as precision, recall, F1 score, and confusion matrix.
    Observations: Report any interesting observations based on the evaluation metrics.

Prerequisites

    Python 3.x
    Required Libraries: numpy, pandas, scikit-learn, matplotlib

Instructions

    Clone the Repository:

    sh

git clone <repository_url>
cd <repository_directory>

Install Dependencies:

sh

pip install -r requirements.txt

Download Dataset:

    Download the training and test datasets from the provided link and place them in the data directory.

Run Data Loading and Preprocessing:

    Load and preprocess the dataset.

sh

python data_preprocessing.py

Train MLP Model:

    Train the MLP model using the training set.

sh

python train_mlp.py

Evaluate Model:

    Evaluate the model's performance on the test sets and report accuracy and other metrics.

sh

python evaluate_model.py


Conclusion

This project demonstrates the implementation of a digit classification system using Multi-layer Perceptrons (MLP). By training and evaluating the MLP model on the provided datasets, we can classify digit images with high accuracy.
