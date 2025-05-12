
# 🎤 Emotion-Aware Speech Recognition Using Whisper and SVM

This project demonstrates an emotion-aware speech recognition pipeline that transcribes audio from video files and classifies the speaker's emotion based on audio features.

---

## 📌 Features

- Converts MP4 videos to WAV audio format.
- Transcribes speech using OpenAI's Whisper model.
- Extracts audio features (MFCC and Pitch) using `librosa`.
- Predicts emotion using a simulated SVM classifier.
- Outputs transcription, detected language, and speaker emotion.

---

## 🧠 Model Components

| Component              | Description                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| Whisper                | Used for transcribing speech and detecting language.                        |
| MFCC + Pitch Extraction| Extracts features from audio for emotion classification.                    |
| SVM Classifier         | Trained on simulated data to predict emotion from audio features.           |
| MoviePy                | Converts MP4 video to WAV format for audio processing.                      |

---

## 🛠️ Installation

Run the following command to install all required libraries:

```bash
pip install openai-whisper librosa scikit-learn moviepy
```

---

## 📁 File Structure

```
emotion_speech_recognition/
│
├── main.py                         # Contains the full Python script
├── angry_alex.wav                 # Output WAV audio (temporary file)
└── vedio.mp4                      # Input MP4 file with speech
```

---

## 🧪 How It Works

1. **Convert MP4 to WAV**  
   Converts the input MP4 file into a WAV format audio file for processing.

2. **Transcribe Audio**  
   Uses the Whisper model to transcribe the spoken content and detect the language.

3. **Extract Audio Features**  
   Calculates MFCC and pitch features from the audio signal using `librosa`.

4. **Emotion Classification**  
   A pre-trained (simulated in this demo) SVM model classifies the emotion based on extracted features.

---

## 🚀 Running the Program

In your script or notebook, simply call:

```python
audio_path = "/content/drive/MyDrive/vedio.mp4"
emotion_aware_speech_recognition(audio_path)
```

---

## ⚠️ Notes

- The current classifier uses **random simulated data** for training. For real-world accuracy, replace it with training on real emotion-labeled datasets like **RAVDESS**.
- Make sure your MP4 file contains a valid audio stream.
- `angry_alex.wav` is a temporary file; you can change the name or delete it after processing.

---

## 📚 Future Improvements

- Replace simulated data with actual audio emotion datasets.
- Use deep learning (e.g., CNNs or LSTMs) for emotion detection.
- Improve feature extraction (e.g., adding Chroma, Spectral Contrast).
- Extend to multi-language support or speaker identification.

---

## 🤝 Acknowledgements

- [OpenAI Whisper](https://github.com/openai/whisper)
- [Librosa](https://librosa.org/)
- [MoviePy](https://zulko.github.io/moviepy/)
- [RAVDESS Dataset](https://zenodo.org/record/1188976)
