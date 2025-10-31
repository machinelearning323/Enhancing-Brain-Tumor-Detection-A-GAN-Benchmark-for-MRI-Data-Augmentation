# Generating Brain MRI Images using Four GAN Architectures

This repository presents an academic research project focused on **synthetic brain MRI image generation** using **four Generative Adversarial Network (GAN)** architectures. The goal is to explore how deep generative models can synthesize realistic MRI scans for use in medical imaging research, data augmentation, and AI-based diagnostic system development.

---

## 🧠 Overview

Deep learning has shown remarkable performance in image-based medical applications, but the success of these models relies heavily on the availability of large and diverse datasets. In medical imaging, data scarcity and privacy constraints often limit training data availability.

This project leverages **GAN-based models** to generate high-quality, realistic brain MRI images. The generated images can support:
- Data augmentation for tumor detection and classification models.
- Research on synthetic data generation and evaluation.
- Development of privacy-preserving AI systems in healthcare.

---

## 📚 Implemented GAN Models

The notebook implements and compares **four GAN architectures** for MRI image generation:

1. **DCGAN (Deep Convolutional GAN)** — Baseline architecture for generating 2D MRI scans.  
2. **WGAN (Wasserstein GAN)** — Enhances stability of training and improves image quality.  
3. **CycleGAN** — Generates cross-domain MRI transformations (if applicable).  
4. **StyleGAN or Conditional GAN** — Produces highly realistic and controlled image outputs.

Each model is trained on the **Kaggle Brain MRI Dataset** and evaluated based on image quality and convergence performance.

---

## 📊 Dataset

- **Source**: [Kaggle Brain MRI Dataset](https://www.kaggle.com/code/harshsingh2209/generating-brain-mri-images-with-dc-gan)
- **Description**: Contains MRI scans labeled as:
  - `yes` — MRI images with a brain tumor  
  - `no` — MRI images without a tumor  
- Images are preprocessed and resized before training.

---

## ⚙️ Environment Setup

To run the notebook locally, set up your environment as follows:

```bash
# Clone this repository
git clone https://github.com/<your-username>/generating-brain-mri-images-with-4-Gan.git
cd generating-brain-mri-images-with-4-Gan

# Create a virtual environment (recommended)
python -m venv gan-env
source gan-env/bin/activate  # For Windows: gan-env\Scripts\activate

# Install dependencies
pip install torch torchvision torchaudio
pip install tensorflow keras
pip install matplotlib numpy pandas opencv-python tqdm
