# SRCNN
A Study on the SRCNN Paper (Super-Resolution Convolutional Neural Network)

## 📄 Paper
**Link**: [https://arxiv.org/abs/1501.00092](https://arxiv.org/abs/1501.00092)

**Datasets Used**:
- [Set5 (Test Set)] [https://paperswithcode.com/dataset/set5](https://www.kaggle.com/datasets/ll01dm/set-5-14-super-resolution-dataset)
- [T91 (Training Set)] [https://github.com/hoycg/NTIRE2017/blob/master/README.md#t91-dataset](https://www.kaggle.com/datasets/ll01dm/t91-image-dataset)
  
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

| Scale | Method        | Bicubic (Paper, Y) | SRCNN (Paper, Y) | Bicubic (Mine, Y) | SRCNN (Mine, Y) |
|-------|---------------|--------------------|------------------|-------------------|-----------------|
| ×2    | PSNR (dB)     | 33.66              | 36.66            | 32.79             | 34.61           | 
| ×3    | PSNR (dB)     | 30.39              | 32.75            | 29.32             | 30.89           | 
| ×4    | PSNR (dB)     | 28.42              | 30.49            | 27.31             | 28.95           |

## 📊 Results ("Butterfly" image from Set5 PSNR)

| Scale | Method        | Bicubic (Paper, RGB) | SRCNN (Paper, RGB) | Bicubic (Mine, RGB) | SRCNN (Mine, RGB) |
|-------|---------------|----------------------|--------------------|---------------------|-------------------|
| ×3    | PSNR (dB)     | 24.04                | 27.95              | 23.01               | 25.75             |

📎 *Note: SRCNN was originally designed for the Y (luminance) channel. 
RGB evaluation was performed only at scale ×3 in this project to examine full-color reconstruction performance.*

---

## 📸 Visual Comparison (RGB, "Butterfly" image from Set5 with an upscaling factor 3)
| HR RGB | Bicubic (Paper, RGB) | SRCNN (Paper, RGB) | Bicubic (Mine, RGB) | SRCNN (Mine, RGB) |
|--------|----------------------|--------------------|---------------------|-------------------|
| <img width="232" height="230" src="https://github.com/user-attachments/assets/335bb81a-215b-4a81-a77a-5628bd4a39f6" /> | <img width="179" height="182" src="https://github.com/user-attachments/assets/d814d356-b2ae-42b9-b702-2e2b61b0ef59" /> | <img width="181" height="182" src="https://github.com/user-attachments/assets/00555592-97ec-4d1c-bd8b-aa30704c9f35" /> | <img width="230" height="230" src="https://github.com/user-attachments/assets/2b15b843-5f74-487f-80d4-8e87dbceb68c" /> | <img width="230" height="230" src="https://github.com/user-attachments/assets/7667994c-7b25-4de0-b26c-6577b2f93dd8" /> |
