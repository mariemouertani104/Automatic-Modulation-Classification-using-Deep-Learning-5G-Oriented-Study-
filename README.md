# Automatic Modulation Classification using Deep Learning (5G-Oriented)

This repository presents an academic and reproducible implementation of an Automatic Modulation Classification (AMC) system using Deep Learning, inspired by recent research on the integration of Artificial Intelligence in 5G wireless communication systems.

The objective of this project is to demonstrate how convolutional neural networks can be used to automatically classify digital modulation schemes directly from raw IQ samples, without handcrafted feature extraction.

This work is aligned with the vision presented in:

Artificial Intelligence for 5G Wireless Systems: Opportunities, Challenges, and Future Research Directions  
Y. Arjoune and S. Faruque, IEEE, 2020.

---

## Project Overview

Automatic Modulation Classification (AMC) is a fundamental task in intelligent and adaptive wireless systems. It enables spectrum awareness, cognitive radio operation, and interference mitigation, which are essential components of future 5G and beyond wireless networks.

In this project, we implement a complete learning pipeline including:

- Digital signal generation
- Baseband modulation
- AWGN channel modeling
- IQ sample preprocessing
- Deep learning based classification using a 1D Convolutional Neural Network
- Performance evaluation under different Signal-to-Noise Ratio (SNR) conditions

---

## Supported Modulation Schemes

The current implementation supports the following digital modulations:

- BPSK  
- QPSK  
- 8PSK  
- 16QAM  

---

## System Architecture

The proposed system follows the pipeline below:

1. Random symbol generation
2. Digital modulation
3. Additive White Gaussian Noise (AWGN) channel
4. IQ normalization
5. CNN-based classifier
6. Softmax-based modulation decision

The neural network processes raw IQ samples directly as input.

---

## Neural Network Model

The classifier is implemented as a 1D Convolutional Neural Network with the following main components:

- Multiple 1D convolutional layers
- Batch normalization
- Max-pooling layers
- Fully connected layers
- Dropout for regularization
- Softmax output layer

The network input is a sequence of IQ samples represented as a two-channel signal.

---

## Dataset Generation

The dataset is synthetically generated and does not rely on any external dataset.

For each modulation type:

- Baseband signals are generated
- AWGN noise is added
- Signals are normalized to unit power
- Each sample contains a sequence of IQ values

This makes the project fully reproducible and independent of proprietary data.

---

## Requirements

The project is designed to run on Google Colab or a local Python environment.

Main dependencies:

- Python 3.8+
- NumPy
- TensorFlow (2.x)
- scikit-learn
- Matplotlib

---

## How to Run

### Using Google Colab

1. Open Google Colab.
2. Upload the notebook or Python script.
3. Run all cells sequentially.

No additional dataset is required.


## Experiments

The following experiments are included:

Training and validation of the CNN classifier at a fixed SNR
Evaluation of classification accuracy for multiple SNR values
Visualization of training and validation accuracy curves
Performance analysis versus SNR

## Results

The model demonstrates:

High classification accuracy at medium and high SNR
Graceful performance degradation at low SNR
Robust learning directly from raw IQ samples
These results confirm the suitability of deep learning for physical layer signal classification tasks in 5G-oriented intelligent radio systems.

###Relation to 5G and AI Research

This project directly relates to AI-enabled 5G wireless systems, especially:

Intelligent spectrum sensing

Cognitive radio
Adaptive and autonomous radio access networks
It reflects the Automatic Modulation Classification use case discussed in recent research on AI-driven 5G wireless communications

### Author

Meriem Ouertani
First-year ICT Engineering Student
National Institute of Applied Science and Technology (INSAT), Tunisia
