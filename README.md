# Deep Learning Foundations: Image Classification and Generative Models

> A comparative study of classical convolution-based classification models and modern generative architectures, evaluated on standard benchmark datasets.

## 📖 Overview
This repository contains the implementation and analysis of two major deep learning laboratory assignments. The projects are divided into two main domains: supervised image classification and unsupervised generative modeling. 

---

## 📂 Project Structure

### Part 1: Image Classification (CNNs, AlexNet, ResNet)
This section evaluates the performance, computational complexity, and feature representation of three different Convolutional Neural Network architectures.

**Key Features & Experiments:**
* **SimpleCNN on MNIST:** The model reached a validation accuracy of 99.01%. We explored model optimization by successfully reducing the parameters in the fully connected layers (using 2x2 max-pooling) without losing accuracy.
* **AlexNet on CIFAR-10:** Evaluated the impact of data augmentation to combat overfitting, achieving a peak validation accuracy of 71.13%.
* **BasicResNet on CIFAR-10:** Demonstrated a superior accuracy-to-size trade-off. Despite having significantly fewer parameters than AlexNet (151,690 vs. 6,199,498), ResNet achieved higher validation accuracy (73.55% baseline, 77.23% with augmentation).
* **Latent Space Analysis:** Extensive use of t-SNE graphs to visualize how intermediate and final network layers cluster image classes, comparing the clear boundaries in MNIST with the higher intra-class variability of CIFAR-10.

### Part 2: Generative Models (VAEs & GANs)
This section explores the synthesis of MNIST handwritten digits using varied generative architectures and loss functions.

**Key Features & Experiments:**
* **Variational Autoencoders (VAE):** Implemented a plain VAE that learned a continuous latent space, demonstrating smooth morphing transitions between digit shapes during latent space interpolation.
* **Conditional VAE:** Added class labels as conditions to allow for controllable generation. Extensive grid search revealed that larger hidden dimensions (256) drastically improved loss and visual quality, while the optimal latent size ranged between 10 and 30.
* **Generative Adversarial Networks (GAN):** Compared a fully connected GAN using standard loss against a Deep Convolutional GAN (DCGAN) using least-squares loss. 
* **Visual Fidelity:** The DCGAN utilizing the least-squares loss function produced the sharpest, cleanest, and most visually consistent digits across all generative experiments.

---

## 📊 Model Performance Summary

| Model Architecture | Dataset | Parameters | Best Validation Accuracy |
| :--- | :--- | :--- | :--- |
| **SimpleCNN** | MNIST | 813,802 | 99.01% |
| **AlexNet** | CIFAR-10 | 6,199,498 | 71.13% |
| **BasicResNet** | CIFAR-10 | 151,690 | 73.55% |

---

## 🛠 Technologies Used
* **Language:** Python
* **Frameworks:** PyTorch, Torchvision
* **Analysis Tools:** t-SNE for dimensionality reduction and clustering visualization

---

## 👥 Authors
* **Andrea Sabbatini**
* **Adham Hamdy**
* **Alexandra Irina Ciurescu**
