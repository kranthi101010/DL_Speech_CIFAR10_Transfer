# DL_Speech_CIFAR10_Transfer_Learning
Deep Learning (DL), Speech Denoising, CIFAR-10, and Transfer Learning
# Deep Learning for Speech Denoising and CIFAR-10 Classification

## 🚀 Overview
This project explores deep learning techniques for two key tasks:
1. **Speech Denoising using CNNs** – A convolutional model trained on magnitude spectrograms to enhance speech signals.
2. **CIFAR-10 Classification with Transfer Learning** – A deep learning approach to classify images with and without pre-training.

---

## 📂 Dataset
### **1. Speech Denoising Dataset**
- **Training Data:** Noisy and clean speech audio files.
- **Testing Data:** Separate noisy speech samples for evaluation.
- **Preprocessing:** Short-Time Fourier Transform (STFT) is used to convert audio into spectrograms.

### **2. CIFAR-10 Image Classification Dataset**
- **Training Data:** 50,000 labeled images of 10 classes.
- **Testing Data:** 10,000 labeled images.
- **Augmentation:** Brightness, contrast adjustments, flipping, and rotation.

---

## 🏗️ Implemented Models

### **1. Speech Denoising**
✅ **CNN-Based Denoising Model:**  
- Takes the magnitude spectrogram of a noisy speech signal as input.
- Predicts the magnitude spectrogram of a clean signal.
- The phase information is preserved, and the STFT inverse is applied to reconstruct the waveform.
- Evaluated using **Signal-to-Noise Ratio (SNR)**.

### **2. CIFAR-10 Classification**
✅ **Baseline CNN Classifier:**  
- A standard convolutional neural network trained from scratch on CIFAR-10.

✅ **Transfer Learning via Pretext Task:**  
- A CNN is first trained on an **unlabeled pretext task**, where it classifies images based on transformations (flipping, rotation, etc.).
- The trained model is then used as a feature extractor for CIFAR-10 classification.
- Compared against the **baseline model** to measure accuracy improvement.

---

## 📊 Experiments & Findings

### **Speech Denoising Results**
- The CNN-based denoising model effectively reconstructs clean speech.
- Evaluated using **SNR (Signal-to-Noise Ratio)**, showing improved speech clarity.

### **CIFAR-10 Classification Results**
- **Baseline CNN Accuracy:** Lower due to limited training data.
- **Transfer Learning Model Accuracy:** Higher due to feature reuse from the pretext model.
- **Data Augmentation:** Improved accuracy by exposing the model to varied images.

---

## ⚙️ Dependencies
Ensure you have the following libraries installed before running the project:

```bash
pip install tensorflow numpy librosa matplotlib soundfile
