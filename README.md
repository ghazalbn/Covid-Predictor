# COVID-19 Detection

This is a COVID-19 prediction project that uses deep learning to classify X-ray images into two classes: COVID-19 positive and non-COVID-19. The project utilizes the SqueezeNet architecture and includes data augmentation techniques to improve model performance.

## Table of Contents
- [Project Overview](#project-overview)
- [Data Loading and Preprocessing](#data-loading-and-preprocessing)
- [Data Augmentation](#data-augmentation)
- [Model Architecture](#model-architecture)
- [Training](#training)
- [Model Evaluation](#model-evaluation)

---

## Project Overview

The project aims to classify X-ray images into two categories: COVID-19 positive and non-COVID-19. It uses a deep learning model based on the SqueezeNet architecture. The workflow involves data loading, preprocessing, data augmentation, model training, and model evaluation.

## Data Loading and Preprocessing

The dataset used in this project is loaded from Google Drive. It contains X-ray images categorized into training and test sets. The data is preprocessed by resizing, cropping, normalizing, and transforming the images to prepare them for model training.

## Data Augmentation

Data augmentation techniques are applied to the training dataset to increase its size and improve model generalization. Techniques include rotation, horizontal flip, perspective transformation, sharpness adjustment, and affine transformations.

## Model Architecture

The project uses the SqueezeNet architecture as a pretrained model. The classifier layer is modified to have two output classes: COVID-19 positive and non-COVID-19. The model is trained with a cross-entropy loss function.

## Training

The model is trained for a specified number of epochs, with a learning rate scheduler and stochastic gradient descent (SGD) optimizer. During training, the model's performance is monitored on both the training and test sets.

## Model Evaluation

The trained model is evaluated using different thresholds to calculate sensitivity and specificity. These metrics are essential for assessing the model's performance in detecting COVID-19 cases. A histogram of predicted probabilities is also generated for visualization.

---

### Usage

To use this project:

1. Mount your Google Drive to access the dataset.

```python
drive.mount('/content/gdrive')
```

2. Unzip the dataset into the dataset directory.

```python
!unzip /content/gdrive/MyDrive/data_upload_v3.zip -d dataset
```

3. Run the provided code sections sequentially to load data, perform data augmentation, build and train the model, and evaluate its performance.

4. You can adjust hyperparameters such as batch_size, num_epochs, and threshold values for model evaluation according to your requirements.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.


