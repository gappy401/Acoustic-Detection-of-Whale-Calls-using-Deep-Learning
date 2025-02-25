# Acoustic Detection of Whale Calls using Deep Learning



## Overview
This project focuses on implementing a communication-efficient federated learning-based anomaly detection framework for Industrial Internet of Things (IIoT) applications. The system incorporates gradient compression techniques to improve efficiency and reduce the communication overhead associated with federated learning.

## Dataset
The dataset consists of time series data from IIoT sensors, capturing various parameters such as:
- **TP2**: Pressure on the compressor
- **TP3**, **H1**, **DV_pressure**, **Reservoirs**, **Oil_temperature**, **Motor_current**, etc.
- **class**: Binary label (1 indicates an anomaly)

The dataset is large, with a potential class imbalance, requiring careful preprocessing and model tuning.

## Models Used
The project compares multiple anomaly detection models, including:
- **CNN-LSTM**: A hybrid deep learning model combining convolutional layers with LSTMs for temporal pattern recognition.
- **Attention Mechanism CNN-LSTM**: An enhanced version incorporating an attention mechanism to focus on critical time steps.
- **SAE (Stacked Autoencoder)**: Used for unsupervised anomaly detection.
- **GRU (Gated Recurrent Unit)**: A variant of RNN suitable for sequential data.

## Federated Learning Approach
The federated learning framework consists of:
- A **central server** aggregating global model updates.
- **Two IIoT client nodes**, each training models on their local data.
- **Gradient compression techniques** (such as sparsification) to optimize communication between clients and the central server.

## Key Findings
- **Gradient compression significantly reduced communication costs** while maintaining high anomaly detection accuracy.
- The **Attention Mechanism CNN-LSTM model benefited the most**, achieving a 35% reduction in training time.
- **Sparsification improved SAE model accuracy** from 95.5% to 97.25% by reducing noise.
