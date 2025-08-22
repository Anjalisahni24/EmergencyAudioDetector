# Emergency Audio Detection (ML)

This repository contains the Machine Learning component of the **Emergency Audio Detection** project—an Android-based app that detects emergency audios using the mobile phone's microphone and sends alerts to a user's emergency contacts.

## Project Overview

The goal of the project is to assist users in emergency situations by automatically detecting emergency sounds (like sirens, alarms, or distress calls) and sending an alert to selected contacts. The Android app records audio, processes it, and utilizes this ML model to classify the audio as either "emergency" or "non-emergency." If an emergency is detected, the app sends an alert SMS with the user's location to the saved contacts.

## ML Approaches

This repository implements and compares two main approaches for audio classification:

- **Approach 1: ANN (Artificial Neural Network)**
  - Inputs 1D flattened feature vectors extracted from audio.
- **Approach 2: CNN (Convolutional Neural Network)**
  - Inputs 2D spectrogram-based representations derived from raw audio.

## Technologies Used

- Python
- Librosa
- Pandas
- Numpy
- TensorFlow
- Keras
- ANN, CNN architectures

## How It Works

1. The user starts recording audio via the mobile app.
2. Recorded audio is preprocessed and sent to the ML model.
3. The model predicts if the audio is an "emergency" or "non-emergency."
4. If an emergency is detected:
   - The user receives a confirmation prompt.
   - If the user confirms or does not respond within 10 seconds, an alert SMS with the user's location is sent to their emergency contacts.
   - If the user dismisses the alert, the app continues monitoring.

## Usage Example

> **Example Scenario:**  
> User A installs the app and sets up emergency contacts. While walking, A activates the recording feature. The app continuously processes recorded audio using the ML model. Upon detecting an emergency sound, the app prompts A for confirmation. If A confirms (or doesn't respond), an alert with the real-time location is automatically sent to the pre-listed emergency contacts.


## Contributors

- [Shagun Thakur](https://github.com/Shagun-Thakur)
- [Anjali Sahni](https://github.com/Anjalisahni24) 


---

**Note:** This repository covers only the ML part. For the full Android app, refer to the corresponding repository.
