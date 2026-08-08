# Deepfake-Video-Detection
AI-based deepfake detection system using ResNeXt and LSTM models to identify manipulated videos and improve the reliability and authenticity of digital media.
# DeepFake Detection Using ResNeXt and LSTM

## 📌 Project Overview

Deepfake technology uses artificial intelligence and deep learning to create highly realistic manipulated videos. As these techniques continue to evolve, distinguishing authentic videos from manipulated content has become increasingly challenging.

This project presents a deep learning-based **DeepFake Detection System** that combines **ResNeXt CNN** and **LSTM** networks to identify manipulated videos. ResNeXt is used to extract spatial features from video frames, while LSTM processes the sequence of extracted features to capture temporal patterns.

The trained model is integrated into a web application using **Flask** for the backend and **ReactJS** for the frontend. Users can upload a video and receive a **REAL/FAKE prediction along with a confidence score**.

---

## 🎯 Objectives

* Detect manipulated and deepfake videos using deep learning.
* Extract spatial features from video frames using ResNeXt.
* Analyze temporal relationships between consecutive video frames using LSTM.
* Provide a simple web interface for video uploads.
* Display the predicted result and confidence score.
* Integrate deep learning inference with a Flask backend and ReactJS frontend.

---

## 🔍 Problem Statement

The rapid development of deepfake generation techniques has made manipulated videos increasingly difficult to identify through conventional visual inspection.

Traditional detection techniques may struggle with sophisticated manipulations and can also require complex infrastructure. Therefore, this project aims to provide an accessible deepfake detection system that combines spatial and temporal deep learning techniques with a lightweight web-based interface.

---

## 🧠 Proposed Approach

The system uses a **ResNeXt + LSTM** architecture.

### ResNeXt

ResNeXt is used as the CNN-based feature extractor. It processes individual video frames and extracts meaningful spatial and visual features.

### LSTM

The extracted features from multiple frames are provided as a sequence to the LSTM network. LSTM helps capture temporal relationships and patterns that occur across frames.

### Classification

The combined spatial and temporal information is used to classify the input video as:

* **REAL**
* **FAKE**

The application also provides a confidence score associated with the prediction.

---

🔄 System Workflow
             ┌─────────────────────┐
             │        User         │
             └──────────┬──────────┘
                        │
                        ▼
             ┌─────────────────────┐
             │   ReactJS Frontend  │
             │    Video Upload     │
             └──────────┬──────────┘
                        │
                        ▼
             ┌─────────────────────┐
             │   Flask Backend     │
             │     server.py       │
             └──────────┬──────────┘
                        │
                        ▼
             ┌─────────────────────┐
             │  Video Processing   │
             │  & Frame Extraction │
             └──────────┬──────────┘
                        │
                        ▼
             ┌─────────────────────┐
             │    ResNeXt CNN      │
             │ Spatial Features    │
             └──────────┬──────────┘
                        │
                        ▼
             ┌─────────────────────┐
             │        LSTM         │
             │ Temporal Features   │
             └──────────┬──────────┘
                        │
                        ▼
             ┌─────────────────────┐
             │    Prediction       │
             │   REAL / FAKE       │
             │ + Confidence Score  │
             └──────────┬──────────┘
                        │
                        ▼
             ┌─────────────────────┐
             │   ReactJS Frontend  │
             │   Display Result    │
             └─────────────────────┘
---

## ✨ Key Features

* Deepfake video detection using deep learning.
* ResNeXt-based spatial feature extraction.
* LSTM-based temporal sequence analysis.
* Video upload through a web interface.
* REAL/FAKE classification.
* Confidence score for predictions.
* Flask backend for model inference.
* ReactJS frontend for user interaction.
* Local deployment support.

---

## 🛠️ Technologies Used

### Programming Language

* Python
* JavaScript

### Machine Learning / Deep Learning

* TensorFlow
* ResNeXt
* LSTM

### Computer Vision

* OpenCV
* NumPy

### Backend

* Flask

### Frontend

* ReactJS

### Development Environment

* Python Virtual Environment (`venv`)

---

## 💻 Hardware Requirements

The following configuration is recommended for model training:

| Component        | Requirement                                        |
| ---------------- | -------------------------------------------------- |
| Processor        | 64-bit, Python-compatible processor                |
| RAM              | 16 GB or higher recommended                        |
| GPU              | NVIDIA RTX 2060 or higher recommended for training |
| Storage          | At least 50 GB free SSD space                      |
| Operating System | Windows/Linux/macOS                                |

