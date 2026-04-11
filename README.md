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


