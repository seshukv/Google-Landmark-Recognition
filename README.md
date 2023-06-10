# Google Landmark Recognition Project
The "Google Landmark Recognition Project" aims to identify the class that a given image belongs to. This project is based on the Kaggle competition named Google Landmark Recognition 2021. The objective of the competition is to develop a CNN that can accurately recognize and classify landmarks from images.

<h3>Installation Instructions</h3>
To run this project locally:
Clone the repository and Install the required dependencies

<h3>Usage Guidelines</h3>
To use this project, follow the guidelines below:

Download the dataset from the Kaggle competition page and ensure it is properly organized.<br>
Perform exploratory data analysis (EDA) to gain insights into the dataset's characteristics and distribution.<br>
Address the class imbalance issue by undersampling the dataset and removing classes with fewer than 3 images to eliminate bias.<br>
Apply class weights and implement image augmentation techniques to enhance the model's performance on the imbalanced dataset.<br>
Utilize two different approaches for image classification:<br>
Build a Convolutional Neural Network (CNN) model from scratch and train it using the image data.<br>
Utilize a pre-trained model, such as ResNetv2, and fine-tune the model's layers at the end to suit the specific problem requirements.<br>
Employ the ImageDatagenerator to preprocess and prepare the images for training and evaluation.

<h3>Features</h3>
Exploratory Data Analysis (EDA) to gain insights into the dataset<br>
Addressing class imbalance through undersampling and removal of classes with few images<br>
Class weighting and image augmentation techniques to enhance model performance<br>
Custom CNN model training from scratch<br>
Utilization of a pre-trained model (ResNetv2) with customized layers for transfer learning<br>
Image preprocessing and preparation using ImageDatagenerator<br>

<h3>Technologies Used</h3>
Python

<h3>Contributing</h3>
Contributions to this project are currently not open. However, feel free to fork the repository and work on your own version.

<h3>License</h3>
The code in this project is available under the MIT License.

<h3>Additional Information</h3>
For more information about the competition and to obtain the required dataset, please refer to the Kaggle competition page. 
(URL: https://www.kaggle.com/competitions/landmark-recognition-2021)
