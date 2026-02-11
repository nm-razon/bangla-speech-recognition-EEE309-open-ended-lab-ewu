# Bangla Speech Recognition – DSP Lab Project (EEE309)

## 📖 Introduction
This repository contains the implementation of a simple **Bangla Speech Recognition System** developed as part of the **EEE309 Digital Signal Processing Lab (Summer 2025)** at East West University.  

The system is designed to distinguish between two Bangla words:  
- **Shotto (True)**  
- **Mittha (False)**  

We used the **cross-correlation technique** for signal comparison, focusing on simplicity and efficiency for small-scale recognition tasks.

---

## 🎙️ Dataset
- **Total Files:** 260 audio samples (`.mp3`)  
- **Sampling Rate:** 4800 Hz  
- **Training Data:**  
  - 130 samples of *Shotto (True)*  
  - 130 samples of *Mittha (False)*  
- **Test Data:** Separate files used for evaluation and classification.  

---

## ⚙️ Methodology
1. **Preprocessing**  
   - Audio normalization to standardize amplitude.  
   - Conversion to mono if stereo recordings are present.  

2. **Signal Processing**  
   - Cross-correlation between test signals and training templates.  
   - Correlation peaks used to measure similarity.  

3. **Classification Logic**  
   - If correlation with *True* set > correlation with *False* set (and above threshold 0.5) → Classified as **True**.  
   - Otherwise → Classified as **False**.  

---

## 📊 Results
- **Accuracy:** 72.22% (8 out of 11 test samples correctly classified).  
- **Runtime:** ~5 minutes for all
