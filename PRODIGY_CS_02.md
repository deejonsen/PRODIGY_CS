---

# 🔐 Pixel Manipulation Image Encryption Tool

## 📖 Task Overview

This task is a beginner-friendly image encryption and decryption tool developed in Python. It uses **Pixel Manipulation** techniques to scramble and restore images by modifying their RGB values. The tool applies a simple mathematical operation to each pixel, effectively transforming the image into unreadable form until decrypted with the same offset.

> 📌 Encryption here is not industry-grade. It’s designed for learning purposes, lightweight use cases, and understanding how digital images work under the hood.

---

## ⚙️ Features

- 🔒 Encrypts image by applying an offset to pixel RGB values
- 🔓 Decrypts image by reversing the pixel transformation
- 🖼️ Supports `.jpg`, `.png`, and other Pillow-supported formats
- ✅ Preserves image dimensions and metadata
- 🧑‍💻 Console-based user interaction for mode selection

---

## 🛠️ Tech Stack

| Component        | Description                                |
|------------------|--------------------------------------------|
| **Language**     | Python 3.13.5                                |
| **Library**      | Pillow (`pip install pillow`)              |
| **Editor**       | Visual Studio Code           |
| **Environment**  | Windows OS (tested)                        |
| **Type**         | Console App                                |

---

## 🧰 Installation Guide (Windows)

### 1️⃣ Install Python

- Download from [python.org](https://www.python.org/downloads)
- Run the installer and **check “Add Python to PATH”**
- Verify with:
  ```bash
  python --version
  ```

### 2️⃣ Install Pillow (Python Imaging Library)

Open Command Prompt or VS Code terminal:
```bash
pip install pillow
```

### 3️⃣ Install VS Code (Optional but Recommended)

- Download from [https://code.visualstudio.com](https://code.visualstudio.com)
- Install the **Python extension** via Extensions tab

---

## 📝 Usage Instructions

1. **Place your image** (e.g. `screen.png`) in the same folder as `image_cipher.py`
2. Run the script from terminal or VS Code:
   ```bash
   python image_cipher.py
   ```
3. Follow the prompts:
   ```
   Type 'encrypt' or 'decrypt': encrypt
   Enter input image filename (e.g. screen.png): screen.png
   Enter output image filename (e.g. encrypted.png): encrypted.png
   Enter offset value (e.g. 50): 50
   ```

4. To decrypt later, use:
   ```
   Type 'encrypt' or 'decrypt': decrypt
   Input image filename: encrypted.png
   Output image filename: decrypted.png
   Offset: 50
   ```

✅ The decrypted image should visually match the original.

---

## 🧠 Sample Code

```python
from PIL import Image

def encrypt_image(path, output_path, offset=50):
    img = Image.open(path)
    pixels = img.load()
    for i in range(img.width):
        for j in range(img.height):
            r, g, b = pixels[i, j]
            pixels[i, j] = ((r + offset) % 256, (g + offset) % 256, (b + offset) % 256)
    img.save(output_path)
    print(f"Image encrypted and saved as {output_path}")

def decrypt_image(path, output_path, offset=50):
    img = Image.open(path)
    pixels = img.load()
    for i in range(img.width):
        for j in range(img.height):
            r, g, b = pixels[i, j]
            pixels[i, j] = ((r - offset) % 256, (g - offset) % 256, (b - offset) % 256)
    img.save(output_path)
    print(f"Image decrypted and saved as {output_path}")

# User interaction
mode = input("Type 'encrypt' or 'decrypt': ").lower()
input_path = input("Enter input image filename: ")
output_path = input("Enter output image filename: ")
offset = int(input("Enter offset value: "))

if mode == 'encrypt':
    encrypt_image(input_path, output_path, offset)
elif mode == 'decrypt':
    decrypt_image(input_path, output_path, offset)
else:
    print("Invalid mode selected.")
```

---

## 🔬 Sample Test Case

```python
def test_image_encryption_decryption():
    encrypt_image("screen.png", "encrypted.png", offset=50)
    decrypt_image("encrypted.png", "decrypted.png", offset=50)

    # Optional: Compare pixel-wise if decrypted image matches original
```

---<img width="1362" height="715" alt="Screenshot 2025-07-13 223654" src="https://github.com/user-attachments/assets/e8c3bf63-e43c-4a4e-98f3-fb42a94b2f7a" />
<img width="1366" height="659" alt="Screenshot 2025-07-13 214802" src="https://github.com/user-attachments/assets/6350aa37-17ca-405d-bf39-27511c0fc47a" />
<img width="1366" height="722" alt="Screenshot 2025-07-13 214743" src="https://github.com/user-attachments/assets/acc4a506-843e-4d56-aa3f-ec891da4195d" />
<img width="1366" height="702" alt="Screenshot 2025-07-13 214436" src="https://github.com/user-attachments/assets/c9dea422-a1d1-4730-8b5e-25a4a021c06c" />
<img width="1366" height="710" alt="Screenshot 2025-07-13 214411" src="https://github.com/user-attachments/assets/c96c5d77-c0d6-4146-a826-ca0843221e7a" />
<img width="1342" height="691" alt="Screenshot 2025-07-13 214321" src="https://github.com/user-attachments/assets/851d4b48-9a55-499d-b921-a3e49f9b977e" />
<img width="720" height="1560" alt="screen" src="https://github.com/user-attachments/assets/3f637b45-7057-4b23-82f7-546115875dc5" />
<img width="720" height="1560" alt="encrypted" src="https://github.com/user-attachments/assets/f0deeb4d-d903-46ed-b203-511fc165ca58" />
<img width="720" height="1560" alt="decrypted" src="https://github.com/user-attachments/assets/1530899d-ce59-46fa-9980-554e31db7fd2" />
<img width="1106" height="576" alt="Screenshot 2025-07-10 185955" src="https://github.com/user-attachments/assets/7f904a38-771f-47ba-8c1f-a174be45e47c" />


