# 🚧 AI-Based Road Damage Detection System

An intelligent web-based system that detects road surface defects such as cracks and potholes using a deep learning model (YOLO) and displays results with GPS location on a dashboard.

---

## 📌 Overview

Manual road inspection is time-consuming and inefficient. This project provides an automated solution using computer vision and geolocation to identify road damage in real time.

The system captures images from a camera or upload, processes them using an AI model, and returns annotated images with detected defects.

---

## 🎯 Features

* 📷 Live camera detection
* 🖼️ Image upload detection
* 🎥 Video frame detection (optional)
* 🧠 AI-based road damage detection (YOLO)
* 📍 GPS location tagging
* 🖼️ Annotated image with bounding boxes
* 🌐 Web dashboard interface
* ⚡ Real-time API communication

---

## 🏗️ System Architecture

```
Frontend (React Dashboard)
        ↓
Send Image + GPS
        ↓
Backend API (Flask - Colab)
        ↓
YOLO Model Detection
        ↓
Draw Bounding Boxes (OpenCV)
        ↓
Upload Image (Supabase)
        ↓
Return Image URL + Data
        ↓
Display on Dashboard
```

---

## 🧰 Tech Stack

### Frontend

* React (TypeScript)
* Canvas API
* Geolocation API

### Backend

* Python (Flask)
* OpenCV
* Ultralytics YOLOv8
* Google Colab
* ngrok

### Storage

* Supabase Storage (for annotated images)

---

## 📡 API Endpoint

### `POST /predict`

#### Request

```json
{
  "image": "base64_image",
  "latitude": 16.71,
  "longitude": 81.09
}
```

#### Response

```json
{
  "detections": [
    {
      "label": "Crack",
      "confidence": 0.92,
      "x": 100,
      "y": 120,
      "w": 80,
      "h": 60
    }
  ],
  "image_url": "https://your-storage-url/image.jpg",
  "latitude": 16.71,
  "longitude": 81.09
}
```

---

## 🚀 How It Works

1. User captures or uploads an image
2. GPS location is fetched from browser
3. Image + location sent to backend API
4. YOLO model detects road damage
5. Bounding boxes are drawn on image
6. Image is uploaded to storage
7. Dashboard displays annotated image

---

## ⚙️ Setup Instructions

### 🔹 Backend (Colab)

1. Install dependencies:

```bash
pip install ultralytics flask flask-cors opencv-python pyngrok
```

2. Run Flask server with ngrok
3. Copy the generated public URL

---

### 🔹 Frontend

1. Clone repository:

```bash
git clone https://github.com/your-username/your-repo.git
```

2. Install dependencies:

```bash
npm install
```

3. Run app:

```bash
npm run dev
```

4. Set API endpoint (ngrok URL)

---

## 📸 Output

* Annotated image with bounding boxes
* Detection labels and confidence
* GPS location of detected damage

---

## 🧠 Model Details

* Model: YOLOv8 (custom trained)
* Dataset: Road Damage Dataset (RDD)
* Capable of detecting:

  * Cracks
  * Potholes
  * Surface defects

---

## 📈 Advantages

* Automated road inspection
* Fast and efficient detection
* Low-cost solution
* Scalable system
* Useful for smart cities

---

## ⚠️ Limitations

* Depends on lighting conditions
* Requires internet connection
* Model accuracy depends on training data

---

## 🔮 Future Improvements

* 🗺️ Map integration for visualization
* 📊 Detection analytics dashboard
* 📱 Mobile application
* 🔔 Automated alert system
* 📦 Offline model deployment

---

## 👨‍💻 Contributors

* Your Name
* Team Members (if any)

---

## 📜 License

This project is for educational and research purposes.

---

## ⭐ Acknowledgements

* Ultralytics YOLO
* OpenCV
* Supabase
* Google Colab

---

## 💡 Inspiration

Smart city infrastructure monitoring and AI-based automation systems.
