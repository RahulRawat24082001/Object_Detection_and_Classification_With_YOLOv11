# 🔍 YOLO Image Search

A **computer vision–powered image search application** built using **YOLOv11m** for object detection & classification and **Streamlit** for an interactive web UI.

This project allows users to:

* Load a dataset directory
* Run object detection on images
* Search images based on detected objects
* View **bounding boxes**, **class names**, and **confidence scores**
* **Export detection results as JSON**
---

## 🚀 Features

* ⚡ YOLOv11m for fast & accurate object detection
* 🖼️ Image-level search based on detected classes
* 📦 COCO-format dataset support
* 📊 Confidence scores for each detection
* 🧾 Export results to JSON
* 🌐 Clean and simple Streamlit UI

---

## 🧠 Model & Tech Stack

* **Model:** YOLOv11m (Ultralytics)
* **Framework:** PyTorch
* **UI:** Streamlit
* **Computer Vision:** OpenCV
* **Dataset:** COCO-Val-2017-500

---

## 📁 Dataset Used

**COCO Validation 2017 (Subset – 500 images)**
Official documentation:

> [https://docs.ultralytics.com/datasets/detect/coco/#how-is-the-coco-dataset-structured-and-how-do-i-use-it](https://docs.ultralytics.com/datasets/detect/coco/#how-is-the-coco-dataset-structured-and-how-do-i-use-it)

### COCO Directory Structure (Expected)

```text
dataset/
├── images/
│   └── val2017/
├── labels/
│   └── val2017/
└── data.yaml
```

The dataset directory is **directly passed to the YOLO model**, which reads images and labels automatically using the `data.yaml` file.

---

## 📦 Prerequisites

Make sure you have the following installed:

* Python **3.9+**
* pip
* Virtual environment (recommended)
* GPU (optional but recommended for faster inference)

---

## 🧾 Requirements

Create a `requirements.txt` file with the following content:

```txt
ultralytics
streamlit
opencv-python
pyyaml
torch
torchvision
pillow
pandas
numpy
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## 🔧 Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/Yolo_Image_Search.git
cd Yolo_Image_Search
```

### 2️⃣ Create Virtual Environment (Recommended)

```bash
python -m venv venv
source venv/bin/activate   # Linux / Mac
venv\Scripts\activate      # Windows
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🧪 Using Ultralytics YOLO

Ultralytics makes YOLO extremely easy to use.

### 🔹 Install Ultralytics

```bash
pip install ultralytics
```

### 🔹 Load YOLOv11m Model (Internally Used)

```python
from ultralytics import YOLO
model = YOLO("yolo11m.pt")
```

### 🔹 Run Detection on Dataset

The model automatically reads the dataset when you pass the dataset directory:

```python
results = model("path/to/dataset")
```

Ultralytics handles:

* Image loading
* Label parsing
* Class mapping
* Bounding box scaling

---

## 🖥️ Running the Streamlit App

```bash
streamlit run app.py
```

---

## 📌 How the Project Works

1. User provides **dataset directory path**
2. YOLOv11m runs detection on images
3. Detected objects are stored with:

   * Bounding box coordinates
   * Class name
   * Confidence score
4. User searches images by **object name**
5. UI displays:

   * Image with bounding boxes
   * Class labels + scores
6. Results can be **exported as a JSON file**

---

## 📤 JSON Export Format (Example)

```json
{
  "image": "000000123.jpg",
  "detections": [
    {
      "class": "person",
      "confidence": 0.91,
      "bbox": [x1, y1, x2, y2]
    }
  ]
}
```

---

## 📊 Use Cases

* Dataset exploration
* Image-based object search
* CV demos & portfolios
* Annotation verification
* Learning YOLO & Streamlit

---

## 🤝 Contributing

Contributions are welcome!
Feel free to fork the repo and submit a pull request.

---

## ⭐ Acknowledgements

* **Ultralytics YOLO**
* **COCO Dataset**
* **Streamlit Community**

---

## 📜 License

This project is for **educational and experimental purposes**.

---

### 👨‍💻 Developed by Rahul Rawat

Certified & Working AI Developer 🚀


