# Directed Adversarial Training for Comprehensive Robustification of CNNs

This repository contains the code, datasets, and analysis for the paper "Directed Adversarial Training for Comprehensive Robustification of CNNs." The project investigates the vulnerabilities of Convolutional Neural Networks (CNNs) to adversarial attacks and proposes a robust retraining method using adversarial examples. The experiments focus on traffic sign classification tasks, utilizing VGG16 and ResNet50 architectures.

## Paper Link
[Directed Adversarial Training for Comprehensive Robustification of CNNs](https://ieeexplore.ieee.org/document/10723934)

## Authors
- Bhuvi Ghosh
- Atharv
- Harsh Shetye

## Introduction
This project emphasizes the importance of traffic sign recognition in autonomous systems and explores the vulnerabilities of CNNs to adversarial attacks. It highlights the effectiveness of white-box attacks, including FGSM, PGD, DeepFool, and Carlini & Wagner (C&W), and proposes directed adversarial training as a solution for improving CNN robustness.

## Dataset Preparation
- **Dataset**: Belgium Traffic Sign Dataset with over 50,000 images across 62 traffic sign classes.
- **Preprocessing**:
  - Standardization and normalization of images.
  - Data augmentation, including the generation of adversarial examples to enhance training.

## Methodology
- **Model Training**:
  - VGG16 and ResNet50 architectures are trained on the Belgium Traffic Sign Dataset.
  - Optimization is performed using Stochastic Gradient Descent with momentum.
- **Adversarial Attacks**:
  - **Fast Gradient Sign Method (FGSM)**: A gradient-based attack that generates small perturbations.
  - **Projected Gradient Descent (PGD)**: An iterative attack with boundary constraints.
  - **DeepFool**: An optimization-based attack that minimizes perturbations for misclassification.
  - **Carlini & Wagner (C&W)**: A sophisticated optimization-based attack that balances misclassification and perturbation invisibility.
- **Retraining with Adversarial Examples**:
  - Augmenting the training data with adversarially perturbed images.
  - Measuring the trade-off between robustness to attacks and accuracy on clean data.

## Model Performance
- Comparison of single-frame and multi-frame analysis approaches.
- Performance metrics: Accuracy, precision, recall, and F1-score.
- Highlight of the SVM-based multi-frame approach achieving the highest accuracy (73.5%).

## Results
- **Comparison of VGG16 and ResNet50**:
  - Standard training accuracy: ResNet50 outperformed VGG16 on clean data.
  - Adversarial attack results: ResNet50 was more vulnerable to all evaluated attacks.
- **Performance under Adversarial Attacks**:
  - Accuracy degradation observed across attack types and epsilon values (perturbation levels).
  - Effectiveness of each attack, with DeepFool and C&W achieving the highest success rates.
- **Retraining Improvement**:
  - Enhanced robustness against FGSM attacks after retraining with adversarial examples.
  - A slight drop in accuracy on clean images due to adversarial optimization.

## Conclusion
- Key findings on CNN vulnerabilities to adversarial attacks.
- Efficacy of adversarial retraining in improving robustness against specific attacks.
- Trade-offs between robustness and accuracy on clean data.

## Future Scope
- Exploration of advanced adversarial training techniques using diverse attack types.
- Leveraging hybrid datasets with both normal and adversarial images for improved generalizability.
- Investigating alternative loss functions and defenses, such as vision transformers, for better multi-attack robustness.
