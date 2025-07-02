# 💪 Smart Rehabilitation System

An AI-powered, secure, and mobile physiotherapy platform that delivers intelligent rehabilitation at home.

![Screenshot 2025-07-02 190328](https://github.com/user-attachments/assets/27ce2f6b-d818-4eb8-a6e7-a06eb6d77188)
---

## 🎯 Abstract

**Smart Rehabilitation System** is a remote physiotherapy platform combining **Artificial Intelligence**, **IoT**, and **secure cloud infrastructure** to:

- Monitor patient muscle activity (sEMG)
- Classify movement as **normal** or **abnormal**
- Guide personalized exercises with **real-time feedback**
- Ensure safety using **ECG heart monitoring**
- Provide **form correction** using **MediaPipe camera tracking**

---

## 🧠 Role of AI

AI is central to every decision in our system:

- 🤖 **ML Models** classify movements as normal or abnormal based on EMG features
- 📈 **LRCN (CNN + Bi-LSTM)** predicts knee joint angles for patients with abnormal movement
- 🎯 **Real-Time Feedback** is given to correct exercises (TKE, squats, sit-ups, bicep curls)
- 🧑‍⚕️ **Computer Vision** using MediaPipe tracks body movement for general fitness

---

## 🧪 Signal Processing Pipeline

We collected and processed **surface EMG** and **IMU** sensor data to analyze movement:

### 📌 EMG Signal Flow:
1. **Filtering**: Bandpass (20–450 Hz), Notch (50Hz)
2. **Denoising**: Discrete Wavelet Transform
3. **Segmentation**: Windowed EMG slices
4. **Normalization**
5. **Oversampling**: SMOTE, ADASYN
6. **Feature Extraction**:
   - MAV, RMS, ZC, SSC, WAMP, AAC, etc.

### 📌 Classification:
- Traditional ML: SVM, Random Forest, Gradient Boosting
- Deep Learning: CNN-LSTM (for abnormal users)

---

## 🧘‍♀️ Personalized Therapy Flow

### 🟠 Abnormal Users
- Tracked using **sEMG + IMU**
- Exercise: Terminal Knee Extension (TKE)
- Model: LRCN (Multi-task: angle regression + classification)
- Real-time corrective feedback

### 🟢 Normal Users
- Tracked using **MediaPipe (camera only)**
- Exercises: Squat, Sit-up, Arm Curl
- Real-time rep feedback using angles & rules

---

## 🔐 Security

- All sensor data is **AES-128 encrypted**
- Stored securely in **Firebase**
- Therapist identity is validated using **Blockchain + Digital Signature**
- MetaMask + Ethereum Sepolia for therapist verification

---

## 📱 Mobile App Features

- Firebase Authentication
- Live EMG Monitoring
- Real-time exercise classification
- Secure therapist-patient booking
- Personalized exercise feedback
- Therapist approval via blockchain

---

## 🖼️ Project Screenshots

> Add these screenshots in your repo inside a folder `images/` and link here:

| EMG Signal | LRCN Output | App Demo | Therapist Verification |
|------------|-------------|----------|-------------------------|
| ![EMG](images/emg_filtered.png) | ![LRCN](images/lrcn_output.png) | ![App](images/app_home.png) | ![Verify](images/therapist_verify.png) |

---

## 👩‍💻 Team

- **Habiba Osama**
- Asmaa Ahmed
- Farah Nasr
- Mariam Ahmed
- Marian Maher

Supervised by:  
Prof. Dr. Saad Darweesh, Dr. Sahar Ghanem, Eng. Esraa Hamshary

---

## 📄 References

> [📄 AI in Healthcare - MDPI](https://www.mdpi.com/2075-4426/13/6/951/pdf)  
> [📄 Human Knee sEMG Dataset](https://doi.org/10.1016/j.bspc.2022.103836)  
> [📄 LRCN Architecture Reference](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9550908/)

---




