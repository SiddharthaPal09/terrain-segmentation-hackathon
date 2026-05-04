# 🌍 Terrain Segmentation using Deep Learning

This project was developed as part of a hackathon focused on semantic segmentation of real-world terrain images. The model identifies and segments different regions such as vegetation, land, water, sky, rocks, and more.

---

## 📌 Problem Statement

Given an input image, the goal is to perform **semantic segmentation** by classifying each pixel into predefined terrain categories such as:
- 🌿 Vegetation
- 🪨 Rock
- 🌊 Water
- 🌄 Land
- ☁️ Sky/ others

---

## 🧠 Approach

We used a **Transformer-based segmentation model (SegFormer)** for accurate pixel-wise classification.

### Key Steps:
- Data cleaning (fixing mismatched RGB and mask files)
- Image preprocessing & augmentations
- Model training using PyTorch
- Loss optimization using CrossEntropyLoss
- Evaluation using mIoU / mAP50

---

## ⚙️ Tech Stack

- Python
- PyTorch
- HuggingFace Transformers
- Albumentations
- NumPy

---

## 📂 Project Structure
.
├── desert-seg-v1/
│   ├── checkpoints/
│   │   ├── best_model.pth
│   │   └── last_model.pth
│   │
│   ├── outputs/
│   │   ├── metrics/
│   │   │   ├── confusion_matrix.png
│   │   │   ├── iou_scores.csv
│   │   │   ├── loss_graph.png
│   │   │   └── val_iou_summary.csv
│   │   │
│   │   └── predictions/
│   │
│   ├── src/
│   │   ├── dataset.py
│   │   ├── evaluate.py
│   │   ├── model.py
│   │   ├── predict.py
│   │   ├── prepare.py
│   │   └── train.py
│   │
│   ├── training-dataset-seg/
│   │   ├── train/
│   │   │   ├── Color_Images/
│   │   │   └── Segmentation/
│   │   │
│   │   └── val/
│   │       ├── Color_Images/
│   │       └── Segmentation/
│   │
│   ├── config.yaml
│   └── venv/
│
└── training-dataset/

---

## 📊 Results

- ✅ **mIoU Achieved:** ~0.4313  
- 📈 Currently working towards improving it to **0.7+**

---

## 🧩 Challenges Faced
- Dataset inconsistencies (missing/mismatched masks)
- Debugging training pipeline under time constraints
- Handling shape mismatch issues in segmentation output
- Limited time for fine-tuning model

---

##🔮 Future Improvements
- Better hyperparameter tuning
- Data augmentation improvements
- Model architecture experimentation
- Increase mIoU beyond 0.6+

---

##👨‍👩‍👦 Team Members
- Ashwani Kumar (Team Leader)
- Siddhartha Pal
- Sumit Mehara
- Nitin Kumar

---

##📌 Notes

- This repository contains the complete implementation used for the hackathon submission. Final evaluation will be conducted by organizers based on submitted results.

---

##🙌 Acknowledgment

- We thank the organizers for providing a meaningful real-world problem and a well-structured hackathon experience.
