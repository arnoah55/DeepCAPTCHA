# 🧠 DeepCAPTCHA

DeepCAPTCHA is an OCR system built using a **CRNN model** trained with **CTC loss** to decode distorted CAPTCHA images **without segmentation**. This project showcases a robust deep learning pipeline for recognizing variable-length text sequences from noisy image data.



---

## 🚀 Highlights

- ✅ **CRNN (CNN + BiLSTM)** architecture with **CTC loss** for unsegmented sequence prediction.
- 🔄 **Data augmentation** via `ImageDataGenerator` for generalization on small datasets.
- 📦 End-to-end pipeline using **TensorFlow**, including a **custom CTCLayer**.
- ⚙️ Optimized training using `tf.data` pipelines and **early stopping**.

---

## 🧱 Architecture

- **CNN**: Extracts visual features from CAPTCHA images.
- **BiLSTM**: Models character-level dependencies across time steps.
- **CTC Loss**: Enables training without aligned target sequences.
- **CTCLayer**: Custom layer to handle the CTC computation during training.

---

## 📊 Dataset

- Started with **1000 labeled CAPTCHA images**.
- Expanded to **5000+ samples** using data augmentation:
  - **Rotation**
  - **Width/height shift**
  - **Zoom**
  - **Noise injection (optional)**

1. Clone the repository:
   ```bash
   git clone https://github.com/arnoah55/DeepCAPTCHA.git
   cd DeepCAPTCHA
