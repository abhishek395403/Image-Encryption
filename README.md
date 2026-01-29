# 🔐 Image Encryption & Decryption Pipeline

A robust and secure **Image Encryption & Decryption system** implemented in Python using Jupyter Notebook.  
This project combines **cryptographic techniques and chaotic maps** to protect images from unauthorized access.

---

## 📌 Overview

The notebook `ency (1).ipynb` implements a multi-layered image encryption pipeline using:

- Color space transformation (RGB ↔ HSV)
- Pixel permutation
- XOR-based encryption
- Angle-based scrambling
- Arnold’s Cat Map (chaotic encryption)

The encrypted image can be perfectly restored using the corresponding inverse operations.

---

## ✨ Features

### 1️⃣ Color Space Conversion
- Converts RGB images to HSV color space
- Applies **180° hue rotation** for encryption
- Inverse hue rotation during decryption
- Converts back to RGB after decryption

---

### 2️⃣ Image Encryption
- **Row/Column Permutation**
  - Randomly permutes pixel positions using a fixed seed
- **XOR Encryption**
  - Uses random keystream for encryption
- Encryption keys are saved for correct decryption

---

### 3️⃣ Advanced Scrambling
- **Angle-based Scrambling**
  - Generates shuffle sequence using trigonometric functions
- **Arnold’s Cat Map**
  - Chaotic permutation for enhanced security
  - Multiple iterations supported
- **Inverse Arnold’s Cat Map**
  - Restores original image during decryption

---

### 4️⃣ Decryption & Recovery
- Inverse Arnold transformation
- Descrambling
- Undo XOR encryption
- Restore row/column permutations
- Apply inverse hue rotation
- Recover original image with no loss

---

## 🔁 Encryption–Decryption Workflow

Original Image
↓
RGB → BGR → HSV Conversion → Hue Rotation
↓
Encrypt (Permutation + XOR)
↓
Scramble (Angle-based)
↓
Arnold’s Cat Map
↓
Inverse Arnold’s Map
↓
Descramble
↓
Decrypt (Undo XOR & Permutation)
↓
Inverse Hue Rotation → HSV → RGB
↓
Restored Image


---

## 🧠 Key Functions

| Function Name | Description |
|---------------|-------------|
| `encrypt_image()` | Encrypts image using permutation and XOR |
| `decrypt_image()` | Decrypts image by reversing encryption |
| `scrambling()` | Generates shuffle sequence |
| `scramble_image()` | Scrambles encrypted image |
| `descrambling()` | Restores scrambled image |
| `arnold_cat_map()` | Applies chaotic permutation |
| `inverse_arnold_cat_map()` | Reverses Arnold map |
| `hue_rotate_180()` | HSV hue rotation for encryption |
| `hue_inverse_180()` | Reverses hue rotation |

---

## 🧰 Requirements

### 📦 Libraries Used
- NumPy
- OpenCV (cv2)
- Matplotlib
- Scikit-image

### 🔧 Installation
```bash
pip install numpy opencv-python matplotlib scikit-image
▶️ How to Run
Clone the repository

git clone https://github.com/abhishek395403/Image-Encryption.git
Open the notebook

jupyter notebook "ency (1).ipynb"
Run cells sequentially

📁 Project Structure
Image-Encryption/
│
├── ency (1).ipynb
├── README.md
└── sample_images/
🎯 Applications
Secure image transmission

Medical image protection

Military & defense communication

Digital watermarking

Chaos-based cryptography research

🚀 Future Enhancements
Video encryption support

GUI interface

AES/RSA hybrid encryption

Performance analysis

👨‍💻 Author
Abhishek Kumar
GitHub: https://github.com/abhishek395403


