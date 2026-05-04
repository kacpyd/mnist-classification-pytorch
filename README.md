# Handwritten Digit Classification with PyTorch

This project presents handwritten digit classification on the MNIST dataset using several neural network architectures implemented in PyTorch.

The notebook compares simple and more advanced models, analyzes overfitting, applies regularization, and tunes a convolutional neural network to achieve more than **99% test accuracy**.

## Models included

- **Perceptron** — a single-layer linear baseline
- **Deep fully-connected network** — a model with a hidden layer
- **CNN** — a basic convolutional neural network
- **BetterCNN** — a tuned convolutional model with Batch Normalization, dropout, and Adam optimizer

## Project goals

- load and preprocess the MNIST dataset
- split the data into training, validation, and test subsets
- train and compare multiple neural network models
- analyze overfitting using training and validation loss
- apply regularization techniques such as L2 regularization
- tune a CNN model to exceed 99% test accuracy
- visualize classification errors using a confusion matrix

## Dataset

The project uses the **MNIST** dataset of handwritten digits:
- **60,000** training images
- **10,000** test images
- grayscale images of size **28 × 28**
- **10 classes** representing digits from `0` to `9`

In this project, the original training set is further split into:
- **50,000** training samples
- **10,000** validation samples

## Results summary

| Model | Test Accuracy | Notes |
|------|------:|------|
| Perceptron | ~92% | Simple baseline, limited capacity |
| Deep | ~96% | Better performance, but shows overfitting |
| Deep + L2 | ~96% | Slightly more stable validation behavior |
| CNN | ~96–98% | Better suited for image classification |
| BetterCNN | **99.27%** | Best model, exceeded the target |

## Key observations

- The **Perceptron** works as a useful baseline, but it is too simple for best performance.
- The **Deep** model significantly improves the results, but it tends to overfit.
- Adding **L2 regularization** slightly improves generalization.
- **CNN-based models** perform better because they preserve the spatial structure of image data.
- The tuned **BetterCNN** achieved **99.27% test accuracy**, successfully exceeding the required **99% threshold**.
- The confusion matrix shows that the remaining mistakes mostly occur between visually similar digits such as **9 and 5**, **9 and 4**, or **7 and 2**.

## Repository structure

```text
mnist-classification-pytorch/
├── README.md
├── requirements.txt
├── .gitignore
├── notebooks/
│   └── mnist_classification.ipynb
└── images/
