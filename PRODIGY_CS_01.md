---

# 🛡️ Caesar Cipher: Text Encryption & Decryption Tool

## 🔍 Task Overview
This project is a Python-based implementation of the classic Caesar Cipher encryption algorithm. It enables users to encrypt and decrypt text messages using a numeric shift value. Caesar Cipher is a simple substitution cipher where each letter is replaced by another letter a fixed number of positions down the alphabet.

---

## 🎯 Features
- Encrypt any plain text message by shifting characters
- Decrypt an encrypted message with the correct shift
- Preserves capitalization and ignores non-alphabetic symbols (e.g., punctuation, digits)
- Accepts user input via console for flexible use
- Beginner-friendly structure for learning basic cryptography

## 🧠 How It Works
1. Each alphabetic character is shifted based on a user-supplied integer.
2. Capital letters (`A–Z`) and lowercase (`a–z`) are handled separately to preserve case.
3. Characters like spaces, numbers, punctuation remain unchanged.
4. Shift wraps around the alphabet using modulo arithmetic:
   - `"Z"` with shift 1 becomes `"A"`

## 🔧 Tech Stack

| Component        | Description                                             |
|------------------|---------------------------------------------------------|
| **Language**     | Python (≥ v3.13.5) – core programming language              |
| **Runtime**      | Terminal / Command Prompt – executes `.py` scripts      |
| **Editor**       | Visual Studio Code – used to write and edit the code    |
| **Environment**  | Windows OS – primary platform used for development      |
| **Application Type** | Console-based – no GUI, ran purely from the terminal |

---

## 💻🛠️ Installation & Setup

## (Windows)

To get started with this project, you'll need **Python** and **Visual Studio Code (VS Code)** installed on your system.

### 🐍 Step 1: Install Python

**1. Download Python**
- Go to the official website: [https://www.python.org/downloads](https://www.python.org/downloads)
- Click the **“Download Python 3.13.5”** button for Windows.

**2. Run the Installer**
- Double-click the downloaded `.exe` file.
- ✅ Check the box that says **"Add Python to PATH"**, this is crucial.
- Click **"Install Now"** and wait for the process to complete.

**3. Verify Installation**
- Open **Command Prompt** (`Win + R`, then type `cmd` and press Enter).
- Type:
  ```bash
  python --version
  ```
  You should see output like:
  ```
  Python 3.13.5
  ```

### 💻 Step 2: Install Visual Studio Code

**1. Download VS Code**
- Visit: [https://code.visualstudio.com](https://code.visualstudio.com)
- Click **"Download for Windows"**.

**2. Run the Installer**
- Launch the downloaded `.exe` file.
- During setup, ✅ select these options:
  - **"Add to PATH"**
  - **"Add 'Open with Code' to Windows Explorer"**
  - **"Register Code as default editor"**
- Click **"Next"** and finish installation.

**3. Launch VS Code**
- Open VS Code from the Start Menu.
- You’ll land on the Welcome screen.


### 🔌 Step 3: Enable Python Support in VS Code

**1. Open Extensions Panel**
- Click the Extensions icon on the left sidebar (or press `Ctrl + Shift + X`).

**2. Search for “Python”**
- Locate the extension published by **Microsoft**.
- Click **Install**.

This adds syntax highlighting, autocompletion, linting, and execution tools for Python.


You can now:
- Write your Caesar Cipher code in `.py` files
- Run your project inside VS Code's integrated terminal
- Begin experimenting with encryption and decryption 🚀

---

## 📝 Create a Python File (.py)
**Option A: Using Notepad**
- Open Notepad.
- Paste your Python code (it's written below).
- Go to File > Save As.
- Name it caesar_cipher.py
- In the Save as type dropdown, choose All Files.
- Save it with .py extension (i.e., caesar_cipher.py) in a known folder like Documents.

**Option B: Using Visual Studio Code (VS Code)**
- Launch VS Code and open a new file
- Save it as caesar_cipher.py.
- You can run it inside VS Code using the built-in terminal.


## 🔐 Code (Functions to Encrypt and Decrypt)
- Save the code into a file named `caesar_cipher.py`
```python
def caesar_cipher(text, shift, mode='encrypt'):
    result = ''
    for char in text:
        if char.isalpha():
            base = ord('A') if char.isupper() else ord('a')
            shifted = (ord(char) - base + (shift if mode == 'encrypt' else -shift)) % 26
            result += chr(shifted + base)
        else:
            result += char
    return result

# User interaction
mode = input("Type 'encrypt' or 'decrypt': ").strip().lower()
message = input("Enter your message: ")
shift = int(input("Enter shift value: "))

output = caesar_cipher(message, shift, mode)
print(f"Result ({mode}ed):", output)
```

## 🧪 Sample Usage 1

```
Type 'encrypt' or 'decrypt': encrypt
Enter your message: Hello, World!
Enter shift value: 3
Result (encrypted): Khoor, Zruog!
```

```
Type 'encrypt' or 'decrypt': decrypt
Enter your message: Khoor, Zruog!
Enter shift value: 3
Result (decrypted): Hello, World!
```

## 🧪 Sample Usage 2

```
Type 'encrypt' or 'decrypt': encrypt
Enter your message: Hacker Dorcas Johnson.
Enter shift value: 3
Result (encrypted): Kdfnhu Grufdv Mrkqvrq.
```

```
Type 'encrypt' or 'decrypt': decrypt
Enter your message: Kdfnhu Grufdv Mrkqvrq
Enter shift value: 3
Result (decrypted): Hacker Dorcas Johnson.
```

---
<img width="1289" height="719" alt="Screenshot 2025-07-13 155019" src="https://github.com/user-attachments/assets/95dae2b1-8c67-4428-8bbd-7e4edb923556" />
<img width="1180" height="720" alt="Screenshot 2025-07-13 154333" src="https://github.com/user-attachments/assets/44d34e71-525a-4df5-b59f-97e1f936f217" />
<img width="1014" height="595" alt="Screenshot 2025-07-13 144514" src="https://github.com/user-attachments/assets/59b0b4ad-4c42-41c2-81d4-3ba5437a9afb" />
<img width="935" height="681" alt="Screenshot 2025-07-13 144352" src="https://github.com/user-attachments/assets/ba763c9f-467c-4f3c-b031-1e5e30bb612a" />
<img width="1366" height="462" alt="Screenshot 2025-07-13 140048" src="https://github.com/user-attachments/assets/93b3fda4-d4a1-462b-8a57-9e4e83096ecf" />
<img width="1366" height="732" alt="Screenshot 2025-07-13 135951" src="https://github.com/user-attachments/assets/b16c3368-a638-4083-9846-eeb521708104" />
<img width="1358" height="722" alt="Screenshot 2025-07-13 135848" src="https://github.com/user-attachments/assets/e277ef42-793a-4d55-9559-5a9aff400b57" />
