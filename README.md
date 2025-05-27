# wireless-wanderlust
Different files show experimenting with different neural network architectures, to see which one is the most accurate for our use case
1. Wanderlust_sample16(teja)- contains dense network results, modified the pipeline from the Dichasus website example
2. Complex-value-neural-network(teja)- trying out the same problem on a cvnn architecture
3. dichasus positioning tutorial(anu)- trying on a cnn architecture
4. task1_new (teja)- Complete pipeline of semi-supervised learning for task 1 implemented- need to improve accuracy, include r90 metric for loss computation


# Wireless Wanderlust – Indoor Localization with CSI

This repository contains Team Antenna avergers's work for the **Wireless Wanderlust** competition, which focuses on indoor localization using Channel State Information (CSI) in a semi-supervised learning setting. The competition tasks span deep learning, signal processing, communication efficiency, and decentralized inference.

## 🚀 Overview

Low-latency and accurate indoor localization is a critical enabler for many real-world applications including IoT, robotics, and AR/VR systems. This project explores the use of CSI data from multiple remote antennas to estimate user positions in complex indoor environments—without relying on traditional GPS.

Participants receive:
- CSI tensors: `4 antenna arrays × 8 elements × 64 frequencies`
- Labeled data: 25%
- Unlabeled data: 75%
- Evaluation metrics: **Mean Absolute Error (MAE)** and **R90 radius**

## 🧠 Core Contributions

- **Task 1: Single-shot Localization**
  - Built deep neural networks to estimate position from raw CSI tensors.
  - Used semi-supervised learning to train on limited labeled data and generalize with unlabeled samples.

- **Task 2: Temporal Trajectory Prediction**
  - Developed models using **LSTM** and **Transformer** architectures to predict positions from CSI sequences.
  - Improved localization accuracy using temporal continuity.

- **Task 3: Grant-Free Random Access**
  - Designed decentralized inference strategies to minimize communication between antennas and fusion center.
  - Created lightweight models for local decision-making under tight bandwidth constraints.

- **Task 4: CSI Compression & Feature Selection**
  - Implemented a global compression model for CSI.
  - Balanced between communication cost and localization accuracy through efficient feature transmission policies.

## 🛠️ Tech Stack

- Python, PyTorch, NumPy
- Data I/O: HDF5, custom loaders
- Deep Learning: CNNs, RNNs (LSTM), Transformers
- Evaluation: MAE, R90
- Optional: GMAT/MATLAB for simulation (if used in later phases)
