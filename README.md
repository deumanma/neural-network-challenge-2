# Overview
This project uses a neural network model to predict employee attrition and department classification based on various employee characteristics. The model processes employee data from a CSV file, applies preprocessing techniques like scaling and encoding, and then trains a neural network to make predictions.


## Getting Started
### Prerequisites

Python 3.x
Pandas
NumPy
Scikit-Learn
TensorFlow
Pillow (optional, if image processing is needed)

## Data
The data used in this project is sourced from a publicly available CSV file containing employee attrition data. It includes various attributes such as age, education, job satisfaction, and others that influence attrition and department classification.

## Model Details
### Architecture
The model uses a functional API to create a multi-output model:

Input Layer: Takes input with 10 features corresponding to the employee attributes.
Shared Layers: Two dense layers shared between two branches of the output.
Department Branch: Predicts the department of the employee.
Attrition Branch: Predicts if an employee will leave the company.

## Compilation
The model is compiled with the Adam optimizer and uses categorical crossentropy as the loss function for both outputs. Accuracy is tracked as a metric.

## Training
The model is trained over 10 epochs with a batch size of 32 and validates on 20% of the training data.

## Results
After training, the model provides accuracy metrics for both outputs, which can be reviewed to assess performance.

## Discussion
Accuracy Metric: The choice of accuracy as a metric is discussed, considering its implications for both binary and multi-class classification problems.
Activation Functions: Sigmoid activation is used for binary classification, and softmax is used for multi-class classification to output probabilities.
