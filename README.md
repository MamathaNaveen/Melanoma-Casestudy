# Project Name CNN Melanoma detection
Problem statement: To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.
The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

## General Information
The data set contains the following diseases:
Actinic keratosis
Basal cell carcinoma
Dermatofibroma
Melanoma
Nevus
Pigmented benign keratosis
Seborrheic keratosis
Squamous cell carcinoma
Vascular lesion

Technologies Used/Modules used for prediction:
import pathlib
import tensorflow as tf
import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import os
import PIL
from tensorflow import keras
from tensorflow.keras import layers
from tensorflow.keras.models import Sequential
from tensorflow.keras import datasets, layers, models
from tensorflow.keras.layers import Conv2D,MaxPooling2D,Flatten, Dense,Rescaling,Activation,BatchNormalization,Dropout,RandomFlip,RandomRotation
from tensorflow.keras.regularizers import l2

## Conclusions
##### **Final Observations:**
#### Numbers of Base Model with Batch Normalization,Drop and Regularization Rescaling:
 - Rescaling
 - Batch Normalization
 - Dropout - 0.15
 - Training Accuracy = 94%, Validation Accuracy = 46%
 - epochs = 20
 - L2 = 0.01
 - Batch_size = 32

#### Adding Rebalancing Dataset for base model with keras improved performance as below:
 - Rescaling
 - Data Augmentation using keras library
 - Dropout - 0.15
 - Batch Normalization
 - epochs = 20
 - L2 = 0.01
 - Training Accuracy = 94%, Validation Accuracy = 80%
 

#### Using Augmentor library resulted in better Accuracy with model.
 - Rescaling
 - DataAugmenter using Augmentor library.
 - Dropout 0.1
 - Batch Normalization
 - L2 = 0.01
 - epochs = 20
 - batch_size = 15
 - Addition addition layer.
 - Training Accuracy = 89%, Validation Accuracy = 84%
 - Model Looks good

##### Testing accuracy - 37.29%

## Acknowledgements
Give credit here.
- Google colab for GPU
- References if any: Google for bugs

## Contact
Created by mamathak2647@gmail.com





