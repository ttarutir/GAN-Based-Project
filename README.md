# GAN-based Cross-Modality Medical Image Synthesis for Prostate Cancer

This repository contains implementation of a BicycleGAN-based approach for cross-modality medical image synthesis, specifically translating ADC MRI scans into high-quality T2-weighted (T2W) MRI images for prostate cancer diagnosis (as a proof of concept).

## Project Overview

The project aims to address limitations in multi-sequence MRI acquisition by generating diagnostic-quality T2W images from ADC MRI scans. Our enhanced BicycleGAN architecture incorporates:

- Self-attention mechanisms
- Gradient penalty
- Perceptual loss components
- Advanced optimization techniques

Key results achieved:
- PSNR: 26.48 dB
- SSIM: 0.82
- L1 Loss: 0.05

## Prerequisites

- Python 3.8+
- PyTorch 1.9+
- CUDA-capable GPU (recommended)

## Installation

1. Clone the repository:

2. Download the dataset:
- Access requires CMU domain credentials
- Download from: [ProstateCancerDataset](https://drive.google.com/file/d/1g77l402OJyRb3hVC5eYM2xclqB-Gb3HO/view?usp=drive_link)
- Place the unzipped dataset in the project root directory

## Model Architecture

The implementation consists of three main components:

1. **Encoder (E)**:
   - Encodes target images into latent space
   - Incorporates self-attention mechanisms
   - Outputs mean and log variance for latent sampling

2. **Generator (G)**:
   - U-Net based architecture
   - Takes source image and latent code as input
   - Generates target modality images

3. **Discriminator (D)**:
   - PatchGAN discriminator
   - Evaluates image authenticity at patch level
   - Includes gradient penalty for stable training

## Training

To train the model, enter your5 wandb key and run all cells in the notebook.

## Results

The model demonstrates significant improvements over baseline approaches:

| Metric | Baseline | Enhanced Model |
|--------|----------|----------------|
| PSNR   | 25.57 dB | 26.48 dB      |
| SSIM   | 0.77     | 0.82          |
| L1 Loss| 0.39     | 0.05          |

## Contributors
- Takudzwa Talent Tarutira (ttarutir)
- Francis Tatenda Chekure (ftc)
- Melinda Tatenda Mudzurandende (mmudzura)
- Prosper Singadi (psingadi)





