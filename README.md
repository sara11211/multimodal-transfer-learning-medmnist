# Multimodal Transfer Learning for Medical Imaging

## Project Title

Multimodal Transfer Learning for Medical Imaging: Linear Probing vs Fine-Tuning

## Topic Description

This project evaluates different transfer learning strategies for medical image classification. The goal is to compare how well a pre-trained model (ResNet-50 on ImageNet) adapts to medical domains when using different fine-tuning approaches.

The main research questions are:
- What is the trade-off between predictive performance and computational cost for different transfer learning methods?
- Does the optimal strategy depend on the type of medical data?

## Datasets

This project uses two datasets from MedMNIST+:
- **DermaMNIST:** Dermatoscopic images of skin lesions (7 classes)
- **BloodMNIST:** Microscopy images of blood cells (8 classes)

Source: https://medmnist.com/

## Methods to Compare

| Method | Description |
|--------|-------------|
| Training from scratch | Baseline without any pretraining |
| Linear probing | Freeze pretrained features, train only the classifier head |
| Full fine-tuning | Update all parameters of the pretrained model |
| Double-transfer learning | Transfer between medical domains (e.g., DermaMNIST → BloodMNIST) |
| Self-supervised pretraining (exploratory) | SimCLR or MoCo pretraining on target domain |

## Evaluation Metrics

- Top-1 Accuracy
- Confusion matrices
- Training time
- GPU memory usage

## Repository Structure
├── README.md
├── requirements.txt
├── .gitignore
├── data/ # datasets 
├── notebooks/ # Jupyter notebooks for EDA and analysis
├── src/ # source code
├── reports/ # weekly reports and final report
└── results/ # experiment outputs 

## Setup Instructions
1. Clone this repository:
   git clone https://github.com/sara11211/multimodal-transfer-learning-medmnist.git
2. Install dependencies from `requirements.txt`:
    pip install -r requirements.txt
