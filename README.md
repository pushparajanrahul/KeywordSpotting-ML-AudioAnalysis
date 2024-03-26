# Mental Health Language Monitoring with Low-Power Audio Analysis Embedded System

This repository contains the code and documentation for a project aimed at developing a low-power audio analysis embedded system capable of monitoring daily mental health language markers. The system focuses on detecting absolute language expressions, such as "never," "none," "all," "must," and "only," which have been identified as potential markers in mental health forums. The objective is to create a tool that performs keyword spotting through a machine learning model trained on specific keywords related to absolutist language use.

## Introduction

The goal of this project is to develop a low-power audio analysis embedded system capable of monitoring daily mental health language markers. The system aims to provide insights into language style rather than content, potentially offering a non-intrusive means of monitoring mental health language patterns. The project emphasizes ethical considerations and data sharing among groups to build a comprehensive dataset for effective model training.

## Experiment

### Data Collection and Dataset Construction

A custom dataset was created by recording the keyword "Rahul" in different tones and pitches. Additionally, absolute language keywords provided by the instructor were utilized. Data preprocessing involved mixing keyword files with noise files to generate additional samples. The final preprocessed dataset was divided into training and testing datasets using an 80-20 split.

## Algorithm

### Machine Learning Algorithm Design

The machine learning algorithm is designed for keyword spotting in audio data. It employs a 1D convolutional neural network (CNN) architecture for feature extraction. The model uses categorical crossentropy loss function and the Adam optimizer. The training process involves monitoring accuracy and cross-entropy loss on both the training and validation sets.

## Results

The model demonstrated high accuracy and F1 scores across different classes. Real-time predictions using Arduino Nano BLE 33 showed promising results, with accurate recognition of keywords, particularly the keyword "Rahul."

### Performance Metrics

The training loss vs. epochs plot and confusion matrices for the validation and test datasets are provided. Both matrices show high accuracy, with most values on the diagonal being close to 100%. F1 scores are generally high, indicating a good balance between precision and recall for each class.

## Discussion

### Summary

The model demonstrated strong performance, achieving high accuracy and F1 scores across different classes. Real-time predictions using Arduino Nano BLE 33 showed promising results, with accurate recognition of keywords, particularly the keyword "Rahul."

### Difficulties and Challenges

Challenges included handling variations in pitch, tone, and audio file content position. Achieving a balance between sensitivity and specificity in real-time predictions could be challenging.

### Resolution Strategies

To address challenges, the model's robustness can be enhanced by incorporating more diverse training data and fine-tuning parameters. Adjusting the threshold for displaying predictions in the serial monitor can help optimize real-time performance.

### Possible Improvements

Augmenting the dataset with more varied examples and experimenting with different machine learning architectures or algorithms could improve the model's generalization.

### Real-time Prediction Accuracy

The real-time predictions met expectations, demonstrating the model's robustness across different pitches, tones, and content positions.

## Repository Structure

- `train.py`: Python script for training the machine learning model.
- `dataset-curation.py`: Python script for data preprocessing.
- `README.md`: Documentation providing an overview of the project, including goals, experiment details, algorithm design, results, discussion, and repository structure.

## Usage

To train the machine learning model, run `train.py` with appropriate arguments for epochs, learning rate, batch size, etc. Ensure dependencies are installed as specified in `requirements.txt`.

## Contributions

Contributions to this project are welcome. Please follow the contribution guidelines outlined in `CONTRIBUTING.md`.

## License

This project is licensed under the [MIT License](LICENSE).

