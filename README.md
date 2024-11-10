
# E-KYC-using-OCR Project

Welcome to the **E-KYC** project! This application leverages state-of-the-art techniques in **Computer Vision**, **Natural Language Processing (NLP)**, **Convolutional Neural Networks (CNNs)**, and **Long Short-Term Memory (LSTM)** networks to automate the **Know Your Customer (KYC)** process.

## Overview

The E-KYC web application allows users to upload their **Aadhar** or **PAN card** along with a **photograph**. The app processes the ID card to extract face data and verifies it against the uploaded photograph for authentication.

## Features

- **Face Verification**:  
   The application extracts and matches the face from the uploaded ID card using **Haarcascade**. If the verification is successful, further operations proceed. If unsuccessful, an error is triggered.
  
  **Face Verification Demo**:  
   *I uploaded my friend's Aadhar card and my photo for testing. Face verification failed, and the code didn't continue as expected.*

- **Optical Character Recognition (OCR)**:  
   Upon successful face verification, the app uses **EasyOCR** to extract text from the ID card based on a pre-configured threshold.

- **Database Interaction**:  
   The app checks for any existing records in the database before inserting new data. If the user is already registered, no new entry is made, and existing data is returned.

- **Face Embeddings**:  
   The app utilizes **FaceNet** (via **DeepFace**) to extract face embeddings, which are then stored in the database.

## Full Workflow

- **Face Verification Failure**:  
   When I uploaded my Aadhar card and my friend's photo, face verification failed, and the subsequent operations didn’t execute.
   
- **Face Verification Success**:  
   When I uploaded my own photo, the face verification passed. The data was then inserted into the database. I later re-uploaded my photo to check for duplicacy, and the system successfully identified that my data already existed in the database.

## Technologies Used

- **Computer Vision**: Face detection and verification
- **Natural Language Processing (NLP)**: Text extraction from images
- **Convolutional Neural Networks (CNNs)**: For image processing
- **Long Short-Term Memory (LSTMs)**: For handling sequential data
- **EasyOCR**: For text extraction (OCR)
- **DeepFace**: For generating face embeddings
- **Haarcascade**: For detecting faces in images

## Upcoming Improvements

- **Live Face Detection**:  
   The application will eventually support live face detection using the device’s camera, eliminating the need for users to upload a photo.

- **Data Privacy**:  
   In future versions, sensitive data (e.g., original IDs) will be **hashed** before being stored in the database to enhance privacy and security. *[COMPLETED]*

## Prerequisites

Before you start, ensure that you have the following installed:

- **Python 12.0** or above
- **MySQL Server**

## Setup Instructions

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/Kishan101101/E-KYC-using-OCR.git
