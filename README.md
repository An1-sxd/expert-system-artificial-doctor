# 🩺 ArtDoc AI - Medical Expert System

ArtDoc AI is a modern, interactive medical expert system designed to assist in diagnostic reasoning. It utilizes a knowledge-based engine to perform **Forward Chaining** for diagnosis and **Backward Chaining** for hypothesis verification.

<p align="center">
  <a href="./output/Artificial Doctor.zip">
    <img src="https://img.shields.io/badge/⬇️_Download_for_Windows-7C3AED?style=for-the-badge&labelColor=2563EB&color=7C3AED" />
  </a>
</p>

## ✨ Features

- **Symptom Analysis**: Select multiple symptoms to receive a potential diagnosis.
- **Diagnostic Trace**: View the logic and rules fired during the reasoning process.
- **Verification Mode**: Test specific hypotheses (diseases) against provided symptoms.
- **Treatment Advice**: Get immediate precautions and recommendations for identified conditions.
- **Modern UI**: A sleek, responsive interface built with PyWebView and HTML/CSS.

## 🚀 Getting Started

### Prerequisites

The application requires Python and the `pywebview` library.

**Note on Python Versions:**
- **Recommended**: Python **3.13.x** (3.13.7 confirmed working).
- Due to dependencies on `pythonnet` for the Windows WebView2 interface, some Python environments may encounter initialization errors. If you see a `RuntimeError: Failed to initialize Python.Runtime.dll`, ensure you are using a standard Python 3.13 installation.

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/an1-sxd/expert-system-artificial-doctor.git
   cd expert-system-artificial-doctor
   ```

2. Install dependencies:
   ```bash
   pip install pywebview
   ```

### Running the App

Execute the main script:
```bash
python app_webview.py
```

## 🧠 System Logic

### Forward Chaining (Diagnosis)
The system starts with a set of symptoms (facts) and applies rules from the `knowledge_base.csv` to derive new facts (conclusions) until no more rules can be fired.

### Backward Chaining (Verification)
The system starts with a target disease (goal) and works backward to see if the known symptoms support the conditions required to reach that goal.

## 📂 Project Structure

- `app_webview.py`: The entry point and GUI wrapper.
- `engine.py`: The core Expert System engine logic.
- `datasets/`: Contains the `knowledge_base.csv` and other data files.
- `web/`: Contains the frontend assets (HTML, CSS, JS).

## ⚠️ Disclaimer
This system is for **educational and demonstration purposes only**. It is not a substitute for professional medical advice, diagnosis, or treatment. Always seek the advice of a physician or other qualified health provider with any questions you may have regarding a medical condition.
