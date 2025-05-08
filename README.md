# Hybrid Self-Supervised and Classical Machine Vision for Polyp Segmentation

## Overview
This project explores a hybrid approach for automated polyp segmentation in colonoscopy images by integrating self-supervised learning (SSL) and classical machine vision techniques. The resulting model, **PolyFusionNet**, addresses key challenges in clinical polyp detection, including data scarcity, domain variability, and model interpretability.

## Motivation
Colorectal cancer (CRC) is a leading cause of cancer-related deaths. Early polyp detection during colonoscopy significantly improves outcomes but remains challenging due to imaging variability and human error. Our approach enhances segmentation accuracy and robustness using a fusion of handcrafted features and deep learning representations.

## Key Features
- ⚙️ **PolyFusionNet Architecture**:
  - Combines classical edge-based feature extraction with a transformer-based encoder.
  - Uses MoCo-v2 for SSL pretraining to learn rich visual representations.
 ![image](https://github.com/user-attachments/assets/499e5660-3018-4a63-9d5b-95418bfe7c4d)

  
- 📊 **Ablation Study**:
  - Baseline U-Net
  - Classical Vision Model
  - SSL-only Model
  - Hybrid SSL + Classical (PolyFusionNet)

| Model               | Val Dice | Val IoU | Val Loss | Val Precision | Val Recall |
|---------------------|----------|---------|----------|----------------|-------------|
| Baseline            | 0.8462   | 0.0124  | 0.0626   | 0.8366         | 0.9176      |
| Classical           | 0.8544   | 0.0125  | 0.0724   | 0.8447         | 0.9158      |
| SSL                 | 0.7821   | 0.0110  | 0.0801   | 0.8322         | 0.8331      |
| PolyFusionNet (Ours)| **0.8601** | **0.0126** | **0.0612** | **0.8489**       | **0.9201**    |
    
- 📈 **Datasets**:
  - `HyperKvasir`: 99k+ unlabeled images for self-supervised pretraining.
  - `CVC-ClinicDB`: Expert-annotated images for supervised fine-tuning and evaluation.

## Evaluation Metrics
- Dice Score
- IoU (Intersection over Union)
- Precision, Sensitivity, Specificity
- Comparative performance vs. PraNet, ACSNet, ColonSegNet, Polyp-PVT

## Results
- Significant improvements in generalization and robustness under domain shifts.
- PolyFusionNet outperforms baseline and achieves competitive performance with fewer annotations.
- Strong interpretability due to classical feature integration.
![image](https://github.com/user-attachments/assets/db6e03a8-307b-499b-8dff-bdfead0c6ce6)


## Future Work
- Apply contrastive learning with advanced SSL frameworks (e.g., DINO, SimCLR).
- Optimize architecture for real-time clinical deployment.
- Incorporate domain adaptation for multi-center generalizability.

## Authors
- **Zinah Ghulam** – MASc Biomedical Engineering, University of Guelph  
- Supervisor: **Dr. Medhat Moussa**

## Citation
If you use this work, please cite:
