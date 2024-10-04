# Deep Learning-Based Approaches for Cardiovascular Monitoring Using SCG Signals

[![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)](https://pytorch.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)

## Project Overview
This project focuses on developing state-of-the-art deep learning techniques for analyzing **Seismocardiography (SCG)** signals, a non-invasive method for assessing cardiovascular function. By leveraging **Unified Attentive Cyclic Generative Adversarial Networks (UAC-GANs)**, we significantly enhance the quality of SCG signal reconstruction and improve the detection accuracy of cardiovascular events like heartbeats, arrhythmias, and other anomalies. Our approach achieves an impressive **83% improvement in signal detection accuracy** through advanced signal processing and neural network techniques.

## Table of Contents
1. [Introduction](#introduction)
2. [Key Objectives](#key-objectives)
3. [Features](#features)
4. [Project Workflow](#project-workflow)
5. [Deep Learning Architecture](#deep-learning-architecture)
6. [Data Generation and Preprocessing](#data-generation-and-preprocessing)
7. [Installation](#installation)
8. [Usage](#usage)
9. [Evaluation Metrics](#evaluation-metrics)
10. [Challenges and Solutions](#challenges-and-solutions)
11. [Future Directions](#future-directions)
12. [Acknowledgements](#acknowledgements)
13. [License](#license)

## Introduction
With cardiovascular diseases being a leading cause of death globally, non-invasive monitoring methods such as SCG are vital. SCG measures chest vibrations caused by heart activity, providing important information about heart mechanics. However, SCG signals are often corrupted by noise and external interference, making accurate signal detection and analysis challenging. This project addresses these issues using deep learning techniques, focusing on improving signal clarity and detection accuracy.

## Key Objectives
- **Signal Denoising and Enhancement**: Apply advanced wavelet and GAN-based techniques to denoise SCG signals and remove artifacts.
- **Unified Attentive Cyclic GANs (UAC-GANs)**: Introduce an attention-based cyclic GAN architecture to generate clearer, more accurate SCG signals.
- **Feature Extraction**: Extract robust features from both **Seismocardiography (SCG)** and **Electrocardiography (ECG)** signals for accurate prediction of cardiovascular events.
- **Classifier Implementation**: Train machine learning models to classify cardiovascular events and achieve high accuracy, using synthetic and real-world datasets.

## Features
- **Wavelet-Based Signal Denoising**: Use **Discrete Wavelet Transform (DWT)** for noise reduction in SCG/ECG signals.
- **UAC-GANs**: A novel architecture for **cyclic reconstruction** of signals with attention mechanisms.
- **Real-Time Cardiovascular Monitoring**: Future implementation of real-time SCG monitoring using wearable devices.
- **Cross-Signal Analysis**: Utilize both ECG and SCG signals in tandem to improve diagnosis accuracy.

## Project Workflow
1. **Data Generation**: Synthetic SCG and ECG signals are generated and corrupted with noise.
2. **Signal Denoising**: Signals are denoised using wavelet transformations.
3. **Feature Extraction**: Wavelet coefficients are extracted as features.
4. **UAC-GAN Model**: Denoised signals are passed through the UAC-GAN for refinement.
5. **Classification**: A classifier is trained on the extracted features.
6. **Evaluation**: The model is evaluated using various metrics.

## Deep Learning Architecture
The core of our project is the **Unified Attentive Cyclic GAN (UAC-GAN)**:
1. **Generator**: Reconstructs high-quality SCG signals from noisy inputs.
2. **Discriminator**: Ensures generated signals are indistinguishable from real signals.
3. **Attention Mechanism**: Focuses on crucial time segments and patterns.
4. **Cyclic Consistency**: Allows for efficient feedback loops and continuous refinement.

## Data Generation and Preprocessing
### Synthetic Data
- **ECG Signals**: Simulated using sinusoidal waveforms at 50Hz.
- **SCG Signals**: Generated as sinusoidal waveforms at 5Hz.
- **Noise**: Gaussian noise added to simulate real-world interference.

### Preprocessing
- **Wavelet Denoising**: Using Daubechies wavelet for multi-level denoising.
- **Standardization**: Features are standardized using **StandardScaler**.

## Installation
```bash
git clone https://github.com/yourusername/deep-learning-cardiovascular-monitoring.git
cd deep-learning-cardiovascular-monitoring
pip install -r requirements.txt
```

## Evaluation Metrics
- **Accuracy**: Percentage of correctly classified cardiovascular events.
- **Precision & Recall**: Balance between false positives and false negatives.
- **F1-Score**: Weighted average of precision and recall.
- **Reconstruction Error**: Difference between real and generated SCG signals.

## Challenges and Solutions
**Challenges**:
- Signal noise in SCG data.
- Complex feature selection from SCG/ECG data.

**Solutions**:
- Implemented wavelet denoising for effective noise removal.
- Used attentive GANs to focus on important signal segments.

## Future Directions
- Integrate real SCG datasets for further validation.
- Explore multi-sensor data fusion with PPG or accelerometer data.
- Develop edge-based AI models for real-time monitoring on wearable devices.

## Acknowledgements
Special thanks to the research community and open-source contributors of PyWavelets, Scikit-learn, and PyTorch.

## License
This project is open source and available under the terms of the license file included in this repository. Please see the [LICENSE](LICENSE) file for full details.
