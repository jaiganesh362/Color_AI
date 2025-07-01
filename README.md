# Color_AI

# 🎨 Image Colorization with GAN (Pix2Pix) | TensorFlow

This project demonstrates how to colorize black-and-white (grayscale) images automatically using a **conditional Generative Adversarial Network (cGAN)**, inspired by the Pix2Pix architecture, implemented in **TensorFlow**.

---

## 📌 Project Overview

> ✅ **Goal:**  
> Given a grayscale image, predict realistic color channels (*a*, *b*) in Lab color space.

> ✅ **Use Case:**  
> Historical photo restoration, enhancing old archives, or creative colorization.

---

## ⚙️ How It Works

- **Input:** Grayscale image (*L* channel).
- **Generator:** A U-Net model learns to predict the missing *a,b* channels.
- **Discriminator:** A PatchGAN checks if the generated color image is realistic by looking at local patches.
- **Loss:** Combination of adversarial loss (**GAN loss**) + L1 loss for pixel-wise similarity.

---

## 🧩 Model Architecture

- **Generator:** U-Net (Encoder-Decoder with skip connections)
- **Discriminator:** PatchGAN (classifies 70x70 patches as real or fake)

---

## 🗂️ Dataset

- You can use **CIFAR-10**, **ImageNet**, or your own dataset.
- Images are converted to **Lab color space**:
  - Input: L channel (grayscale)
  - Target: a,b channels (color)

---
