# Face Recognition & Gender Prediction Flask App

This project is a **Flask-based web application** that performs **face detection and gender prediction** using Machine Learning models.  
Users can upload images, and the application detects faces and predicts gender using a trained SVM model with PCA features.

---

## 🚀 Features
- Face detection using **Haar Cascade Classifier**
- Gender prediction using **SVM (Support Vector Machine)**
- Dimensionality reduction with **PCA**
- Simple and clean **Flask web interface**
- Supports image upload and testing with sample images

---

## 🗂 Project Structure
```
Face-recongination-main/
│
├── app/
│   ├── face_recognition.py   # Face detection & prediction logic
│   └── views.py              # Flask routes and views
│
├── model/
│   ├── haarcascade_frontalface_default.xml
│   ├── model_svm.pickle
│   └── pca_dict.pickle
│
├── static/
│   └── upload/               # Uploaded images
│
├── templates/
│   ├── base.html
│   ├── index.html
│   ├── app.html
│   └── gender.html
│
├── test_images/              # Sample images for testing
├── main.py                   # Application entry point
└── README.md
```

---

## 🛠 Technologies Used
- Python
- Flask
- OpenCV
- NumPy
- scikit-learn
- HTML/CSS (Jinja templates)

---

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
