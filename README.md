# Brain Tumor Segmentation: Swin-UNETR vs. nnUNet vs. U-Net  
**BraTS 2023 (100 Samples)**  
*AMS 691: Medical Image Analysis, Stony Brook University | Spring 2025*

---

## Abstract
Benchmarked **Swin-UNETR (transformer)**, **nnUNet**, and **U-Net** on **100 BraTS 2023 MRI volumes** using **MONAI**.  
Trained on **T1, T1ce, T2, FLAIR** with **DiceCE loss**.  
Evaluated **accuracy, boundary precision, inference time, memory**.

> **nnUNet**: Best accuracy (**Dice 0.152**, **HD95 40.79**)  
> **Swin-UNETR**: Competitive (**Dice 0.1399**) but **25× slower**  
> **U-Net**: Fastest (0.05s) but weak (**Dice 0.1021**)  

Open-source pipeline for **low-data, low-resource** clinical AI.

---

## Results (5-Fold Cross-Validation)
| Model       | Dice ↑ | HD95 ↓ | ASD ↓  | Inf. Time ↓ | Memory |
|-------------|--------|--------|--------|-------------|--------|
| **nnUNet**  | **0.152** | **40.79** | **17.12** | 0.87s     | 1.57MB |
| Swin-UNETR  | 0.1399 | 53.83  | 20.85  | 1.24s     | 1.57MB |
| U-Net       | 0.1021 | 100.70 | 48.31  | **0.05s** | 1.57MB |

---

## Run the Code
```bash
pip install -r requirements.txt
jupyter notebook Tumor-Segmentation-BraTS.ipynb
