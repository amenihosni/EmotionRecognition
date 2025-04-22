# 🎭 Emotion Recognition from Speech using Diffusion Models

This project presents a state-of-the-art approach to **speech emotion recognition (SER)** through **mel-spectrogram-based data augmentation using diffusion models**. Our method leverages diffusion processes to generate high-quality, emotionally rich audio representations, enabling improved emotion classification accuracy.

---

## 📌 Overview

We use diffusion modeling to enhance emotion clarity in speech data, which is evaluated using a ResNet-based emotion recognition classifier. The process involves:

- Converting emotional audio clips into mel-spectrograms.
- Using a **diffusion model** to generate augmented spectrograms with stronger emotional features.
- Training a **ResNet-50 CNN** model for emotion classification.
- Evaluating performance improvements on **EmoDB** and **RAVDESS** datasets.

---

## 📊 Results

| Dataset | Weighted Accuracy (WA) | Unweighted Accuracy (UA) |
|--------|------------------------|--------------------------|
| EmoDB (Original) | 82.1% | 81.7% |
| EmoDB (Generated) | **94.3%** | **91.6%** |
| RAVDESS (Original) | 67.7% | 65.1% |
| RAVDESS (Generated) | **77.8%** | **79.7%** |

Classification performance (Generated data - EmoDB):
- **Accuracy:** 98.31%
- **F1 Score:** 0.9831

---

## 📁 Dataset

We use the following publicly available datasets:

- **[EmoDB](http://emodb.bilderbar.info/)** (German, 6 emotions)
- **[RAVDESS](https://zenodo.org/record/1188976)** (English, 7 emotions)

All data is resampled to 22,025 Hz and standardized to 10-second utterances.

---

## 🧪 Model Architecture

### 🧠 Emotion Recognition Model
- **Input:** Mel-spectrogram
- **Model:** ResNet-50 (CNN-based)
- **Optimizer:** Adam (`lr=1e-4`)
- **Loss:** CrossEntropy
- **Epochs:** 800

### 🌫️ Diffusion Model for Augmentation
- **Input:** Emotion + Style embedding
- **Architecture:** ResNet blocks with attention layers
- **Output:** Emotionally enriched mel-spectrogram

---

