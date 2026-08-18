# plant-disease-prediction-using-neural-network
Deep learning project for classifying 15 plant diseases from leaf images using a CNN built with TensorFlow/Keras. Achieves ~90% test accuracy on the PlantVillage dataset

##  Project Overview

The goal of this project is to develop an image classification model capable of identifying plant diseases from leaf images.

The model was trained using the PlantVillage dataset and can classify images into 15 different classes covering Pepper, Potato, and Tomato plants.

##  Classes

The model supports the following 15 classes:

1. Pepper Bell Bacterial Spot
2. Pepper Bell Healthy
3. Potato Early Blight
4. Potato Late Blight
5. Potato Healthy
6. Tomato Bacterial Spot
7. Tomato Early Blight
8. Tomato Late Blight
9. Tomato Leaf Mold
10. Tomato Septoria Leaf Spot
11. Tomato Spider Mites
12. Tomato Target Spot
13. Tomato Yellow Leaf Curl Virus
14. Tomato Mosaic Virus
15. Tomato Healthy

##  Model

The project uses a Convolutional Neural Network (CNN) for image classification.

The general architecture consists of:

- Convolutional layers
- Max Pooling layers
- Regularization
- Fully connected layers
- Softmax output layer

The final layer contains 15 neurons, corresponding to the 15 plant classes.

##  Dataset Split

The dataset was divided into:

- **70%** Training
- **20%** Validation
- **10%** Testing

The test set was kept separate from training to evaluate the model on unseen images.

##  Results

The model achieved approximately:

| Metric | Result |
|---|---:|
| Validation Accuracy | **91.76%** |
| Test Accuracy | **90.26%** |

The model was also evaluated using a confusion matrix to identify which plant diseases were being confused with each other.

##  Error Analysis

The confusion matrix showed that some visually similar diseases were difficult for the model to distinguish.

One notable example was:

**Tomato Early Blight ↔ Tomato Late Blight**

I investigated misclassified images to understand why these classes were being confused.

This helped demonstrate that model evaluation is not only about overall accuracy, but also about understanding where and why a model makes mistakes.

##  Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- scikit-learn
- Matplotlib

##  Project Structure

```text
plant-disease/
│
├── data_set/
│   └── PlantVillage/
│
├──── plant_disease.ipynb
│
│
└── README.md
