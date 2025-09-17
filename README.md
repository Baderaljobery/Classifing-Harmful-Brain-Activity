# Harmful Brain Activity Classification using Deep Learning

This repository contains a deep learning-based system for classifying harmful brain activities using EEG (Electroencephalography) data. The goal is to assist medical professionals in detecting abnormal brain patterns such as seizures and discharges with greater speed and accuracy.

## Project Summary

EEG is widely used to monitor the electrical activity of the brain, especially in critically ill patients. However, interpreting EEG signals manually is time-consuming and prone to human error. This project introduces an automated approach using deep learning to classify various harmful EEG patterns with competitive performance.

## Objectives

- Automate the classification of harmful brain activities using EEG data.
- Reduce diagnostic time and support neurologists in critical care settings.
- Improve accuracy using spectrogram transformation and deep learning techniques.

## Target Classes

The model classifies EEG activity into six categories:

- Seizure (SZ)
- Generalized Periodic Discharges (GPD)
- Lateralized Periodic Discharges (LPD)
- Lateralized Rhythmic Delta Activity (LRDA)
- Generalized Rhythmic Delta Activity (GRDA)
- Other

## Technologies Used

| Category         | Tools & Libraries                          |
|------------------|---------------------------------------------|
| Language         | Python                                      |
| Deep Learning    | TensorFlow, Keras, KerasCV                  |
| Data Processing  | NumPy, Pandas, Parquet                      |
| Visualization    | Matplotlib                                  |
| Deployment       | Streamlit                                   |
| Training Platform| Kaggle (free GPU resources)                 |

## Model Architecture

- Base Model: EfficientNetV2-B2 (pretrained on ImageNet)
- Input Format: EEG spectrogram images (400x300x3)
- Loss Function: Kullback-Leibler (KL) Divergence
- Data Split: Stratified K-Fold Cross Validation
- Augmentation: MixUp, RandomCutout
- Feature Reduction: PCA (Principal Component Analysis)

## Evaluation Metrics

| Metric    | Value     |
|-----------|-----------|
| Accuracy  | 70.44%    |
| Precision | 70.31%    |
| Recall    | 70.44%    |
| F1 Score  | 70.03%    |
| AUC       | 0.8981    |

## Dataset

- Source: Harvard Medical School
- Format: Parquet
- Type: EEG recordings from critically ill patients
- Preprocessing: Normalization, noise filtering, spectrogram conversion

> ⚠️ Dataset not included due to licensing and privacy constraints.

## Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/harmful-brain-activity-classification.git
cd harmful-brain-activity-classification
