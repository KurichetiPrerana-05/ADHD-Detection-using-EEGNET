# Investigation of EEGNet and its Variants for ADHD Detection  
## Joint Spatial, Temporal, and Frequency Domain Learning

📄 **Paper Type:** Research / Conference Paper  
🎯 **Domain:** EEG Signal Processing, Deep Learning, Healthcare AI  
🧠 **Focus:** ADHD Detection using EEGNet and its Variants  

---

## 📌 Overview

This repository contains the research work and materials for the paper:

**"Investigation of EEGNet and its Variants for ADHD Detection: Joint Spatial, Temporal, and Frequency Domain Learning"**

The study proposes an end-to-end deep learning framework for automated ADHD detection using multi-channel EEG signals. It evaluates lightweight CNN architectures, including EEGNet and a modified ShallowConvNet, under clinically realistic, subject-wise validation to avoid data leakage and ensure generalization.

---

## 📄 Abstract (Short Summary)

Early and reliable detection of ADHD using EEG signals can enable objective and accessible neurodiagnostics. This work investigates EEGNet and its variants for jointly learning spatial, temporal, and frequency-domain representations from EEG data. The models are evaluated using strict subject-wise Group K-Fold cross-validation to prevent data leakage. Statistical channel selection using the Wilcoxon rank-sum test is applied to reduce dimensionality while preserving performance. Results show that modified EEGNet improves accuracy over the standard EEGNet and highlight how sample-wise splitting can lead to artificially inflated performance.

---

## 🧠 Key Contributions

- End-to-end deep learning framework for EEG-based ADHD detection  
- Joint learning of spatial, temporal, and frequency-domain EEG features  
- Comparison between EEGNet and modified ShallowConvNet architectures  
- Subject-wise Group K-Fold validation to avoid data leakage  
- Statistical channel selection using Wilcoxon rank-sum test  
- Demonstration of how sample-wise splitting inflates performance metrics  
- Support for lightweight and wearable EEG-based diagnostic systems  

---

## 🗂️ Dataset

- **Source:** EEG Data for ADHD / Control Children (IEEE DataPort)  
- **Subjects:** 121 children (60 ADHD, 61 Control)  
- **Channels:** 19 EEG channels (10–20 system)  
- **Sampling Rate:** 128 Hz  
- **Conditions:** Eyes-open and eyes-closed resting-state EEG  

---

## ⚙️ Methodology

### 1. Preprocessing
- Band-pass filtering (0.5–40 Hz) using Butterworth filter  
- Artifact removal using FastICA  
- Epoching using sliding window (10s windows, 50% overlap)  
- Data balancing with fixed number of segments per subject  

### 2. Models
- **EEGNet (19-channel and 9-channel variants)**  
- **Modified EEGNet (ShallowConvNet inspired by FBCSP)**  
- Compact CNN architectures for efficient EEG decoding  

### 3. Channel Selection
- Wilcoxon rank-sum test to identify ADHD-relevant EEG channels  
- Reduced input dimensionality with minimal performance loss  

### 4. Training & Evaluation
- Subject-wise Group K-Fold Cross Validation (k = 5)  
- Categorical Focal Loss for class imbalance  
- Adam optimizer with learning rate scheduling  
- Comparison with sample-wise splitting to analyze data leakage  

---

## 📊 Results Summary

- Modified EEGNet outperforms standard EEGNet under subject-wise validation  
- Accuracy (19 channels):  
  - EEGNet: ~72.98%  
  - Modified EEGNet: ~77.46%  
- Reduced channel models maintain competitive performance  
- Sample-wise splitting achieves ~97–99% accuracy, but this is shown to be **inflated due to data leakage**  
- Results emphasize the importance of **subject-wise evaluation** for clinically valid EEG-based diagnosis  

---

## 🧪 Key Findings

- ADHD shows increased Delta and Theta power in frontal-central regions  
- Reduced Alpha, Beta, and Gamma power in posterior regions  
- CNNs can learn discriminative neural patterns without handcrafted features  
- Lightweight models are suitable for practical and wearable EEG systems  

---

## 👩‍💻 Authors

- Kuricheti Prerana  
- Niharika Sharma  
- Diya Dinesh  
- Pavani Satwika  
- Amrutha Veluppal  

Amrita School of Artificial Intelligence, Amrita Vishwa Vidyapeetham, India
