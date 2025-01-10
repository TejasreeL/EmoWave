# EmoWave - Speech Emotion Recognition
This project implements a deep learning model for **Speech Emotion Recognition (SER)** using audio data. The model is trained on the **RAVDESS dataset** to classify audio signals into one of eight emotions: neutral, calm, happy, sad, angry, fear, disgust, and surprise. The pipeline includes data preprocessing, feature extraction, data augmentation, model building, training, and evaluation.

Dataset link: [Ravdess Dataset](https://www.kaggle.com/datasets/uwrfkaggler/ravdess-emotional-speech-audio)

## Project Workflow
### 1. Dataset Loading
Load the audio files from the RAVDESS dataset and assign labels based on file names.

### 2. Data Visualization
Visualize waveplots and spectrograms for various emotions.

![waveplot](https://github.com/TejasreeL/EmoWave/blob/main/images/waveplot.jpg)

![spectrogram](https://github.com/TejasreeL/EmoWave/blob/main/images/spectrogram.jpg)

### 3. Data Augmentation
Apply the following techniques:
- noise injection
- time-stretching
- shifting
- pitch adjustment

### 4. Feature Extraction
Extract the following features to reduce complexity and reduce noise:
- Zero-Crossing Rate (ZCR)
- Chroma features
- Mel-Frequency Cepstral Coefficients (MFCCs)
- MelSpectogram
- Root Mean Square (RMS)

### 5. Model Training
The model is a **1D Convolutional Neural Network (CNN)** designed for feature extraction and classification.
#### Layers:
- _Convolutional Layers_: Extract spatial features from the audio data.
- _Dropout Layers_: Prevent overfitting.
- _MaxPooling Layers_: Reduce the dimensionality of feature maps.
- _Dense Layers_: Perform classification into the 8 emotion categories.

### 6. Evaluation
Evaluate the model using metrics like accuracy, confusion matrix, and classification report.

![confusion_matrix](https://github.com/TejasreeL/EmoWave/blob/main/images/confusion.jpg)

## Results
The model achieved an accuracy of _**65.74%**_ on the test dataset.
- Loss: Decreases consistently over epochs.
- Accuracy: Peaks around 65% on validation dataset.
