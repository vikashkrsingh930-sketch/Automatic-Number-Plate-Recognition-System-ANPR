# 🚗 Automatic Number Plate Recognition (ANPR) System

## 📌 Overview

This project is a **real-time Automatic Number Plate Recognition (ANPR) system** built using modern computer vision and deep learning techniques.
It detects vehicle number plates from images, videos, or live camera feeds and extracts the plate text with high accuracy.

---

## 🚀 Features

* 🔍 Real-time number plate detection
* 🎯 High accuracy OCR using Transformer-based model
* 🇮🇳 Indian number plate validation using regex
* 🎥 Multi-input support (Webcam, Image, Video)
* 📊 Excel logging of detected plates
* 📸 Automatic saving of cropped plate images
* 🔁 Multi-frame validation for better accuracy
* 🧠 Smart OCR correction (O ↔ 0, I ↔ 1)

---

## 🧠 Technologies Used

### Programming Language

* Python

### AI / ML Models

* YOLOv8 → Number plate detection
* TrOCR → Text recognition

### Libraries

* OpenCV → Image & video processing
* Ultralytics → YOLOv8 implementation
* Transformers → TrOCR model
* Pillow → Image handling
* OpenPyXL → Excel file operations
* Regex (re) → Plate validation

---

## ⚙️ System Workflow

Input → Detection → Cropping → Preprocessing → OCR → Validation → Storage

1. Input (Webcam / Image / Video)
2. Detect number plate using YOLOv8
3. Crop plate region
4. Preprocess image for clarity
5. Extract text using TrOCR
6. Validate using Indian plate regex
7. Save results to Excel + image folder

---

## 🇮🇳 Indian Number Plate Format

The system validates plates using:

```
[A-Z]{2}[0-9]{2}[A-Z]{1,2}[0-9]{4}
```

Example:

```
OD02AB1234
WB12CD5678
```

---

## 📂 Project Structure

```
ANPR-System/
│
├── anpr.py                # Main ANPR system
├── dashboard.py          # (Optional) Dashboard UI
├── plates.xlsx           # Output log file
├── plates_images/        # Saved plate images
├── model/                # YOLO trained model (best.pt)
├── README.md             # Project documentation
```

---

## ▶️ How to Run

### 1. Install Dependencies

```
pip install ultralytics opencv-python transformers pillow openpyxl streamlit
```

### 2. Run ANPR System

```
python anpr.py
```

### 3. (Optional) Run Dashboard

```
streamlit run dashboard.py
```

---

## 📊 Output

### Excel File (`plates.xlsx`)

* Plate Number
* Date
* Time
* Image Path

### Image Folder

* Cropped number plate images

---

## ⚠️ Limitations

* Performance may reduce in low-light conditions
* OCR accuracy affected by motion blur or extreme angles
* Requires good training dataset for best results

---

## 🚀 Future Improvements

* Vehicle tracking (DeepSORT)
* Real-time dashboard with live feed
* Database integration (MySQL/MongoDB)
* Blacklist alert system 🚨
* Cloud deployment

---

## 🎯 Applications

* Traffic monitoring systems
* Toll booth automation
* Parking management
* Law enforcement
* Smart city solutions
