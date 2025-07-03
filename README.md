# License Plate Recognition Web App

Built with:  
- **Frontend**: React + TypeScript  
- **Backend**: Flask + EasyOCR  
- **Computer Vision**: OpenCV  

---

## Overview

This application is designed to detect and recognize license plate numbers from vehicle images. By combining object detection and Optical Character Recognition (OCR), the app automates the identification of license plates, which can be used in various smart traffic or parking systems. It provides a clean interface for uploading images, processes them using a Flask backend, and highlights the recognized plate with bounding boxes and predicted text.

---

## Features

### > Upload Image & Detect Plate  
Users can upload an image of a vehicle directly through the interface. The app automatically locates the license plate using OpenCV and extracts the relevant region for OCR processing.  
**For testing**: Try uploading different vehicle images with clear license plates.

### > OCR with EasyOCR  
After detecting the plate, the app uses EasyOCR to extract alphanumeric characters. The recognized text is displayed alongside the image with confidence scores.  
**For testing**: Upload plates from different countries or in different fonts/sizes to evaluate OCR performance.

### > Image Preprocessing  
The backend applies grayscale conversion, edge detection, and contour analysis to accurately locate plates before passing them to OCR. This improves accuracy even in noisy or low-light images.

### > Simple UI with React  
The frontend is designed to be user-friendly and responsive. It provides a step-by-step flow from uploading an image to viewing the recognized plate text.

---

## Deployment

### Backend (Flask)  
1. Navigate to the backend directory:  
   `cd backend`  
2. Install dependencies:  
   `pip install -r requirements.txt`  
3. Start the Flask server:  
   `python app.py`

---

### Frontend (React)  
1. Navigate to the frontend directory:  
   `cd frontend`  
2. Install dependencies:  
   `npm install`  
3. Start the development server:  
   `npm start`

Visit **http://localhost:3000** to use the application.

---

## Future Improvements

- Support for real-time video feed detection  
- Integration with license plate databases for vehicle lookup  
- Multi-language OCR support  
- Enhanced image preprocessing with deep learning-based detectors
