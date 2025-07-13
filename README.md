# SRCNN
A Study on the SRCNN Paper (Super-Resolution Convolutional Neural Network)

## 📄 Paper
**Link**: [https://arxiv.org/abs/1501.00092](https://arxiv.org/abs/1501.00092)

---

## 📌 Project Objective
This repository reproduces the SRCNN model and validates its results on:
- **Y-channel only (luminance)**
- **RGB channels**
Compare results with the original paper to verify consistency of PSNR/Bicubic values.

---

## 🧪 Key Features
- Fully reimplemented SRCNN in **PyTorch** following paper architecture  
- Training conducted separately for:
  - ✅ **Y-channel only** (grayscale luminance)
  - ✅ **Full RGB**  
- Patch-based training from **T91 dataset**  
- Evaluation on **Set5** with average PSNR comparison  
- Visualization of super-resolved images (Y and RGB)  
- Bicubic baseline vs. SRCNN model comparison for both input types  

---

## 📊 Results (Set5 Average PSNR)

| Scale | Method        | Bicubic (Y) | SRCNN (Paper, Y) | Mine (Y) |
|-------|---------------|-------------|------------------|----------|
| ×2    | PSNR (dB)     | 33.66       | 36.66            | 34.61    | 
| ×3    | PSNR (dB)     | 30.39       | 32.75            | 30.89    | 
| ×4    | PSNR (dB)     | 28.42       | 30.49            | 28.95    |
