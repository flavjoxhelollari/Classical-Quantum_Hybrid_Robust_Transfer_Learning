# Hybrid Classical-Quantum Transfer Learning: Robustness, Privacy, and Adversarial Attacks

This project demonstrates a **hybrid classical-quantum transfer learning framework** that unites pre-trained Vision Transformer (ViT) backbones with a quantum-enhanced classifier, adversarial training, and differential privacy (DP). The code and experiments let you explore how quantum enhancements, privacy constraints, and adversarial defenses interact in modern machine learning pipelines, using CIFAR-10 as a testbed.

---

## Features

- **Hybrid Classical-Quantum Model**  
  - Freezes a pre-trained ViT backbone and replaces the classifier with a parameterized quantum circuit (PennyLane).
  - Includes a classical baseline for direct comparison.
- **Differential Privacy (DP) Training**  
  - Integrates DP-SGD to provide formal privacy guarantees by adding calibrated noise to gradients during training.
- **Adversarial Training & Evaluation**  
  - Supports adversarial training (FGSM, PGD attacks) and robust evaluation under various perturbation strengths.
- **Mixed-Data Adversarial Training**  
  - Combines adversarial examples from both DP-protected and unprotected data to balance privacy, accuracy, and robustness.
- **Empirical Analysis & Visualization**  
  - Includes scripts to plot privacy-robustness-accuracy trade-offs and visualize model vulnerability to adversarial attacks.

---

## Workflow

1. **Prepare Data**  
   - Download and preprocess CIFAR-10 images for training and evaluation.
2. **Model Selection**  
   - Choose between the hybrid quantum-classical model or a classical-only baseline.
3. **Training Regimes**  
   - Train with standard, DP, adversarial, or mixed adversarial+DP regimes.
4. **Evaluate Performance**  
   - Assess clean accuracy and robustness against FGSM/PGD attacks at varying ε.
   - Analyze the impact of DP noise on decision boundaries and attack surface.
5. **Interpret Results**  
   - Compare privacy, accuracy, and robustness trade-offs.
   - Examine the effect of quantum classifier vs. classical classifier.

---

## Requirements

- Python 3.8+
- torch, torchvision, numpy, matplotlib, tqdm, scipy
- pennylane
- opacus (for DP-SGD)
- torchattacks (for adversarial attacks)
- transformers (for ViT backbone)

Install dependencies:
pip install pennylane opacus torchattacks transformers torchvision matplotlib tqdm scipy



---


**Note:** For detailed usage, see the source code and notebooks in this repository.  
For correspondence: flavjoxhelollari
