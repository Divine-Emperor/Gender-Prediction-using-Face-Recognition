<h1 align="center">🎭 Face Recognition & Gender Prediction Web App</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white" alt="Flask" />
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white" alt="OpenCV" />
  <img src="https://img.shields.io/badge/scikit_learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="Scikit-Learn" />
</p>

## 📌 Overview
This project is a **Flask-based web application** designed to perform real-time face detection and gender prediction. Users can seamlessly upload images through a clean UI, where the backend processes the image to isolate facial features and uses a trained Machine Learning model to classify the gender. 

## 🧠 The Machine Learning Pipeline
This application relies on a robust, classic Computer Vision pipeline:
1. **Face Detection:** Utilizes OpenCV's **Haar Cascade Classifier** to locate and extract faces from the uploaded image.
2. **Dimensionality Reduction:** Applies **Principal Component Analysis (PCA)** to extract the most critical features from the facial image, reducing computational load while maintaining accuracy.
3. **Classification:** Feeds the PCA-reduced features into a trained **Support Vector Machine (SVM)** to predict the gender.

## ✨ Features
* **📷 Image Uploads:** Simple and clean Flask web interface for uploading local images.
* **🔍 Face Isolation:** Automatically detects and crops faces from complex backgrounds.
* **🤖 Fast Prediction:** Near-instantaneous gender prediction using pre-trained `.pickle` models.
* **🧪 Test Ready:** Includes a `test_images/` directory with sample images to verify the model immediately.

## 🛠️ Technologies Used
* **Backend:** Python, Flask
* **Computer Vision:** OpenCV (`cv2`)
* **Machine Learning:** Scikit-Learn (SVM, PCA), NumPy
* **Frontend:** HTML/CSS (Jinja2 Templates)

## 🗂 Project Structure
```text
Face-recongination-main/
│
├── app/
│   ├── face_recognition.py   # Face detection & prediction ML logic
│   └── views.py              # Flask routes and views handling
│
├── model/
│   ├── haarcascade_frontalface_default.xml # OpenCV detection model
│   ├── model_svm.pickle                    # Trained SVM classifier
│   └── pca_dict.pickle                     # Trained PCA components
│
├── static/
│   └── upload/               # Temporary storage for uploaded images
│
├── templates/
│   ├── base.html             # Base layout
│   ├── index.html            # Landing page
│   ├── app.html              # App interface
│   └── gender.html           # Results page
│
├── test_images/              # Sample images for testing
├── main.py                   # Application entry point
└── README.md

---
```
## ▶️ How to Run
1. Install dependencies:
```bash
pip install flask opencv-python numpy scikit-learn
```

2. Run the application:
```bash
python main.py
```

3. Open your browser and visit:
```
http://127.0.0.1:5000/
```

---

## 📸 Usage
- Upload an image containing a face
- The app detects the face
- Gender prediction result is displayed on the UI

---

## 📌 Notes
- Models are pre-trained and stored in the `model/` directory
- Best results with clear, front-facing images

---

## 📄 License
This project is for educational purposes.
