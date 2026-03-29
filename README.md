# Quantum-Inspired EEG Classification for Motor Imagery

## Overview
This project benchmarks a quantum-inspired support vector machine (QSVM) for EEG motor imagery classification using the PhysioNet EEG Motor Movement/Imagery Dataset.

## Research Question
Can a lightweight quantum-inspired classifier achieve competitive performance while using less computation than deep learning models?

## Dataset
- PhysioNet EEG Motor Movement/Imagery Dataset
- 109 subjects
- 64 EEG channels
- 160 Hz sampling rate

## Models Compared
- QSVM (proposed)
- Classical SVM
- CNN1D
- CNN2D
- EEGConformer
- EEGNet
- EEGTransformer
- LSTM
- ShallowConvNet
- TSception

## Key Results
- QSVM Accuracy: 0.734
- QSVM F1-Score: 0.814
- QSVM ROC-AUC: 0.696
- QSVM outperformed the classical SVM baseline

## Figures

### Model Comparison
![Model Comparison](bar_chart.png)

### Confusion Matrix Comparison
![Confusion Matrices](confusion_matrices.png)

## Significance
The proposed QSVM achieved competitive performance with lower computational complexity than many deep learning baselines, making it promising for more efficient brain-computer interface systems.

## Author
Sanvi Tummala
