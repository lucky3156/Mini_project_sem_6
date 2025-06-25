```markdown
# NASRGAN - Neural Architecture Search for Image Super-Resolution

This repository implements **NASRGAN**, a generative adversarial network for single image super-resolution, as part of a mini project for Semester 6. The model is built using PyTorch and utilizes a modular architecture for flexible training and evaluation.

---

## 🔍 Overview

NASRGAN is a GAN-based model trained to enhance the resolution and quality of low-resolution images using deep learning. It employs neural architecture search principles to find optimal network configurations.

---

## 📁 Project Structure

```
Mini_project_sem_6/
├── dataset.py             # Data loading and preprocessing
├── losses.py              # Loss functions for training
├── main.py                # Entry point for training and testing
├── nasrgan_model.py       # NASRGAN architecture
├── ops.py                 # Utility functions and custom layers
├── vgg19.py               # VGG model used for perceptual loss
├── environment.yml        # Conda environment specification
└── README.md              # Project documentation
```

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/lucky3156/Mini_project_sem_6.git
cd Mini_project_sem_6
```

### 2. Setup the Conda Environment

```bash
conda env create -f environment.yml
conda activate nasrgan
```

> 📌 Note: The `environment.yml` specifies PyTorch 1.1.0 and CUDA 10.0. Consider updating these if using a modern system.

---

## 🚀 Usage

### 🔧 Train the model

```bash
python main.py --mode train --epochs 100 --batch_size 16 --lr 1e-4
```

### 🧪 Test the model

```bash
python main.py --mode test --checkpoint ./checkpoints/best_model.pth
```

### 📋 Available Arguments

| Argument       | Description                         | Default       |
|----------------|-------------------------------------|---------------|
| `--mode`       | `train` or `test`                   | `train`       |
| `--epochs`     | Number of training epochs           | `100`         |
| `--batch_size` | Batch size for training/testing     | `16`          |
| `--lr`         | Learning rate                       | `1e-4`        |
| `--checkpoint` | Path to model weights               | `None`        |

---

## 📈 Evaluation Metrics

Add PSNR/SSIM evaluation in `main.py` (optional). A typical evaluation might look like:

```python
from skimage.metrics import peak_signal_noise_ratio as psnr
from skimage.metrics import structural_similarity as ssim
```

---

## ✍️ Credits

- Developed by: **[Pramodd, Toshan, Jashwanth]**
- Institution: [Chandigarh University]
- For: Mini Project, Semester 6

---

