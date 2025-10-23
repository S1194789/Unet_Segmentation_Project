# 🌊 U-Net Image Segmentation — Sea & Sky Classification

> A deep learning project implementing **U-Net architecture** for image segmentation using **infrared datasets**,  
> developed as part of the *Deep Learning* module in the **Erasmus Mundus MIR Programme** at Université de Toulon (2025).

---

## 🎯 Objective

The objective of this project was to build and train a **U-Net convolutional neural network**  
to segment infrared images into *sea* and *sky* regions.  
The model was implemented from scratch using **PyTorch**, with full control over  
the architecture, training process, and metric evaluation.

---

## 📂 Repository Structure

| Path | Description |
|------|--------------|
| **Unet_Hyejoo_kwon.ipynb** | Main training notebook with U-Net implementation, loss tracking, and visualization |
| **UNET_Hyejoo_Kwon.pdf** | Project report with results, analysis, and segmentation outputs |
| **unet_model_final_Hyejoo_kwon.pth** | Saved model weights after 10 epochs of training |
| **Questions_DL_Kwon.xlsx** | Theory and quiz responses for the Deep Learning module |
| **README.md** | Project overview and documentation (this file) |

---

## ⚙️ Model Architecture

- **Encoder:** Convolution + ReLU + MaxPool layers to extract deep spatial features  
- **Decoder:** Transposed convolutions for upsampling and skip connections for spatial recovery  
- **Loss Function:** Binary Cross-Entropy + Dice Coefficient  
- **Optimizer:** Adam (lr = 1e-4)  
- **Evaluation Metric:** Dice Score  

---

## 📊 Results

| Epoch | Train Loss | Validation Loss | Dice Score |
|:------|:-----------:|:----------------:|:-----------:|
| 0 | — | — | 0.4872 |
| 1 | 0.0879 | 0.0291 | 0.9789 |
| 5 | 0.0153 | 0.0114 | 0.9925 |
| 10 | 0.0123 | 0.0099 | **0.9953** ✅ |

**Segmentation Outcome:**  
The model successfully separated *sea* and *sky* in infrared images with minimal boundary error,  
achieving near-perfect Dice similarity after 10 epochs.

---

## 💡 Key Learnings

- Fixed critical bugs in **loss accumulation** (`loss.item()` for numeric conversion)  
- Resolved **channel mismatch** errors in `ConvTranspose2d` skip connections  
- Corrected **accuracy misinterpretation** between predicted and ground-truth masks  
- Understood the role of **proper normalization and loss scaling** for stable convergence  

---

## 🧩 Tools & Libraries

- **PyTorch** · NumPy · Matplotlib  
- **Google Colab / Jupyter Notebook**  
- **Infrared Image Dataset** (custom sea-sky segmentation)  

---

## 🧠 Learning Outcomes

| Concept | Skill Gained |
|----------|--------------|
| CNN Architectures | Designed and debugged U-Net from scratch |
| Image Segmentation | Applied encoder-decoder design with skip connections |
| Model Debugging | Solved channel and loss computation issues |
| Metric Evaluation | Implemented Dice score for performance tracking |

---

## 👩‍💻 Author

**Hyejoo Kwon**  
📍 Erasmus Mundus Master’s in *Marine & Maritime Intelligent Robotics (MIR)*  
📅 Submitted: January 2025  

🔗 [GitHub Repository](https://github.com/S1194789/Unet_Segmentation_Project)
