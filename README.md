# Directed-Adversarial-Training-for-Comprehensive-Robustification-of-CNNs

This repository contains the code, datasets, and analysis for the paper "Directed Adversarial Training for Comprehensive Robustification of CNNs". The project explores the vulnerabilities of convolutional neural networks (CNNs) to adversarial attacks and proposes retraining with adversarial examples to enhance robustness. The experiments focus on traffic sign classification using VGG16 and ResNet50 architectures.


## Paper Link

[https://ieeexplore.ieee.org/document/10723934](https://ieeexplore.ieee.org/document/10723934)
## Authors

- [@bhuvighosh3](https://github.com/bhuvighosh3)
- [@Atharv56](https://github.com/Atharv56)
- [@HarshShetye]


## Introduction

- Overview of the significance of traffic sign recognition for autonomous systems.
- Discussion on CNN vulnerabilities to adversarial attacks, emphasizing white-box attacks like FGSM, PGD, DeepFool, and Carlini & Wagner (C&W).
- Motivation for adversarial training to enhance robustness against these attacks.


## Dataset Preparation

- Description of the Belgium Traffic Sign Dataset used in the experiments.
- Details about dataset composition: 50,000+ images across 62 traffic sign classes.
- Preprocessing steps:
    Standardization and normalization of images.
    Data augmentation with adversarial examples.
## Methodology

- Model Training:
    Training of VGG16 and ResNet50 architectures on the traffic sign dataset.
    Optimization using Stochastic Gradient Descent with momentum.
- Adversarial Attacks:
    Implementation of white-box attacks:
    Fast Gradient Sign Method (FGSM): Gradient-based attack using perturbations.
    Projected Gradient Descent (PGD): Iterative gradient-based attack with boundary constraints.
    DeepFool: Optimization-based attack minimizing perturbations.
    Carlini & Wagner (C&W): Sophisticated optimization-based attack balancing misclassification and perturbation invisibility.
- Retraining with Adversarial Examples:
    Augmenting training data with adversarially perturbed images.
    Measuring trade-offs between robustness to attacks and accuracy on clean data.
## Model Performance

- Comparison of single-frame and mult-frame analysis approaches.
- Performance metrics: accuracy, precision, recall, F1-score.
- Highlight of the SVM-based multi-frame approach achieving the highest accuracy (73.5%).

## Results

- Comparison of VGG16 and ResNet50:
    Standard training accuracy: ResNet50 outperformed VGG16 on clean data.
- Adversarial attack results: ResNet50 was more vulnerable to all evaluated attacks.
- Performance of models under adversarial attacks:
    Accuracy degradation across attack types and epsilon values (perturbation levels).
- Effectiveness of each attack, with DeepFool and C&W achieving the highest success rates.
- Improvement after retraining:
    Enhanced robustness against FGSM attacks after retraining with adversarial examples.
- Slight drop in accuracy on clean images due to adversarial optimization.
## Conclusion

- Key findings on CNN vulnerabilities to adversarial attacks.
- Efficacy of adversarial retraining in improving robustness against specific attacks.
- Trade-offs between robustness and accuracy on clean data.
## Future Scope

- Exploration of advanced adversarial training techniques using diverse attack types.
- Leveraging hybrid datasets with both normal and adversarial images for improved generalizability.
- Investigating alternative loss functions and defenses like vision transformers for better multi-attack robustness.
