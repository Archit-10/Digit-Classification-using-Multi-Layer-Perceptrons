# Multi-layer Perceptrons - Digit Classification

## **Project Overview**
In this project, we perform digit classification using a Multi-layer Perceptron (MLP) model. The dataset consists of images representing digits, and the goal is to predict the corresponding digit for each image. We utilize the `MLPClassifier` from `sklearn` to train and evaluate the model's performance on the given dataset.

## **Dataset**
The dataset consists of three parts:
- **training_3digits.hdf5**: Contains training images and their corresponding digit labels.
- **testing_3digits_part1.hdf5**: The first part of the testing dataset.
- **testing_3digits_part2.hdf5**: The second part of the testing dataset.

### **Number of Images**
- **Training set**: 2726 images
- **Testing set 1**: 3147 images
- **Testing set 2**: 3147 images

## **Setup**
To run the project, you need the following Python packages:
- `numpy`
- `h5py`
- `matplotlib`
- `sklearn`

### **Loading the Dataset**
The dataset is loaded from `.hdf5` files. Below is an example of how the dataset is loaded and processed.

```python
import numpy as np
import h5py

# Load the training data
filename = "training_3digits.hdf5"
train = h5py.File(filename,'r')
train_images = np.array(train['images'])
train_digits = np.array(train['digits'])
train.close()

# Load the testing data
filename = "testing_3digits_part1.hdf5"
test1 = h5py.File(filename,'r')
test_images_1 = np.array(test1['images'])
test_digits_1 = np.array(test1['digits'])
test1.close()

filename = "testing_3digits_part2.hdf5"
test2 = h5py.File(filename,'r')
test_images_2 = np.array(test2['images'])
test_digits_2 = np.array(test2['digits'])
test2.close()
