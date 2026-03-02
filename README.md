# **Echo Trace: Multimodal Deepfake & Dub Detection**

**Echo Trace** ek AI‑powered **digital forensics** tool hai jo dubbed ya manipulated videos ko detect karta hai, audio‑visual sync, facial motion aur acoustic artifacts analyse karke.  
Yeh FOSS hackathons aur practical deepfake investigation ke liye design kiya gaya hai.

---

## **✨ Key Features**

- **Audio‑visual sync analysis** (lip‑sync, jaw movement, frame‑level timing)
- **Visual artifacts**: frame inconsistencies, frequency / compression anomalies
- **Physiological cues**: approximate rPPG / micro‑movement signals from faces
- **Audio forensics**: prosody, pauses, unnatural pacing patterns
- **Simple web UI (Streamlit)**: upload video → REAL/FAKE + probability
- **Modular Python codebase**: easily extendable with better models or features

---

## **📂 Project Structure**

```text
echo_trace_project/
  ├── echo_trace/
  │   ├── __init__.py
  │   ├── config.py            # paths and global settings
  │   ├── video_utils.py       # face detection, landmarks, frame sampling
  │   ├── audio_utils.py       # audio loading, MFCC/features
  │   ├── features.py          # combine audio + visual into feature vectors
  │   ├── classifier.py        # ML model (e.g., RandomForest)
  │   ├── pipeline.py          # end‑to‑end video → prediction pipeline
  ├── data/
  │   └── videos/              # sample real/fake videos (not included in repo)
  ├── models/
  │   └── rf_classifier.pkl    # trained model (optional, can be regenerated)
  ├── train_classifier.py      # script to train the classifier
  ├── app.py                   # Streamlit app for the UI
  └── README.md
Note: Kuch folders (jaise data/videos) empty reh sakte hain ya .gitignore me honge taaki repo halka rahe.


