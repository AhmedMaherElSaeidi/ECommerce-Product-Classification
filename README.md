# E-Commerce Product Classification

Developing a deep learning model to classify product images within the Slash application into predefined groups, streamlining product categorization.

## Table of Contents

- [Introduction](#introduction)
- [Approach](#approach) 
- [Kaggle](#kaggle)
- [Demo](#demo)

## Introduction

Thank you for considering me for the AI Internship at Slash! This repository contains my solution for the Product Image Classifier task.

## Approach

To tackle this task, I followed a step-by-step approach outlined below:

1. **Dataset Download:** I obtained the product images by screenshotting them through the Slash application. I used OpenCV to clean the images and unify their shapes, I made two shapes 1080*1080 and 480*480, and because of limited resources, I used the 480*480 images to train the model. 

2. **Data Preparation:** I preprocessed the images by normalization, and splitting the data into training and validation sets `80:20`. And for the labels, I use one hot encoding as a common practice for my case.

3. **Model Building:** As we have a small dataset I used transfer learning to enhance my model performance and `DenseNet121` was the one that improved the accuracy rather than `Inception-ResNet-v2`. I used `softmax` as an activation function for the output layer as the model is considered to classify multiple labels instead of a binary label. I used `adam` as an optimizer with a learning rate of `0.0001` as it improved accuracy and reduced overfit ( I used dropout layers too in the model architecture to handle the overfitting issue. ).

4. **Training:** I trained the CNN model on the prepared dataset. I used a callback function to save the model state at its best weights tracking the least `val_loss` value which was `0.1343`

5. **Validation:** I evaluated the trained model's performance using the validation set to ensure it generalizes well to unseen data, it showed an accuracy of `94.79%` and a loss of `0.1343`.

7. **Testing:** Finally, I tested the trained model on a separate test set to assess its overall accuracy and effectiveness in classifying product images.

## Kaggle

### Kaggle Dataset

The dataset used for training the model is available on Kaggle. You can download it from the following link: [Kaggle Dataset](https://www.kaggle.com/datasets/ahmedmaherelsaeidy/slash-dataset).

### Kaggle Notebook

I have also created a Kaggle notebook for this project. You can access it [here](https://www.kaggle.com/code/ahmedmaherelsaeidy/slash-products-classification).

## Demo

Here's a short video demonstrating the functionality of the Product Image Classifier: [Demo](https://www.youtube.com/watch?v=M5c6Qx5DGvo)


