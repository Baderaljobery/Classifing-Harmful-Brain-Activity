# Harmful Brain Activity Classification Using Deep Learning

This repository provides a deep learning system for automated classification of harmful brain activities based on EEG (Electroencephalography) data. The objective is to support medical professionals by improving the speed and accuracy of EEG interpretation, particularly for critically ill patients.

---

## Overview

Manual interpretation of EEG signals is time-consuming and susceptible to human error. This project leverages state-of-the-art deep learning and data processing techniques to automate the detection and classification of abnormal brain activities, thereby assisting neurologists in clinical decision-making.

---

## Objectives

- **Automated Detection**: Classify harmful brain activities using EEG data.
- **Clinical Support**: Reduce diagnostic time and assist neurologists in critical care.
- **Enhanced Accuracy**: Utilize spectrogram transformation and advanced deep learning architectures.

---

## Classification Categories

The model identifies six categories of EEG activity:

1. **Seizure (SZ)**
2. **Generalized Periodic Discharges (GPD)**
3. **Lateralized Periodic Discharges (LPD)**
4. **Lateralized Rhythmic Delta Activity (LRDA)**
5. **Generalized Rhythmic Delta Activity (GRDA)**
6. **Other**

---

## Technologies & Tools

| Category          | Tools & Libraries                        |
|-------------------|------------------------------------------|
| Programming       | Python                                   |
| Deep Learning     | TensorFlow, Keras, KerasCV               |
| Data Processing   | NumPy, Pandas, Parquet                   |
| Visualization     | Matplotlib                               |
| Deployment        | Streamlit                                |
| Training Platform | Kaggle (GPU resources)                   |

---

## Model Architecture

- **Base Model**: EfficientNetV2-B2 (pretrained on ImageNet)
- **Input Format**: EEG spectrogram images (`400x300x3`)
- **Loss Function**: Kullback-Leibler (KL) Divergence
- **Validation**: Stratified K-Fold Cross Validation
- **Augmentation**: MixUp, RandomCutout
- **Feature Reduction**: Principal Component Analysis (PCA)

---

## Performance Metrics

| Metric    | Value     |
|-----------|-----------|
| Accuracy  | 70.44%    |
| Precision | 70.31%    |
| Recall    | 70.44%    |
| F1 Score  | 70.03%    |
| AUC       | 0.8981    |

---

## Dataset

- **Source**: Harvard Medical School
- **Format**: Parquet
- **Type**: EEG recordings from critically ill patients
- **Preprocessing**: Normalization, noise filtering, spectrogram conversion

> **Note:** The dataset is excluded from this repository due to licensing and privacy constraints.

---

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/Baderaljobery/Classifing-Harmful-Brain-Activity.git
cd Classifing-Harmful-Brain-Activity
```

### 2. Project Structure

```
Classifing-Harmful-Brain-Activity/
│
├── app.py                 # Streamlit app for model predictions
├── train.py               # Training script
├── best_model.keras       # Trained model file
├── requirements.txt       # Python dependencies
├── README.md              # Project documentation
└── data/                  # (Excluded) EEG spectrogram files
```

---

## Authors

- **Bader Abdulaziz Aldhahi**
- **Bader Hubaytir Aljubayri**
- **Mohammed Abdullah Aldukhayel**

**Supervised by:** Dr. Mohd Anul Haq

---

## License

This project is for academic and research purposes. Please refer to the repository for licensing details.
