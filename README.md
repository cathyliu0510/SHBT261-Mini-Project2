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

.
├── figures/ # Visualization results
├── segmentation_pipeline_v3.ipynb # Main notebook
├── results_summary.json # Quantitative results
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

---

## Results

### Quantitative Summary
See:

results_summary.json

---

## Qualitative Results

### Best Predictions
![Best Results](figures/best_results.png)

### Worst Predictions
![Worst Results](figures/worst_results.png)

### Model Comparison
![Comparison](figures/comparison.png)

---

## Ablation Studies
- Backbone size: ResNet-18 vs ResNet-50
- Data augmentation: with vs without
- Loss function: Cross-Entropy vs Dice

---

## How to Run

```bash
pip install torch torchvision segmentation-models-pytorch matplotlib numpy
jupyter notebook segmentation_pipeline_v3.ipynb

Update dataset path before running.

Notes
- Large files (datasets, checkpoints) are excluded
- SAM2 requires external checkpoint loading
