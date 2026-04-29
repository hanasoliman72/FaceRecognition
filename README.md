# 🐱 Binky Face Recognition

> A desktop face recognition app for user registration and login, with attendance logging to Excel.

---

## 📖 Overview

**Binky** is a Python-based face recognition system with a GUI that lets users register their face and log in using it. Every successful login is automatically recorded in an Excel sheet with a timestamp — making it useful as a lightweight attendance or access-log tool.

---

## ✨ Features

- 📸 **Face Registration** — Captures and encodes a user's face via webcam and saves it locally
- 🔐 **Face Login** — Matches a live webcam feed against stored encodings to authenticate users
- 🚫 **Duplicate Detection** — Prevents registering the same face or name twice
- 📊 **Excel Logging** — Logs every successful login with name, timestamp, and team member status
- 🖥️ **Tkinter GUI** — Clean, centered desktop window for easy interaction

---

## 🗂️ Project Structure

```
binky-face-recognition/
├── main.py                  # Main application (GUI + logic)
├── requirements.txt         # Python dependencies
├── registered_faces.json    # Stored face encodings (auto-generated)
└── login_log.xlsx           # Login history (auto-generated)
```

---

## 🛠️ Tech Stack

| Library | Purpose |
|---|---|
| `face_recognition` | Face detection & encoding |
| `opencv-python` | Webcam access & video frames |
| `tkinter` | Desktop GUI |
| `openpyxl` | Excel login logging |
| `numpy` | Encoding distance calculations |

---

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- A working webcam
- `cmake` and `dlib` dependencies (required by `face_recognition`)

### Install Dependencies

```bash
pip install -r requirements.txt
```

> **Note:** Installing `face_recognition` may require `cmake` and `Visual Studio Build Tools` on Windows, or `build-essential` on Linux.

### Run the App

```bash
python main.py
```

---

## 🧭 How to Use

1. **Register** — Enter your name, click *Register*, and look at the camera. Press `s` to capture your face.
2. **Login** — Enter your name, click *Login*, and look at the camera. If your face matches, you're logged in.
3. **Log file** — Each successful login is saved to `login_log.xlsx` automatically.

---

## 📋 Login Log Format

| Name | Login Time | Team Member |
|---|---|---|
| Hana | 2025-04-29 10:23:45 | Yes |
| John | 2025-04-29 11:00:12 | No |

---

## ⚙️ Configuration

You can adjust the face matching sensitivity in `main.py`:

```python
# Lower = stricter matching, Higher = more lenient
if distance < 0.45:
```

---

## 📄 License

This project is for educational purposes.
