---

# **PRODIGY_CS**


## **Overview**
Welcome to **PRODIGY_CS**! This repository contains five Python-based tools for educational purposes in cybersecurity. Each tool demonstrates fundamental concepts in encryption, password security, and network analysis. The tools are designed for learning and must be used ethically, with explicit permission where required.

## **Tools Included:**

- **Caesar Cipher:** Encrypts and decrypts text using the Caesar Cipher algorithm with a user-specified shift.
- **Image Encryption:** Encrypts and decrypts images by applying XOR to pixel RGB values.
- **Password Complexity Checker:** Evaluates password strength based on length and character types, providing feedback.
- **Keylogger:** Logs keystrokes to a file with timestamps (requires explicit consent for use).
- **Network Packet Sniffer:** Captures and displays network packet details (requires admin privileges and network owner consent).

## **Prerequisites:**

- **Python 3:** Download and install from python.org.
Libraries:
Pillow: pip install Pillow (for image encryption)
pynput: pip install pynput (for keylogger)
scapy: pip install scapy (for packet sniffer)


Administrative Privileges: Required for the packet sniffer (packet_sniffer.py).
Image File: A PNG image (e.g., input.png) for the image encryption tool.

Installation

Clone the repository:git clone https://github.com/yourusername/cybersecurity-tools.git
cd cybersecurity-tools


Install dependencies:pip install Pillow pynput scapy


Ensure Python 3 is installed:python --version



Usage
Each tool is a standalone Python script. Run them from the command line in the repository folder.
1. Caesar Cipher

File: caesar_cipher.py
Run:python caesar_cipher.py


Instructions:
Choose 1 (encrypt), 2 (decrypt), or 3 (exit).
Enter a message and shift value (e.g., 3).
Example: Encrypt "Hello, World!" with shift 3 → "Khoor, Zruog!"


Output: Displays encrypted or decrypted text.

2. Image Encryption

File: image_encryption.py
Run:python image_encryption.py


Instructions:
Place a PNG image (e.g., input.png) in the folder.
Choose 1 (encrypt), 2 (decrypt), or 3 (exit).
Enter input/output file paths and a key (0-255).
Example: Encrypt input.png with key 42 → Creates encrypted.png.


Output: Saves the encrypted/decrypted image.

3. Password Complexity Checker

File: password_checker.py
Run:python password_checker.py


Instructions:
Enter a password.
Example: "Pass123" → Moderate strength, suggests adding special characters.


Output: Displays strength (Strong/Moderate/Weak) and feedback.

4. Keylogger

File: keylogger.py
Run:python keylogger.py


Instructions:
Press keys to log them to keylog.txt.
Press 'Esc' to stop.
Example: Type "Hello" → Logs to keylog.txt with timestamps.


Output: Creates/appends to keylog.txt.
Warning: Use only with explicit consent on your own device.

5. Network Packet Sniffer

File: packet_sniffer.py
Run:sudo python packet_sniffer.py  # Requires admin privileges


### Instructions:
Run with admin privileges (Windows: Run as Administrator; macOS/Linux: use sudo).
Captures 10 packets and displays source/destination IPs, protocol, and payload.
Example: Shows packets like "Source: 192.168.1.100 -> Destination: 8.8.8.8 | Protocol: UDP".


### Output: Prints packet details to the console.
### Warning: Use only on networks where you have explicit permission.

### Ethical Considerations:

Keylogger and Packet Sniffer: These tools can be misused to harm others. Use them only for educational purposes on your own devices/networks with explicit consent. Unauthorized use may violate privacy laws.
Caesar Cipher and Image Encryption: These are weak encryption methods for learning only, not suitable for securing sensitive data.
Password Checker: Do not store or transmit passwords entered into the tool.

### Contribute:
Feel free to open issues, submit pull requests, and share your own experiences and insights! Let’s make this the ultimate resource for everyone.

### Author: Dorcas Johnson

---



# Cybersecurity Tools Repository

![Cybersecurity](https://img.shields.io/badge/Field-Cybersecurity-blue) ![Python](https://img.shields.io/badge/Language-Python-green) ![Educational](https://img.shields.io/badge/Purpose-Educational-orange)

This repository contains Python-based cybersecurity tools designed for educational purposes. Each tool demonstrates fundamental concepts in encryption, password security, and network analysis. **Use these tools responsibly and only with explicit permission where required.**

## ⚠️ Important Ethical Notice

**The tools in this repository are for educational purposes only.** Unauthorized use of tools like the keylogger or packet sniffer may violate privacy laws and ethical guidelines. Always obtain explicit consent before using these tools on any device or network you don't own.

## 🧰 Tools Included

1. **Caesar Cipher**  
   Encrypts/decrypts text using a shift cipher algorithm
2. **Image Encryption**  
   Encrypts/decrypts images using XOR operations on pixel values
3. **Password Complexity Checker**  
   Evaluates password strength and provides feedback
4. **Keylogger**  
   Logs keystrokes with timestamps (requires explicit consent)
5. **Network Packet Sniffer**  
   Captures and displays network packet details (requires admin privileges)

## 📋 Prerequisites

- Python 3.x ([Download](https://python.org))
- Required libraries:
  ```bash
  pip install Pillow pynput scapy
  ```
- Administrative privileges for packet sniffer
- PNG image file for image encryption tool

## ⚙️ Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/cybersecurity-tools.git
   cd cybersecurity-tools
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## 🚀 Usage

### 1. Caesar Cipher (`caesar_cipher.py`)
```bash
python caesar_cipher.py
```
- Encrypt/decrypt text with a shift value
- Example: Encrypt "Hello" with shift 3 → "Khoor"

### 2. Image Encryption (`image_encryption.py`)
```bash
python image_encryption.py
```
- Encrypt/decrypt PNG images using a numeric key
- Place `input.png` in folder before running
- Example: Encrypt with key 42 → Creates `encrypted.png`

### 3. Password Complexity Checker (`password_checker.py`)
```bash
python password_checker.py
```
- Evaluate password strength
- Receives feedback on complexity
- Example: "P@ssw0rd!" → Strong password

### 4. Keylogger (`keylogger.py`)
```bash
python keylogger.py
```
- Logs keystrokes to `keylog.txt`
- Press `Esc` to stop logging
- **Requires explicit consent for use**

### 5. Network Packet Sniffer (`packet_sniffer.py`)
```bash
# Linux/macOS
sudo python3 packet_sniffer.py

# Windows (Run as Administrator)
python packet_sniffer.py
```
- Captures network packets
- Displays source/destination IPs and protocols
- **Requires admin privileges and network owner consent**

## ⚖️ Ethical Considerations

- **Keylogger & Packet Sniffer:** Use only with explicit consent on your own devices/networks
- **Caesar Cipher & Image Encryption:** Weak methods for educational purposes only
- **Password Checker:** Never store or transmit passwords processed by this tool
- Compliance with local laws and regulations is your responsibility

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m "Add your feature"`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a pull request

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📧 Contact

For questions or issues, please [open an issue](https://github.com/yourusername/cybersecurity-tools/issues) or contact [your email].

---

**Disclaimer:** These tools are for educational purposes only. The developers assume no liability for misuse of these tools. Always obtain proper authorization before testing any security tools.
