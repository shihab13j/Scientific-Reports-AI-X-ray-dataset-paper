

---

# 🛑 Attention-Guided YOLOv11 and Transformer Fusion for Enhanced Detection of Prohibited Items in X-Ray Security Images

> Official implementation of **YOLOv11-TFNet**
> Hybrid Attention-Guided YOLOv11 + Transformer Fusion Framework
> (Submitted to *Scientific Reports*)

---

## 📌 Overview

This repository contains the official PyTorch implementation of **YOLOv11-TFNet**, a hybrid deep learning framework designed for robust prohibited item detection in dual-energy X-ray security images.

The proposed model integrates:

* ⚡ YOLOv11 for high-speed object localization
* 🧠 Transformer-based multi-head self-attention for global contextual reasoning
* 🎯 Attention-guided feature fusion
* 🔄 Class-Specific Augmentation Framework (CSAF) to address class imbalance

The model is designed for **real-time deployment** in high-throughput security environments such as airport baggage screening.

---

## 🚀 Key Contributions

* ✅ Hybrid YOLOv11 + Transformer architecture
* ✅ Dual-energy feature exploitation
* ✅ Attention-guided contextual reasoning
* ✅ Class-specific augmentation strategy
* ✅ Real-time inference (~104 FPS on NVIDIA Tesla T4)

---

## 📊 Performance

| Metric    | Value    |
| --------- | -------- |
| mAP@50    | 0.886    |
| mAP@50–95 | 0.712    |
| Precision | 0.885    |
| Recall    | 0.823    |
| F1-score  | 0.853    |
| Inference | ~104 FPS |

---

## 🗂 Dataset

**Balanced X-ray Contraband Detection Dataset**

* 13,728 images
* 12 prohibited item categories
* Dual-energy X-ray format

Kaggle Dataset link:https://www.kaggle.com/datasets/nikitamanaenkov/x-ray-contraband-detection-dataset

---

## 🏗 Model Architecture

```
Input Image
     ↓
YOLOv11 Backbone
     ↓
Transformer Fusion Block
     ↓
Attention-Guided Feature Enhancement
     ↓
Detection Head
     ↓
Bounding Boxes + Class Scores
```

---



---

## ▶️ Training

```bash
python train.py --data data.yaml --epochs 150 --img 640
```

---

## 🔎 Inference

```bash
python detect.py --weights best.pt --source test_images/
```

---

## 📈 Ablation Study

We conducted extensive ablation experiments to validate:

* Transformer Fusion contribution
* Attention module effectiveness
* CSAF impact on minority classes

Results demonstrate consistent performance gains across all major metrics.

---

## 🔬 Visualization

* Attention heatmaps
* Precision-Recall curves
* Class-wise ROC curves
* Detection outputs

---

## 📦 Repository Structure

```
├── models/
├── datasets/
├── train.py
├── detect.py
├── utils/
├── requirements.txt
└── README.md
```

---




