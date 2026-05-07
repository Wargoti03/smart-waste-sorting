Smart Waste Sorting System

Team Members
❖ Philip Ayoreh
❖ Kristina Akpan
❖ Torry Andris
❖ Omar Nayel
❖ Brandon Rollins
➢ Tier 1 – Image Classification

The Problem
Problem:
• People frequently misclassify waste (recyclable vs trash), leading to contamination in recycling systems.

Who cares:
• Households
• Recycling companies
• Environmental agencies

Why it’s important:
• Reduces recycling efficiency
• Increases processing costs
• Harms environmental sustainability

Solution
Solution:
An AI-powered image classification system that identifies waste
type from images.

How it works:
User uploads image → Model classifies waste → Output category

Summary:
This project builds an image classification model that predicts the
category of waste (plastic, paper, metal, or trash) from an input
image. The system helps users make better recycling decisions.

Technical Approach
• Technique: Image Classification
• Model: ResNet-50
• Framework: PyTorch

Why this works:
ResNet is accurate, pretrained, and easy to fine-tune for
classification tasks.

Dataset Plan
• Source: TrashNet dataset (Kaggle)
• Size: ~2500 images
• Labels: Plastic, paper, glass, metal, trash
• Preparation: minimal cleaning and resizing

System Diagram
[User Image]
↓
[Preprocessing]
↓
[ResNet Model]
↓
[Classification]
↓
[Output Label]

Metrics
Metric Type   Example        Target
Primary       Accuracy      ≥ 90%
Secondary     Speed         < 1 sec/image

Week-by-Week Plan
Week        Task                Milestone
1       Setup dataset          Data ready
2       Train model            Model works
3       Improve accuracy       Better results
4       Build demo             Completed system
5       Submission             Ready


Challenges & Backup Plans
Risk                    Probability          Mitigation
Low accuracy            Medium               Data augmentation
Small/Missing data      Low                  Use larger dataset
Overfitting             Medium               Regularization/Add dropout
Training issues         Low                  Use pretrained weights

Resources Needed
• Google Colab
• PyTorch
• Python
Estimated Cost: $0


UPDATE:

Smart Waste Sorting System
Project Overview

The Smart Waste Sorting System is a deep learning computer vision project designed to automatically classify waste materials into recycling categories using image classification techniques. The goal of the project is to improve recycling efficiency, reduce manual sorting effort, and demonstrate how artificial intelligence can support sustainable waste management systems.

This project uses a ResNet-based convolutional neural network implemented with PyTorch and trained using transfer learning on a garbage classification dataset.

Problem Statement

Manual waste sorting is:

Time-consuming
Inconsistent
Labor-intensive
Prone to contamination errors

Incorrect sorting can reduce recycling effectiveness and increase waste management costs.

The Smart Waste Sorting System solves this problem by automatically identifying waste categories from images with high classification accuracy.

Solution

The system accepts an image of waste material and predicts the correct category using a trained deep learning model.

The model can classify:

Cardboard
Glass
Metal
Paper
Plastic
Trash

The system was trained and evaluated in Google Colab using PyTorch and transfer learning with ResNet.

Dataset

Dataset Used:

Garbage Classification / TrashNet Dataset

Dataset Characteristics:

Thousands of labeled waste images
Multiple recycling categories
Real-world waste object photographs
Dataset Classes
Cardboard
Glass
Metal
Paper
Plastic
Trash
Dataset Split
Split	Purpose
Training Set	Model training
Validation Set	Hyperparameter tuning
Test Set	Final evaluation
Data Preprocessing and Augmentation

The following preprocessing steps were applied:

Image resizing to 224 × 224
Tensor conversion
Pixel normalization

Augmentation techniques included:

Random horizontal flipping
Random rotations
Random transformations
Data normalization

These steps improved generalization and reduced overfitting.

Model Architecture
Why ResNet?

ResNet was selected because it:

Performs strongly on image classification tasks
Solves vanishing gradient problems
Learns deep visual features effectively
Works well with transfer learning

Transfer learning was used with pretrained ImageNet weights to improve accuracy and reduce training time.

Frameworks and Libraries

Framework:

PyTorch

Libraries:

torchvision
scikit-learn
matplotlib
numpy
PIL
OpenCV

Development Environment:

Google Colab
Training Configuration
Hyperparameter	Best Value
Learning Rate	0.001
Batch Size	32
Optimizer	Adam
Epochs	20
Loss Function	CrossEntropyLoss
Results
Evaluation Metrics
Metric	Result
Accuracy	92%
Precision	90%
Recall	89%
F1-Score	89%
Inference Speed	0.05s per image

The model achieved strong classification accuracy and fast inference performance suitable for near real-time waste classification.

Confusion Matrix Analysis

The confusion matrix showed:

Strong performance on cardboard, glass, and metal
Moderate confusion between paper and cardboard
Some confusion between plastic and glass
Trash category was the most difficult due to high visual variation
Class-Wise Performance
Class	Performance
Cardboard	Excellent
Glass	Excellent
Metal	Very Good
Paper	Good
Plastic	Good
Trash	Moderate
Screenshots
Sample Predictions

Confusion Matrix

Add confusion matrix screenshot here:

results/visualizations/confusion_matrix.png
Training Curves

Add training graphs here:

results/visualizations/training_accuracy.png
results/visualizations/loss_curve.png
Failure Cases

The model struggled under:

Poor lighting
Blurry images
Occluded objects
Mixed waste items
Similar-looking materials

Examples:

Plastic confused with glass
Paper confused with cardboard

Future improvements could include:

Larger datasets
Weighted loss functions
Object detection models (YOLO)
Real-time webcam integration
How to Run the Project
1. Clone Repository
git clone https://github.com/yourusername/smart-waste-sorting.git
cd smart-waste-sorting
2. Install Requirements
pip install -r requirements.txt
3. Open Notebook

Open:

notebooks/SmarWasteSorting.ipynb

Run all notebook cells in Google Colab or Jupyter Notebook.

4. Dataset Setup

Place the dataset inside:

dataset/garbage_classification/

The folder should contain class subfolders such as:

cardboard
glass
metal
paper
plastic
trash


