# Cityscapes Semantic Segmentation (PyTorch)

This project implements a full semantic segmentation pipeline on the Cityscapes dataset using PyTorch. It focuses on training, evaluating, and comparing two popular architectures: FCN-ResNet50 and DeepLabV3-ResNet50.

## Overview
The repository covers the complete workflow required for urban scene segmentation:
- Loading and exploring the Cityscapes dataset
- Preprocessing images and masks with consistent resizing
- Remapping Cityscapes label IDs to 19 valid training classes
- Handling ignored labels correctly during training
- Training FCN and DeepLabV3 models
- Evaluating performance using confusion matrices and mean IoU
- Visualizing and comparing model predictions

## Models
- **FCN-ResNet50**: A baseline fully convolutional network for semantic segmentation  
- **DeepLabV3-ResNet50**: An advanced model using atrous convolutions for better context capture

## Training
Models are trained using CrossEntropyLoss with an ignore index for unlabeled pixels and optimized with Adam. Training progress is tracked per epoch, and losses are reported for monitoring convergence.

## Evaluation
Performance is evaluated both quantitatively and qualitatively:
- Confusion matrices across all 19 classes
- Mean Intersection-over-Union (mIoU)
- Side-by-side visual comparison of predictions from both models

## Purpose
This project is intended as a clean, practical reference for learning and experimenting with semantic segmentation on real-world street-scene data using modern deep learning models in PyTorch.
