# 🎯 Live Face Recognition System

A real-time Face Recognition system built using **Python**, **OpenCV**,
and the **face_recognition** library.\
The system detects and recognizes faces from a live webcam feed using
pre-stored images.

------------------------------------------------------------------------

## 📌 Features

-   ✅ Real-time face detection using webcam\
-   ✅ Face recognition using pre-trained encodings\
-   ✅ Multiple persons support\
-   ✅ Automatic name labeling\
-   ✅ Unknown face detection\
-   ✅ Simple folder-based dataset structure

------------------------------------------------------------------------

## 🛠️ Technologies Used

-   Python 3.x\
-   OpenCV\
-   face_recognition\
-   dlib\
-   NumPy

------------------------------------------------------------------------

## 📂 Project Structure

    Face-Recognition/
    │
    ├── dataset/
    │   ├── Person1/
    │   │   ├── img1.jpg
    │   │   ├── img2.jpg
    │   │
    │   ├── Person2/
    │       ├── img1.jpg
    │
    ├── face_recognition_script.py
    └── README.md

------------------------------------------------------------------------

## 📁 Dataset Setup

1.  Create a main folder (e.g., `dataset`)
2.  Inside it, create subfolders for each person.
3.  Name each folder with the person's name.
4.  Add multiple images of that person inside their respective folder.

Example:

    dataset/
        Milan/
            img1.jpg
            img2.jpg
        Rahul/
            img1.jpg

⚠️ Make sure images clearly show the person's face.

------------------------------------------------------------------------

## ⚙️ Installation

### 1️⃣ Clone the repository

``` bash
git clone https://github.com/yourusername/Face-Recognition.git
cd Face-Recognition
```

### 2️⃣ Install dependencies

``` bash
pip install opencv-python
pip install face-recognition
pip install numpy
```

If you face issues installing `face_recognition`, install `dlib` first:

``` bash
pip install dlib
```

------------------------------------------------------------------------

## 🔧 Configuration

In the script, replace this line:

``` python
DATA_DIR = r"Replace with the folder path in which your other folder of images are present"
```

With:

``` python
DATA_DIR = r"dataset"
```

Or provide the full path:

``` python
DATA_DIR = r"C:\Users\YourName\Face-Recognition\dataset"
```

------------------------------------------------------------------------

## ▶️ How to Run

``` bash
python face_recognition_script.py
```

-   Webcam will open.
-   Recognized faces will show **green box** with name.
-   Unknown faces will show **red box**.
-   Press **Q** to exit.

------------------------------------------------------------------------

## 🧠 How It Works

1.  Loads all images from dataset folders.
2.  Converts images into face encodings.
3.  Captures live webcam feed.
4.  Detects faces in each frame.
5.  Compares live face encoding with stored encodings.
6.  Displays matched name if found.

------------------------------------------------------------------------

## 📌 Parameters

You can adjust recognition sensitivity:

``` python
matches = face_recognition.compare_faces(known_encodings, face_encoding, tolerance=0.5)
```

-   Lower tolerance → More strict matching\
-   Higher tolerance → More flexible matching

Recommended range: `0.4 – 0.6`

------------------------------------------------------------------------

## 🚀 Future Improvements

-   Add GUI interface\
-   Add face registration feature\
-   Save attendance automatically\
-   Add database integration\
-   Deploy using Flask or FastAPI\
-   Improve performance with threading

------------------------------------------------------------------------

## ⚠️ Requirements

-   Webcam
-   Good lighting conditions
-   Clear face images

------------------------------------------------------------------------

## 📄 License

This project is open-source and free to use for educational purposes.

------------------------------------------------------------------------

## 👨‍💻 Author

**Milan Saini**
