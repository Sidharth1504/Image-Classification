# Fashion MNIST Classification Project

## Overview
This project analyzes the Fashion MNIST dataset, a collection of 70,000 grayscale images of 10 different clothing categories. Each image is 28x28 pixels with pixel values ranging from 0 to 255. The project implements and compares multiple machine learning models for classifying these fashion items.

## Dataset

The Fashion MNIST dataset contains the following 10 categories:

* 0: T-shirt/top
* 1: Trouser
* 2: Pullover
* 3: Dress
* 4: Coat
* 5: Sandal
* 6: Shirt
* 7: Sneaker
* 8: Bag
* 9: Ankle boot

### Option 1: Automatic Download
Automatically download the dataset using TensorFlow.
```
tensorflow.keras.datasets.fashion_mnist.load_data()
```

### Option 2: Manual Download
1. Download the dataset from [Zalando Research](https://github.com/zalandoresearch/fashion-mnist)
2. Place the files in the `dataset/` directory:
   - `dataset/images-idx3-ubyte`
   - `dataset/labels-idx1-ubyte`


## Project Structure

IMAGE-CLASSIFICATION/
├── dataset/
│   ├── data.csv
│   ├── images-idx3-ubyte
│   └── labels-idx1-ubyte
├── fashion_mnist_CNN_model.h5
├── model.ipynb
└── README.md

## Features

* Data Loading: Support for both CSV and IDX file formats
* Exploratory Data Analysis: Visualization of the dataset with class distribution and pixel intensity analysis
* Multiple Models:

    * Logistic Regression (traditional ML approach)
    * Multilayer Perceptron (MLP)
    * Convolutional Neural Network (CNN)


* Model Evaluation: Comprehensive performance metrics including accuracy, confusion matrices, and classification reports
* Explainable AI: Feature importance visualization for the logistic regression model
* Visualization: Display of correctly and incorrectly classified images

## Requirements
* numpy
* pandas
* matplotlib
* seaborn
* scikit-learn
* tensorflow


## Model Performance
The project evaluates multiple models:

| Model  | Test Accuracy |
| ------------- | ------------- |
| Logistic Regression | ~85% |
| MLP | ~89% |
| CNN | ~91% |

The CNN model generally performs the best due to its ability to capture spatial patterns in the images.

## Results Visualization

* Confusion matrices show which classes are most commonly confused
* Side-by-side comparisons of correctly and incorrectly classified images
* Feature importance visualization highlights which pixels are most informative for classification

## Future Improvements

* Implement data augmentation to improve model generalization
* Try more advanced CNN architectures (ResNet, MobileNet)
* Add hyperparameter tuning using grid search or random search