# DLProject
# Fine-Tuning EfficientNet for Medical # Image Classification

# Project Title:
Fine-Tuning EfficientNet for Medical Image Classification

# Overview:
The project will be directed towards the development of a robust medical image classifier using the state-of-the-art convolutional neural network architecture known as EfficientNet. We will apply transfer learning using pre-trained weights in order to adapt EfficientNet for medical data, for example, pneumonia case detection using chest X-ray images and skin cancer using dermoscopic images. We will also be taking a look at the performance of EfficientNet on limited data scenarios.

# Motivation and Objectives:
Efficient medical image classification can contribute much to helping health professionals with diagnostics. Herein, we shall be performing the following: 
1. Implement and fine-tune EfficientNet for medical image tasks.
2. Compare its performance against VGG16 and ResNet.
3. Use Batch Normalization for better training stability.
4. Investigate the impact of transfer learning on small datasets.
5. Search for an optimal trade-off between accuracy and inference speed.

# Dataset:
We are going to use one of the publicly available medical datasets:
1. Chest X-ray Images (Pneumonia): This is a dataset of X-ray images representing pneumonia+ and pneumonia- patients. The goal will be to identify whether an X-ray given is positive for pneumonia.
Source: https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia
2. ISIC Skin Cancer Dataset: This dataset contains images of skin lesions created by dermatoscopes. The images of skin lesions will be used in the classification of skin cancers to be either benign or malignant.
Source: https://challenge.isic-archive.com/

# Methodology:
The methodology involves preprocessing images to the EfficientNet input size of 224x224 pixels, normalizing pixel values, and applying data augmentation techniques like rotation, flipping, and zooming. The dataset is split into 70% training, 20% validation, and 10% testing. A model based on EfficientNet-B0 is constructed by replacing the final layer for binary or multi-class classification, incorporating Batch Normalization. Transfer learning is employed by initially freezing the pre-trained layers and gradually unfreezing deeper layers for fine-tuning on the medical dataset. Model evaluation is conducted using metrics such as accuracy, precision, recall, F1-score, AUC, and confusion matrices to assess classification performance.
