# Big Five Image Recognition Project

A project by Mihir Arjun

## Table of Contents

- [Image Recognition for Classifying the Big Five Animals of South Africa](#image-recognition-for-classifying-the-big-five-animals-of-south-africa)
- [Data Preparation and Cleaning](#data-preparation-and-cleaning)
- [Loading and Visualising the Data](#loading-and-visualising-the-data)
- [Data Scaling](#data-scaling)
- [Splitting the Data](#splitting-the-data)
- [Building the Deep Learning Model](#building-the-deep-learning-model)
- [Training the Model](#training-the-model)
- [Plotting Model Performance](#plotting-model-performance)
- [Evaluating the Model](#evaluating-the-model)
- [Testing the Model](#testing-the-model)
- [Summary](#summary)

## Image Recognition for Classifying the Big Five Animals of South Africa

This project focuses on classifying images of the Big Five animals of South Africa using a Convolutional Neural Network (CNN) built with TensorFlow and Keras. The Big Five includes buffalo, elephant, leopard, lion, and rhino. The guide provides a step-by-step approach to building, training, and deploying a CNN for this classification task.

## Data Preparation and Cleaning

- **Image Validation:** Validate each image using OpenCV to ensure it is not corrupted.
- **Format Verification:** Verify the image file type against supported formats.
- **Removal of Invalid Images:** Remove corrupted or unsupported images to maintain dataset integrity.

## Loading and Visualising the Data

Use TensorFlow's `image_dataset_from_directory` utility to load images and automatically infer labels based on subdirectory names. Visualise a few sample images to verify correct loading and labeling.

## Data Scaling

- **Normalising Pixel Values:** Normalise pixel values to a range between 0 and 1 by dividing by 255.0.
- **Verifying Scaling:** Fetch and visualise a batch of images post-normalisation to ensure proper scaling.

## Splitting the Data

Split the dataset into:

1. **Training Set (70%)**: For model training.
2. **Validation Set (20%)**: For hyperparameter tuning and monitoring.
3. **Test Set (10%)**: For final performance evaluation.

## Building the Deep Learning Model

- **Initialising the Model:** Create a Sequential model using Keras.
- **Adding Convolutional and Pooling Layers:** Extract spatial features and downsample feature maps.
- **Flattening and Adding Dense Layers:** Flatten 2D feature maps into a 1D vector and add Dense layers for high-level representations.
- **Adding the Output Layer:** Use a Dense layer with softmax activation for multi-class classification.
- **Compiling the Model:** Use the Adam optimizer, Sparse Categorical Cross Entropy loss function, and monitor accuracy.

## Training the Model

- **Fitting the Model:** Train the CNN using the training dataset over specified epochs while monitoring validation performance.
- **Saving the Trained Model:** Save the trained model for future use.

## Plotting Model Performance

- **Plotting Loss:** Visualise training and validation loss over epochs to assess learning.
- **Plotting Accuracy:** Plot training and validation accuracy to evaluate classification capability.

## Evaluating the Model

- **Assessing Performance on Test Data:** Evaluate the model using the test dataset and calculate accuracy metrics.
- **Evaluation Process:** Iterate through test data in batches and update accuracy metrics.

## Testing the Model

- **Loading the Saved Model:** Load the saved model for prediction without retraining.
- **Preparing a Test Image:** Resize and normalise new images for compatibility.
- **Making Predictions:** Predict class probabilities for test images.
- **Determining the Predicted Class:** Identify the class with the highest probability.
- **Extracting Prediction Probability:** Retrieve the predicted class probability.
- **Applying a Confidence Threshold:** Define a threshold (e.g., 60%) for conclusive predictions.
- **Outputting the Result:** Display the predicted class and probability or indicate insufficient confidence.

## Summary

- **Data Cleaning:** Ensure dataset integrity by removing invalid images.
- **Data Loading and Scaling:** Load and normalise images for efficient training.
- **Data Splitting:** Divide the dataset for training, validation, and testing.
- **Model Building:** Construct a CNN tailored for multi-class classification.
- **Training and Saving:** Train the model while monitoring performance and save for future use.
- **Performance Visualisation:** Plot loss and accuracy to assess learning.
- **Model Evaluation and Testing:** Evaluate on unseen data and make confident predictions.

