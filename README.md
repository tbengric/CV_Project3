# Super-Resolution Image Enhancement

## Overview
This project implements **Single Image Super-Resolution (SISR)** using deep learning to reconstruct high-resolution images from their low-resolution counterparts. We compare three CNN architectures and explore different loss functions to achieve optimal image quality.

## Key Features
- **3 Model Architectures**: SimpleCNN (baseline), MobileNetV2 (transfer learning), ResNet18-UNet (advanced)
- **Loss Function Comparison**: L1, L2 (MSE), and Perceptual Loss (VGG16-based)
- **Data Augmentation**: Flips, rotations, brightness/contrast adjustments
- **Comprehensive Evaluation**: PSNR and SSIM metrics on test set

## Results
- **Best Model**: ResNet18-UNet achieves ~33-35 dB PSNR and 0.91-0.94 SSIM
- **Best Loss**: L2 Loss performs slightly better (PSNR=32.96 dB, SSIM=0.9648)
- **Transfer Learning**: Significantly outperforms training from scratch with limited data

## Dataset
Source: [Image Super Resolution from Unsplash](https://www.kaggle.com/datasets/quadeer15sh/image-super-resolution-from-unsplash)
- 200 images (256×256 RGB)
- 4× upscaling factor
- 70% train / 15% val / 15% test split

## Project Structure
```
project/
├── project3_report.ipynb    # Complete technical report with code
├── requirements.txt         # Python dependencies
├── dataset/                 # High-res and low-res images (hidden)
└── checkpoints/            # Saved models and training histories
```

## Quick Start
```bash
# Install dependencies
pip install -r requirements.txt

# Run the notebook
jupyter notebook project3_report.ipynb
```

## Technologies
- PyTorch 2.0+
- TorchVision (Pre-trained models)
- NumPy, Pandas, Matplotlib
- PSNR/SSIM metrics for evaluation    