# MNIST Digit Classification

This repository contains code for digit classification on the MNIST dataset using various neural network architectures with TensorFlow and Keras. The models include a basic artificial neural network (ANN) and a more complex deep neural network (DNN) with batch normalization. Hyperparameter tuning is also performed using Keras Tuner.

## Data

The MNIST dataset consists of 60,000 training images and 10,000 test images of handwritten digits (0-9). The images are 28x28 pixels in size.

## Model Architectures

### Basic ANN

A simple artificial neural network with the following architecture:
- **Input Layer**: Flatten (28x28)
- **Hidden Layer**: Dense(128, activation='relu')
- **Output Layer**: Dense(10, activation='softmax')

### Complex DNN with Batch Normalization

A deeper neural network with batch normalization layers:
- **Input Layer**: Flatten (28x28)
- **Hidden Layers**:
  - Dense(128, activation='relu')
  - BatchNormalization()
  - Dense(128, activation='relu')
  - BatchNormalization()
  - Dense(64, activation='relu')
  - BatchNormalization()
  - Dense(64, activation='relu')
  - BatchNormalization()
- **Output Layer**: Dense(10, activation='softmax')

### Hyperparameter Tuning

The `ann` function in `mnist_classification.py` uses Keras Tuner to search for the best hyperparameters. The tuning includes:
- Number of layers
- Number of units per layer
- Activation functions
- Dropout rates
- Optimizers

## Training

1. Load and preprocess the MNIST dataset.
2. Build and train the models using the ANN and DNN architectures.
3. Perform hyperparameter tuning using Keras Tuner.
4. Save the best model and visualize predictions.

## Results

- The basic ANN achieved a validation accuracy of approximately 98.02%.
- The more complex DNN with batch normalization achieved around 97.96%.
- Hyperparameter tuning found a model with a validation accuracy of 97.6%.

## Visualizations

Sample predictions on test images are visualized in the script output.

## Feedback and Contributions

Feel free to provide feedback or contribute to this project. If you have suggestions for improvements or additional features, your contributions are welcome!

[View the LinkedIn post for video demo](https://www.linkedin.com/posts/kaibalyamohapatra_machinelearning-deeplearning-ai-activity-7224613029596819456-KyBd?utm_source=share&utm_medium=member_desktop)
