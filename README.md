---

# **PRODIGY_CS**


### **Overview**
Welcome to **PRODIGY_CS**! This repository contains five Python-based tools for educational purposes in cybersecurity. Each tool demonstrates fundamental concepts in encryption, password security, and network analysis. The tools are designed for learning and must be used ethically, with explicit permission where required.

---

### ⚠️ **Important Ethical Notice**
The tools in this repository are for educational purposes only. Unauthorized use of tools like the keylogger or packet sniffer may violate privacy laws and ethical guidelines. Always obtain explicit consent before using these tools on any device or network you don't own.

---

### 🧰 **Tools Included:**

- **Caesar Cipher:** Encrypts and decrypts text using the Caesar Cipher algorithm with a user-specified shift.
- **Image Encryption:** Encrypts and decrypts images by applying XOR to pixel RGB values.
- **Password Complexity Checker:** Evaluates password strength based on length and character types, providing feedback.
- **Keylogger:** Logs keystrokes to a file with timestamps (requires explicit consent for use).
- **Network Packet Sniffer:** Captures and displays network packet details (requires admin privileges and network owner consent).

---

### 📋 **Prerequisites:**

- **Python 3:** Downloaded and installed from [https://www.python.org/](https://www.python.org/).
- **Required Libraries:**
  ```bash
  pip install Pillow pynput scapy
   ```
   - **Pillow:** for image encryption
   - **pynput:** for keylogger
   - **scapy:** for packet sniffer


- **Administrative Privileges:** Required for the packet sniffer (`packet_sniffer.py`).
- **Image File:** A PNG image (e.g., `input.png`) for the image encryption tool.

---

### ⚙️ **Installation:**

1. **Clone the repository:**
```bash
git clone https://github.com/deejonsen/PRODIGY-CS.git
cd PRODIGY_CS
```

2. **Install dependencies:**
```bash
pip install -r requirements.txt
```

Ensure Python 3 is installed: python --version

---

### 🚀 **Usage:**
Each tool is a standalone Python script. Run them from the command line in the repository folder.
### 1. **Caesar Cipher:**
- **File:** `caesar_cipher.py`

```bash
python caesar_cipher.py
```

- **Instructions:**
   - Choose 1 (encrypt), 2 (decrypt), or 3 (exit).
   - Enter a message and shift value (e.g., 3).
      - Example: Encrypt "Hello, World!" with shift 3 → "Khoor, Zruog!"

   - Output: Displays encrypted or decrypted text.

### 2. **Image Encryption:**
- **File:** `image_encryption.py`

```bash
python image_encryption.py
```

- **Instructions:**
   - Place a PNG image (e.g., input.png) in the folder.
   - Choose 1 (encrypt), 2 (decrypt), or 3 (exit).
   - Enter input/output file paths and a key (0-255).
      - Example: Encrypt input.png with key 42 → Creates encrypted.png.

   - Output: Saves the encrypted/decrypted image.

### 3. **Password Complexity Checker:**
- **File:** `password_checker.py`

```bash
python password_checker.py
```

- **Instructions:**
   - Enter a password.
   - Evaluate password strength
   - Receive feedback on complexity
      - Example: "P@ssw0rd!" → Strong password
      - Example: "Pass123" → Moderate strength, suggests adding special characters.
   - Output: Displays strength (Strong/Moderate/Weak) and feedback.

### 4. **Keylogger:**
- **File:** `keylogger.py`

```bash
python keylogger.py
```

- **Instructions:**
   - Press keys to log them to `keylog.txt`.
   - Press `Esc` to stop logging.
      - Example: Type "Hello" → Logs to `keylog.txt` with timestamps.
   - **Output:** Creates/appends to keylog.txt.
   - **Warning:** Use only with explicit consent on your own device.

### 5. **Network Packet Sniffer:**
- **File:** `packet_sniffer.py`

```bash
# Linux/macOS
sudo python3 packet_sniffer.py

# Windows (Run as Administrator)
python packet_sniffer.py
```

- **Instructions:**
   - Run with admin privileges (Windows: `Run as Administrator`; macOS/Linux: use `sudo`).
- Captures 10 packets and displays source/destination IPs, protocol, and payload.
   - Example: Shows packets like `Source: 192.168.1.100 -> Destination: 8.8.8.8 | Protocol: UDP`.

- **Output:** Prints packet details to the console.
- **Warning:** Use only on networks where you have explicit permission.

---

### ⚖️ Ethical Considerations:
- 🔹 **Keylogger and Packet Sniffer:** These tools can be misused to harm others. Use them only for educational purposes on your own devices/networks with explicit consent. Unauthorized use may violate privacy laws.
- 🔹 **Caesar Cipher and Image Encryption:** These are weak encryption methods for learning only, not suitable for securing sensitive data.
- 🔹 **Password Checker:** Do not store or transmit passwords entered into the tool.
- 🔹 Compliance with local laws and regulations is your responsibility

### 🤝 Contribute:
Feel free to open issues, submit pull requests, and share your own experiences and insights! Let’s make this the ultimate resource for everyone. Please follow these steps:
1. Fork the repository
2. Create a new branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m "Add your feature"`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a pull request

### Author: Dorcas Johnson

---

## 📧 Contact

For questions or issues, please [open an issue](https://github.com/deejonsen/PRODIGY_CS/issues) or contact [deejonsen23@gmail.com](deejonsen23@gmail.com).


### **Resources**  
- 🔗 [https://github.com/deejonsen/PRODIGY_CS/blob/main/PRODIGY_CS_01.md](https://github.com/deejonsen/PRODIGY_CS/blob/main/PRODIGY_CS_01.md)
-  🔗 [https://github.com/deejonsen/PRODIGY_CS/blob/main/PRODIGY_CS_02.md](https://github.com/deejonsen/PRODIGY_CS/blob/main/PRODIGY_CS_02.md)
-  🔗 [https://github.com/deejonsen/PRODIGY_CS/blob/main/PRODIGY_CS_03.md](https://github.com/deejonsen/PRODIGY_CS/blob/main/PRODIGY_CS_03.md)
-  🔗 [https://github.com/deejonsen/PRODIGY_CS/blob/main/PRODIGY_CS_04.md](https://github.com/deejonsen/PRODIGY_CS/blob/main/PRODIGY_CS_04.md)
-  🔗 [https://github.com/deejonsen/PRODIGY_CS/blob/main/PRODIGY_CS_05.md](https://github.com/deejonsen/PRODIGY_CS/blob/main/PRODIGY_CS_05.md)

---
