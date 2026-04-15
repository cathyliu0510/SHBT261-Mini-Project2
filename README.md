# SHBT261-Mini-Project2

# Semantic Segmentation on Pascal VOC 2007

## Overview
This project implements and evaluates multiple semantic segmentation models on the Pascal VOC 2007 dataset. The goal is to compare model performance, analyze trade-offs between architectures, and understand the impact of key design choices.

The models evaluated include:
- U-Net (ResNet-18 encoder)
- DeepLabV3+ (ResNet-50 encoder)
- SAM2 (Segment Anything Model 2, zero-shot)

---

## Repository Structure

├── figures/ # Visualization outputs

├── segmentation_pipeline_v3.ipynb

├── results_summary.json

├── README.md


---

## Dataset
This project uses the **Pascal VOC 2007 dataset**, which contains:
- 20 object classes + background
- Pixel-wise segmentation masks

Download:
https://www.kaggle.com/datasets/zaraks/pascal-voc-2007

---

## Methods

### Models
- **U-Net**: Encoder–decoder architecture with skip connections
- **DeepLabV3+**: Multi-scale context via atrous convolution
- **SAM2**: Zero-shot foundation segmentation model

### Evaluation Metrics
- Mean Intersection-over-Union (mIoU)
- Dice Coefficient
- Pixel Accuracy
- Per-class IoU
- HD95
- Confusion matrix

### Visualization
- Mosaic-style qualitative segmentation maps
- Side-by-side comparisons of input, ground truth, and prediction
- Top 3 best and top 3 worst results
- Special attention to the human class due to its complexity

---

## Ablation Studies
- Backbone size: ResNet-18 vs ResNet-50
- Data augmentation: with vs without
- Loss function: Cross-Entropy vs Dice

---

## Notes
- Large files (datasets, checkpoints) are excluded
- SAM2 requires external checkpoint loading
