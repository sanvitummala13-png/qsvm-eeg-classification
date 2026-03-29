# Quantum-Inspired EEG Classification for Motor Imagery

> A lightweight quantum-inspired machine learning framework for EEG motor imagery classification using the PhysioNet EEG Motor Movement/Imagery Dataset.

---

## Project Summary

Brain-computer interfaces (BCIs) often rely on computationally expensive models or long calibration times, limiting real-world usability. This project investigates whether a **quantum-inspired support vector machine (QSVM)** can provide a more computationally efficient alternative while maintaining competitive classification performance.

This work benchmarks a proposed QSVM pipeline against **classical machine learning** and **state-of-the-art deep learning architectures** on EEG motor imagery data.

---

## Research Question

**Can a lightweight quantum-inspired classifier achieve competitive EEG classification performance while using less computational complexity than deep learning models?**

---

## Why This Matters

Non-invasive EEG-based BCIs are promising for:
- Assistive communication systems
- Neurorehabilitation
- Motor intention decoding
- Wearable neural interfaces

However, many high-performing models require:
- Large training compute
- GPU acceleration
- Longer calibration pipelines

A more efficient classification framework could improve accessibility and real-world deployment.

---

## Dataset

**PhysioNet EEG Motor Movement/Imagery Dataset**

- **Subjects:** 109
- **Channels:** 64 EEG channels
- **Sampling Frequency:** 160 Hz
- **Task Type:** Baseline vs Motor Imagery classification
- **Recordings:** 654 total runs

### Class Definitions
- **Class 0:** Baseline / resting state
- **Class 1:** Motor imagery condition

---

## Methodology

### 1) EEG Preprocessing
- Signal loading and trial segmentation
- Artifact-aware preprocessing
- Feature extraction using **Power Spectral Density (PSD)**

### 2) Benchmarking Framework
The proposed QSVM was evaluated against the following models:

- **QSVM (Proposed)**
- Classical SVM
- CNN1D
- CNN2D
- EEGConformer
- EEGNet
- EEGTransformer
- LSTM
- ShallowConvNet
- TSception

### 3) Evaluation Metrics
Models were compared using:

- Accuracy
- F1-Score
- ROC-AUC
- Recall
- Precision

### 4) Statistical Validation
A **Wilcoxon signed-rank test** was used to assess whether the QSVM significantly outperformed the classical SVM baseline.

---

## Key Results

### QSVM Performance
- **Accuracy:** 0.734
- **F1-Score:** 0.814
- **ROC-AUC:** 0.696
- **Recall:** 0.913
- **Precision:** 0.720

### Main Finding
The proposed QSVM:
- **Outperformed the classical SVM baseline**
- Achieved performance **comparable to several deep learning baselines**
- Required substantially lower computational complexity than many deep architectures

---

## Results Visualizations

### Model Performance Comparison
![Model Comparison](bar_chart.png)

### Confusion Matrix Comparison
![Confusion Matrix](confusion_matrices.png)

---

## Interpretation

Although the QSVM did not exceed the top-performing deep learning model on every metric, it demonstrated a strong tradeoff between **classification performance** and **computational efficiency**.

This suggests that **quantum-inspired approaches may be especially valuable in resource-constrained BCI settings**, where lightweight models are preferable to GPU-intensive pipelines.

---

## Future Work

Potential next steps include:

- Subject-specific personalization
- Cross-subject generalization analysis
- Real-time inference for BCI deployment
- Exploration of quantum kernel methods
- Integration with wearable EEG systems
- Reducing calibration time in assistive neural interfaces

---

## Repository Structure

```bash
.
├── README.md
├── qsvm_eeg_benchmark.ipynb
├── qsvm_eeg_classification.py
├── bar_chart.png
├── confusion_matrices.png
└── requirements.txt
```

---

## Installation

```bash
pip install -r requirements.txt
```

---

## Author

**Sanvi Tummala**  
High school researcher in machine learning, neurotechnology, and computational neuroscience.

---

## Citation

If referencing this project, please cite the repository or contact the author for collaboration or academic use.