> GPU requirements mainly apply to model training. Requirements for running the trained model may be lower depending on the implementation.


# 🚀 How to Run the Project

## Prerequisites

Make sure the following are installed on your system:

* Python
* Node.js and npm
* Git
* A modern web browser

If a preconfigured `venv` folder is included with the project, the existing virtual environment can be activated directly.

---

## 1. Open the Project Folder

Locate the downloaded or cloned project folder.

For example:
C:\Users\YourName\DeepFake-Detection


Open the folder in **File Explorer**.

---

## 2. Open Command Prompt

Click the address bar at the top of the project folder.

Type:
cmd

and press **Enter**.

Command Prompt will open directly inside the project directory.

---

## 3. Activate the Virtual Environment

Run:
.\venv\Scripts\activate

After successful activation, `(venv)` should appear at the beginning of the command prompt.

Example:
(venv) C:\Users\YourName\DeepFake-Detection>


If `(venv)` appears, the virtual environment is active.


## 4. Navigate to the Application Directory

Run:
cd DeepFake_Detection


The command prompt should now point to the application directory.

Example:
(venv) C:\Users\YourName\DeepFake-Detection\DeepFake_Detection>


---

## 5. Start the Flask Server

Run:
python server.py

Wait for the Flask server and model components to finish loading.

Once the server starts successfully, a local URL should be displayed in the terminal.

For example:
http://127.0.0.1:3000/

---

## 6. Open the Application

You can **Ctrl + Click** the URL displayed in the Command Prompt.

Alternatively, copy the URL and open it in a browser.

You can also try:
http://localhost:3000/

## 7. Use the Application

After the application opens:

1. Select or upload a video.
2. Wait while the video is processed.
3. The system extracts relevant video frames.
4. ResNeXt extracts spatial features.
5. LSTM analyzes the temporal sequence.
6. The model generates a prediction.
7. The result is displayed as **REAL** or **FAKE** with a confidence score.

> **Important:** Keep the Command Prompt window open while using the application. Closing the terminal will stop the Flask server.

---

# 📊 Model Pipeline

The model follows the pipeline below:

```text
Input Video
     ↓
Frame Extraction
     ↓
ResNeXt CNN
     ↓
Spatial Feature Extraction
     ↓
Feature Sequence
     ↓
LSTM
     ↓
Temporal Feature Analysis
     ↓
Classification
     ↓
REAL / FAKE
     ↓
Confidence Score
```

---

# 📈 Results

The application provides a classification result for the uploaded video along with a confidence score.

| Metric    | Score |
| --------- | ----: |
| Accuracy  |   98% |


---

# 👨‍💻 My Contributions

This project is based on an existing open-source implementation and has been modified and extended for the requirements of this project.

My contributions include:

* Modified the existing project implementation.
* Worked with the ResNeXt + LSTM deep learning pipeline.
* Integrated the detection model with a Flask backend.
* Connected the backend with the ReactJS frontend.
* Worked on the video upload and prediction workflow.
* Improved the usability and presentation of prediction results.
* Structured the project for local web-based execution.

---

# 🔮 Future Scope

The project can be further improved in several areas:

* Improve model generalization across different types of deepfake videos.
* Support additional video formats and resolutions.
* Improve detection accuracy on unseen manipulation techniques.
* Optimize model inference speed.
* Explore newer deepfake detection architectures.
* Implement real-time deepfake detection.
* Improve robustness against newly emerging deepfake generation methods.
* Deploy the application to a cloud-based environment.
* Develop an API for integration with other applications.

---

# 📝 Conclusion

This project demonstrates the application of deep learning techniques for detecting manipulated videos by combining **ResNeXt CNN for spatial feature extraction** and **LSTM for temporal sequence analysis**.

The integration of the model with a **Flask backend and ReactJS frontend** provides a simple interface through which users can upload videos and obtain deepfake detection results.

The project provides practical experience in **deep learning, computer vision, video processing, model inference, backend development, and frontend integration**, while addressing the growing challenge of maintaining trust and authenticity in digital media.

---

# 🙏 Acknowledgement

This project is based on an existing open-source implementation by Dhruti Patel (2021)
The original implementation has been modified and extended for the requirements of this project.
