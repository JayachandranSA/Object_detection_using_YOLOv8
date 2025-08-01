# 🚗 Object Detection on Vehicle Dashboard Camera Video using YOLOv8

## 🔍 Overview

This project uses the **YOLOv8** object detection model to identify and localize vehicles such as **cars, buses, trucks, and motorcycles** in a 30-second dashboard camera video. The solution performs **frame-by-frame inference** with bounding box annotations and class labels overlaid directly onto the video. The project is built to be **lightweight and optimized for Google Colab**, handling large video files (\~300MB) efficiently to avoid memory issues.

---

## ✨ Features

* Real-time object detection using **YOLOv8**.
* Supports **bounding box and label annotations** for detected objects.
* Processes videos in a memory-efficient streaming mode.
* Utilizes **Google Drive** for file storage and access in Colab.
* End-to-end script from loading video → detecting objects → saving annotated video.

---

## 🎯 Use Case

This system is designed for use in:

* Smart mobility & transportation surveillance.
* Driver assistance systems (ADAS).
* Automotive analytics & behavior monitoring.

---

## 🎥 Sample Input

A sample dashboard camera video with a variety of on-road vehicles and movement patterns is used as the input. The output video will display detection overlays for:

* 🚗 Cars
* 🚌 Buses
* 🚚 Trucks
* 🏍️ Motorcycles

---

## 📁 Folder Structure

```
├── video/                # Raw video files (input)
├── output/               # Annotated video (output)
├── yolo_inference.py     # Main script to run detection
├── requirements.txt      # Dependencies
├── README.md             # Project documentation
```

---

## ⚙️ Installation & Usage (in Google Colab)

### ✅ Step 1: Clone the Repository

```bash
git clone https://github.com/JayachandranSA/YOLOv8_Object_Detection.git
cd YOLOv8_Object_Detection
```

### ✅ Step 2: Install YOLOv8 and Required Libraries

```python
!pip install ultralytics
```

### ✅ Step 3: Mount Google Drive (if using Colab)

```python
from google.colab import drive
drive.mount('/content/drive')
```

### ✅ Step 4: Run Object Detection

```python
python yolo_inference.py
```

The `yolo_inference.py` script loads the model, processes the video frame-by-frame, performs detection, and saves an annotated video.

---

## 🧠 Model

* **Model Used**: YOLOv8n (Nano)
  *Pre-trained model from Ultralytics for lightweight inference.*
* **Framework**: [Ultralytics YOLOv8](https://docs.ultralytics.com)

---

## 🔋 Optimization for Large Video

* Inference is run using `stream=True` mode in YOLOv8 to process one frame at a time.
* This avoids loading the entire video into memory.
* Output video is written frame-by-frame to prevent RAM overflow in Colab.

---

## ✅ Future Improvements

* Add support for object tracking across frames.
* Visualize detection statistics (counts, types, timestamps).
* Deploy using Flask for live video stream detection.

---

## 🤝 Contributions

Feel free to fork the repo, raise issues, or submit pull requests to contribute!

---

## 📬 Contact

For any queries, reach out via GitHub or email:
📧 [jayachandran.sa@outlook.com](mailto:jayachandran.sa@outlook.com)

---

🚀 **Happy Coding!**

---
