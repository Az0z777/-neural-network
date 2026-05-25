# -neural-network
House Price Prediction using ANN (PyTorch)

Project Overview

This project uses an Artificial Neural Network (ANN) built with PyTorch to predict house prices using the California Housing dataset from Scikit-learn.

The model learns patterns from housing features such as:

Median Income

House Age

Average Rooms

Population

Latitude & Longitude


The project also compares different neural network configurations and visualizes training performance.


---

Technologies Used

Python

PyTorch

Scikit-learn

Matplotlib



---

Dataset

The project uses the California Housing dataset available in Scikit-learn.

Dataset Features:

MedInc → Median income

HouseAge → Average house age

AveRooms → Average rooms

AveBedrms → Average bedrooms

Population → Area population

AveOccup → Average occupancy

Latitude

Longitude


Target:

House Price



---

Project Workflow

1. Data Loading

The California Housing dataset is loaded using:

fetch_california_housing()


---

2. Data Preprocessing

Feature Scaling

The features are normalized using:

StandardScaler()

Why?

Neural networks perform better when values are on similar scales.

Helps faster and more stable training.



---

3. Converting to Tensors

The dataset is converted into PyTorch tensors:

torch.tensor()

Why?

PyTorch models work with tensors only.



---

4. Train/Test Split

The dataset is divided into:

80% Training Data

20% Testing Data


Using:

train_test_split()


---

Neural Network Architecture

The main model is:

HousePriceMLP

Architecture

Layer	Size

Input Layer	8 Features
Hidden Layer 1	64 Neurons
BatchNorm	64
Hidden Layer 2	32 Neurons
Output Layer	1 Neuron


Activation Function

ReLU


Regularization

Dropout (0.2)



---

Loss Function

The project uses:

MSELoss()

MSE = Mean Squared Error

Used because this is a regression problem.


---

Optimizer

The optimizer used is:

Adam

Learning Rate

lr = 0.001

Why Adam?

Fast convergence

Adaptive learning

Popular in deep learning



---

Training Process

The model is trained for:

100 Epochs


During training:

Forward propagation

Loss calculation

Backpropagation

Weight updates


Training and validation losses are stored for visualization.


---

Model Experiments

Experiment 1

Increased learning rate:


lr = 0.01

Purpose

Test faster learning.



---

Experiment 2

A second neural network uses:

Tanh activation function instead of ReLU.


Purpose

Compare activation functions.



---

Visualization

The project plots:

Training Loss

Validation Loss


Using:

matplotlib.pyplot

This helps monitor:

Learning progress

Overfitting

Model performance



---

Final Output

The project prints:

Final MSE

Predicted house prices

Actual house prices


Example

Predicted Price: 2.45
Actual Price : 2.39


---

Project Structure

project/
│
├── main.py
├── README.md
└── requirements.txt


---

Requirements

Install dependencies using:

pip install torch matplotlib scikit-learn


---

How to Run

Run the project using:

python main.py


---

Expected Results

After training:

Loss decreases gradually

Predictions become closer to actual prices

Graph shows learning behavior



---

Concepts Used

This project covers:

Artificial Neural Networks (ANN)

Forward Propagation

Backpropagation

Regression

Activation Functions

Batch Normalization

Dropout

Optimizers

Loss Functions



---

Future Improvements

Possible improvements:

Add more hidden layers

Use GPU training

Hyperparameter tuning

Save/load trained model

Add evaluation metrics like MAE and R²

