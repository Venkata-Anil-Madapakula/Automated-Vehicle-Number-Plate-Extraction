# 🚘 Automated Vehicle Number Plate Extraction

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)  
[![Flask](https://img.shields.io/badge/Flask-Web%20Framework-green.svg)](https://flask.palletsprojects.com/)  
[![License](https://img.shields.io/badge/License-MIT-brightgreen.svg)](LICENSE)

---

# 📖 Table of Contents

1. 📌 [Project Overview](#-project-overview)
2. ✨ [Features](#-features)
3. ⚙️ [Installation](#️-installation)
4. 📊 [Dataset](#-dataset)
5. 🛠️ [Project Workflow](#-project-workflow)
6. 📈 [Model Training and Evaluation](#-model-training-and-evaluation)
7. 🚀 [Deployment](#-deployment)
8. 📌 [Results and Insights](#-results-and-insights)
9. 🧠 [Future Enhancements](#-future-enhancements)
10. 👥 [Contributors](#-contributors)

---

## 📌 Project Overview

With the rise of vehicle-related crimes and the need for efficient surveillance, automated number plate detection has become increasingly important. This project leverages deep learning and OCR technologies to detect and extract vehicle license plates from real-time camera feeds and uploaded images. It is particularly useful in areas such as traffic enforcement, automated tolling, and parking systems.

The system aims to deliver accurate and real-time number plate extraction using state-of-the-art object detection (YOLOv8) and text recognition (Tesseract OCR). 🔍🚘🔠

---

- 📂 **GitHub Repository**: [Project Repository](https://github.com/your-username/number-plate-extraction)
- 🌐 **Live Demo**: [Streamlit App](https://your-streamlit-app-link)

---

## ✨ Features

- 🚗 Vehicle number plate detection using YOLOv8
- 🔤 Text recognition with Tesseract OCR
- ⌛ Real-time webcam processing
- 📤 Upload image support
- ✅ Validation of Indian plate format
- 🗃️ Plate data storage in CSV
- 🌐 Simple Flask web interface

---

## ⚙️ Installation

### Prerequisites

- Python 3.8+
- Tesseract OCR installed  
  [Tesseract Installation Guide](https://github.com/tesseract-ocr/tesseract)

### Steps

```bash
git clone https://github.com/yourusername/vehicle-number-plate-extraction.git
cd vehicle-number-plate-extraction
pip install -r requirements.txt
```

### Tesseract Path

Set the correct Tesseract path in `app.py`:

```python
pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'
```

---

## 📊 Dataset

- **Input Data**: Real-world images and live webcam streams
- **Annotations**: Bounding boxes for number plates
- **Storage Format**: CSV logs of detected plates with timestamps
- **Sample Output Fields**: `Plate Number`, `Date`, `Time`

---

## 🛠️ Project Workflow

### 🔹 1. Data Acquisition & Preprocessing
- 📸 Collected input from image uploads and live webcam streams via Flask.
- 🖼️ Converted images to grayscale, cropped number plate regions, and applied noise reduction.

### 🔹 2. Detection & OCR
- 🧠 Detected license plates using a fine-tuned YOLOv8 model.
- 🔤 Extracted alphanumeric text from plate regions using Tesseract OCR.
- 🧪 Filtered results to match Indian license plate formats.

### 🔹 3. Validation, Output & Storage
- ✅ Validated plate numbers and rejected noisy outputs.
- 💾 Saved results and logged plate data with timestamps in CSV format.
- 🌐 Displayed outputs to the user via the web interface.


---

## 📈 Model Training and Evaluation

### 🔹Model Details

- YOLOv8 pre-trained model used for object detection
- Fine-tuned on vehicle plate datasets
- Tesseract used for OCR post-detection

### 🔹Evaluation Metrics

| Metric                  | Value     |
|-------------------------|-----------|
| Detection Accuracy      | > 90%     |
| OCR Accuracy            | ~85%      |
| Frame Processing Speed  | ~30 ms    |
| Valid Plate Match Rate  | High      |

---

## 🚀 Deployment

### Local Server

```bash
python app.py
```

### Usage

- Navigate to `http://localhost:5000`
- Use **Upload** or **Real-time** menu options

---

## 📌 Results and Insights

- ✅ Accurate detection in varying lighting conditions
- ❌ Slight OCR drop in motion blur scenarios
- 📊 CSV-based data logging effective for analysis
- ⚡ Real-time processing enables use in surveillance

---

## 🧠 Future Enhancements

- 🧬 CRNN/Transformer-based OCR for complex fonts
- 🌙 Low-light performance improvement
- ☁️ Cloud deployment options
- 🔐 Add user authentication and DB integration

---

## 👥 Contributors

👨‍💻 **Venkata Anil Madapakula**  
---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
