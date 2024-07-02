# Real-time-Stress-Monitoring-System
An automated and streamlined system for detecting stress in drivers through the development of a real-time stress monitoring pipeline that classifies ECG signals collected from a sensor, using an effective Deep Learning model based on the VGGNet architecture predict various stress levels.

## Introduction
Stress is a significant concern as it can lead to health issues such as depression, anxiety, and cardiovascular problems. In the context of driving, stress can adversely affect performance and increase the likelihood of accidents. The proposed system leverages advancements in wearable technology to monitor electrocardiogram (ECG) signals, aiming to automate stress detection through deep learning models​

## System Overview
The core of the system is the real-time collection and analysis of ECG signals using sensors. The hardware design includes components for power management, an analog front end, and WiFi modules. The ECG sensors are strategically placed on the driver to ensure accurate data acquisition. The collected data is transmitted to a processing unit (Jetson Nano), where it is analyzed using a pre-trained deep learning model based on the VGGNet architecture. The results are then displayed on a user-friendly interface developed with a Flask web application, providing real-time feedback to the driver​.

## Data Processing and Model Training
The training was done using the publicly available driveDB dataset. [link (https://physionet.org/content/drivedb/1.0.0/)]
Comprehensive data processing pipeline, starting from data cleaning to feature extraction was conducted. Various ECG signal processing techniques were employed, and the data was used to train machine learning and deep learning models. Classical machine learning models such as K-Nearest Neighbors (K-NN), Decision Trees, Random Forest, and XGBoost were evaluated, but deep learning models, particularly VGGNet, demonstrated superior performance. The VGGNet model achieved varying accuracy rates for different stress levels, with the highest accuracy observed for severe stress​.

## Dependencies and Packages

The code was written in Python 3 within Jupyter Notebooks (`.ipynb`).
Below are the python libraries necessary for this section.

- `pandas`
- `numpy`
- `matplotlib`
- `scipy`
- `imblearn`
- `wfdb`
- `sklearn`
- `torch`
- `seaborn`

## Files description

1. `pre-processing.ipynb` -> Contains code to read and annotate driveDB dataset.
2. `ECG_signal_processing.ipynb` -> Contains code that performs basic cleaning i.e., baseline wander removal, bandpass filtering. It also calculates Heart Rate (HR).
3. `Feature_extraction_and_ML.ipynb` -> Contains code to extract features from ECG and HR data, to rank the features by computing feature importance, and the final code that trains and tests classical Machine Learning models.
4. `Deep_learning_training` -> Training VGGNet architecture using PyTorch.

Read report for full details!
