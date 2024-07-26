# CIFAR-10 Image Classification with Fastai

## Table of Contents
- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
  - [Extracting the Dataset](#extracting-the-dataset)
  - [Load the Dataset](#load-the-dataset)
  - [Training the Model](#training-the-model)
  - [Making Predictions](#making-predictions)
- [Model Comparison](#model-comparison)
- [Acknowledgments](#acknowledgments)

## Introduction
This project classifies images from the CIFAR-10 dataset using various models, including a CNN, ResNet50, and a fine-tuned ResNet152. The CIFAR-10 dataset consists of 60,000 32x32 color images across 10 different classes.

## Installation
To install and run this project, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/Amnaikram1/cifar10-image-classification.git
   cd cifar10-image-classification
   ```

## Usage

### Extracting the Dataset
To extract the training and test datasets, use the 7z archives:

- `extract_train.py`: Extracts the training dataset using the `py7zr` package.
- `extract_test.py`: Extracts the test dataset using the `py7zr` package.

### Load the Dataset
Data is loaded using the Data Loader script. 

#### Data Loader
A data loader specifically refers to an object that encapsulates the training, validation, and optionally test datasets in a format suitable for training deep learning models. It provides a high-level interface to specify:

- Data Source
- Data Augmentation
- Batching
- Normalization

### Training the Model
Train the model using Fastai by running the CNN learner script. This script defines the Image Data Loaders, creates a learner with a pre-trained ResNet152 model, and fine-tunes it.

### Making Predictions
To make predictions on the test set, use the `get_preds()` method of CNN learner. This function will load the trained model and generate predictions for the test images.

## Model Comparison
The accuracy of different models used in this project:

| Model                  | Accuracy (%) |
|------------------------|--------------|
| CNN                    | 28%          |
| ResNet50               | 46%          |
| ResNet152 (Fine-tuned) | 97%          |

## Acknowledgments
- The Fastai library and its contributors
- Kaggle for providing the CIFAR-10 dataset
- The open-source community for their invaluable contributions
```

Feel free to adjust further as needed!
