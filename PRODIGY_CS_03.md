---

# 🔐 Password Complexity Checker

## 📖 Task Overview

This task is a Python-based command-line tool designed to evaluate the strength of user passwords. It checks passwords against standard complexity requirements; including length, character diversity, and symbol usage, and provides real-time feedback to help users improve password strength.

> 🛡️ A strong password is your first line of defense against unauthorized access. This tool promotes safer practices through instant feedback and education.

---

## ✨ Features

- ✅ Detects password length
- 🔡 Checks for lowercase letters
- 🔠 Checks for uppercase letters
- 🔢 Checks for digits
- 🔣 Checks for special characters (e.g. `!@#$%^&*`)
- 📊 Ranks strength as **Weak**, **Moderate**, or **Strong**
- 📢 User-friendly feedback with emoji indicators

---

## 🛠️ Tech Stack

| Component        | Description                                |
|------------------|--------------------------------------------|
| **Language**     | Python (≥ v3.13.5)                            |
| **Type**         | Console-based command-line application     |
| **Editor**       | Visual Studio Code (recommended)           |
| **Environment**  | Windows OS (tested)                        |

---

## 💻 Installation & Setup

### 🔹 Step 1: Install Python

- Download Python from [https://www.python.org/downloads](https://www.python.org/downloads)
- Run the installer and ✅ check **"Add Python to PATH"**
- Confirm install via Command Prompt:
  ```bash
  python --version
  ```

### 🔹 Step 2: Set Up Your Project

- Create a folder: `PasswordChecker`
- Inside the folder, create a file: `password_checker.py`
- Open in VS Code or any code editor

---

## 📄 Sample Code

```python
import string

def check_password_strength(password):
    length_ok = len(password) >= 8
    has_lower = any(char.islower() for char in password)
    has_upper = any(char.isupper() for char in password)
    has_digit = any(char.isdigit() for char in password)
    has_special = any(char in string.punctuation for char in password)

    score = sum([length_ok, has_lower, has_upper, has_digit, has_special])

    print("\n🔍 Password Analysis:")
    print(f"- Length ≥ 8: {'✅' if length_ok else '❌'}")
    print(f"- Contains lowercase: {'✅' if has_lower else '❌'}")
    print(f"- Contains uppercase: {'✅' if has_upper else '❌'}")
    print(f"- Contains digit: {'✅' if has_digit else '❌'}")
    print(f"- Contains special character: {'✅' if has_special else '❌'}")

    if score == 5:
        print("\n🔐 Password Strength: STRONG 💪")
    elif score >= 3:
        print("\n🛡️ Password Strength: MODERATE ⚠️")
    else:
        print("\n🚫 Password Strength: WEAK ❌")

# Prompt user for a password
user_input = input("Enter your password to analyze: ")
check_password_strength(user_input)
```

---

## 🧪 Sample Test Case

| Password           | Strength  | Reason                                                             |
|--------------------|-----------|--------------------------------------------------------------------|
| `abc123`           | Weak      | Short, lacks uppercase and special character                       |
| `Abc123!`          | Moderate  | Meets most criteria but shorter length                             |
| `P@ssW0rd2023!`    | Strong    | Long, mixed case, includes digits and special characters           |
| `Qwerty!`          | Weak      | Short, lacks digit                                                 |
| `SecurePass123!`   | Strong    | Meets all 5 complexity checks                                      |

---

<img width="1208" height="548" alt="Screenshot 2025-07-13 231302" src="https://github.com/user-attachments/assets/538f19fb-00b8-4e00-a6fd-ff60c4ac3014" />
<img width="1158" height="702" alt="Screenshot 2025-07-13 231231" src="https://github.com/user-attachments/assets/6b0c2be7-0a16-4470-be69-aa33ee3bef2c" />
<img width="1366" height="719" alt="Screenshot 2025-07-13 231203" src="https://github.com/user-attachments/assets/942ab908-0580-4607-bb65-fba0641a6c4b" />
<img width="1097" height="497" alt="Screenshot 2025-07-10 190011" src="https://github.com/user-attachments/assets/8519bcd4-6a66-4516-a476-283bb42e7761" />
