# MustGAN: T1 ↔ T2 MRI Image Translation

MustGAN is a deep learning model based on Generative Adversarial Networks (GANs) for translating between T1-weighted and T2-weighted MRI scans. The model enables bidirectional synthesis: generating T2 images from T1 inputs and vice versa, facilitating tasks in medical image preprocessing, data augmentation, and cross-modality synthesis.

##  Overview

Magnetic Resonance Imaging (MRI) is commonly used in clinical diagnostics. T1 and T2 modalities provide complementary anatomical and pathological information. MustGAN aims to bridge the modality gap by learning mappings between T1 and T2 MR images using unpaired data, leveraging adversarial and cycle consistency losses.

##  Features

- Converts **T1 MRI** to **T2 MRI**
- Converts **T2 MRI** to **T1 MRI**
- Based on a CycleGAN-style architecture
- Supports training and testing modes
- Modular and customizable PyTorch implementation

##  Sample Results

*(Add sample before/after images if available)*

| Input (T1) | Generated (T2) | Ground Truth (T2) |
|------------|----------------|-------------------|
| ![](samples/t1_input.png) | ![](samples/t2_fake.png) | ![](samples/t2_real.png) |

##  Architecture

MustGAN is built upon a CycleGAN-like architecture with two generators (`G_T1 to T2`, `G_T2toT1`) and two discriminators (`D_T1`, `D_T2`). The model is trained using:

- Adversarial loss
- Cycle consistency loss
- Identity loss (optional)

## Directory Structure

