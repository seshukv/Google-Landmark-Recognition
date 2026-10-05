# Google Landmark Recognition

## Overview
Deep learning project for the Google Landmark Recognition 2021 Kaggle competition.
Built and compared two CNN approaches to classify landmark images across 76,563 classes.

## The Challenge
- Massive dataset with extreme class imbalance
- Some landmarks had 1000+ images, others had just 1-2
- Required careful data preprocessing before any modeling

## Approach

### Data Preprocessing
- Analyzed class distribution across 76,563 landmark categories
- Undersampled classes with 30+ images to maximum 30 per class
- Removed classes with fewer than 3 images to reduce noise
- Applied class weights to handle remaining imbalance

### Image Augmentation
- Random horizontal flip
- Random rotation (±30°)
- Width and height shift
- Zoom range
- Shear transformation

### Model 1 — Custom CNN from Scratch
- 3 Convolutional layers (16, 32, 64 filters)
- MaxPooling after each conv layer
- Dropout (0.1) for regularization
- Dense layers (128, 256 units)
- LeakyReLU activation throughout
- Softmax output for 76,563 classes

### Model 2 — Transfer Learning with ResNet50V2
- Loaded pretrained ResNet50V2 (trained on ImageNet)
- Froze all pretrained layers
- Added custom Dense layers (256, 512 units)
- Fine tuned only the top layers
- Significantly faster convergence than custom CNN

## Key Learnings
- Transfer learning dramatically outperforms training from scratch on image classification
- Class imbalance handling is critical — without it model ignores rare classes
- Image augmentation significantly improves generalization on limited data
- ResNet50V2 pretrained on ImageNet transfers well even to landmark recognition

## Technologies
- Python, TensorFlow, Keras
- ResNet50V2 (pretrained on ImageNet)
- ImageDataGenerator for augmentation
- scikit-learn for class weights

## Dataset
Kaggle — Google Landmark Recognition 2021
https://www.kaggle.com/competitions/landmark-recognition-2021
