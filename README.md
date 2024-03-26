# Real-time Keyword Spotting Embedded System for Mental Health Monitoring

## Introduction
This repository contains the implementation details and resources for a low-power audio analysis embedded system designed for monitoring daily mental health language markers. The system focuses on detecting absolute language expressions, potentially indicative of mental health conditions, through keyword spotting using machine learning models. 

### Goals of the Project
The primary goal of this project is to develop an embedded system capable of:
- Monitoring daily mental health language markers.
- Detecting absolute language expressions such as "never," "none," "all," "must," and "only."
- Training a machine learning model for keyword spotting.
- Providing insights into language style without diagnosing mental health conditions.
- Ensuring ethical considerations and data sharing among groups for effective model training.

## Experiment
### Data Collection and Dataset Construction
The dataset construction involved:
- Creation of a custom dataset with recordings of the keyword "Rahul."
- Augmentation of the dataset by mixing noise files with provided absolute language keywords.
- Division of the dataset into training and testing datasets with an 80-20 split.

## Algorithm
### Machine Learning Algorithm Design
The machine learning algorithm utilizes a Convolutional Neural Network (CNN) architecture for keyword spotting in audio data. Key aspects include:
- Data preprocessing to reshape input audio data.
- CNN architecture with convolutional layers, max-pooling layers, and dropout layers.
- Loss function (categorical crossentropy) and optimizer (Adam) selection.
- Training process with specified hyperparameters.

## Results
### Model Performance
The model achieved high accuracy and F1 scores on both validation and test datasets. Real-time predictions using Arduino Nano BLE 33 showed promising results.

### Demo
A demonstration showcasing real-time keyword prediction using the system was developed. The Arduino code displays identified words in the serial monitor based on prediction scores.

## Discussion
### Summary
The project demonstrated strong performance in keyword spotting for mental health monitoring.

### Difficulties and Challenges
Challenges included handling variations in pitch, tone, and audio content position.

### Resolution Strategies
Strategies to address challenges involve enhancing model robustness through diverse training data and parameter tuning.

### Improvements
Potential improvements include augmenting the dataset with more varied examples and exploring alternative machine learning architectures.

### Real-time Prediction Accuracy
Real-time predictions met expectations, demonstrating the model's effectiveness across various scenarios.

## Training Program
The provided training program utilizes TensorFlow and Keras for model training. Key parameters such as epochs, learning rate, and batch size are adjustable.

## How to Use
To replicate the project or experiment with the provided code:
1. Clone the repository.
2. Set up the environment with required dependencies.
3. Run the provided training program with desired parameters.
4. Explore the trained model's performance and experiment with real-time predictions.

## License
This project is licensed under the [MIT License](LICENSE).
