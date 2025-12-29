# ECG Signal Analysis Before and After Exercise

## Overview
This project analyzes electrocardiogram (ECG) signals recorded at rest and immediately after aerobic exercise to study short-term cardiovascular responses. Python-based signal processing techniques are used to filter ECG signals, detect R-peaks, extract RR intervals, compute heart rate (HR), and evaluate heart rate variability (SDNN).

The project demonstrates a full ECG analysis pipeline, including data preprocessing, feature extraction, visualization, and comparison of resting versus post-exercise conditions.

---

## Aim
To investigate the effect of a 20-minute jogging exercise on ECG-derived parameters by comparing recordings acquired at rest and immediately after exercise.

---

## Objectives
- Record a 60-second resting ECG using a three-electrode limb configuration  
- Record a 60-second post-exercise ECG after 20 minutes of jogging  
- Preprocess ECG signals (data cleaning, band-pass filtering, notch filtering)  
- Detect R-peaks and compute RR intervals and heart rate  
- Compare resting and post-exercise ECG features using descriptive statistics  

---

## Data Description
- **Sampling frequency:** 1000 Hz  
- **Recording duration:** 60 seconds per condition  
- **Electrode configuration:** Right arm, left arm, left leg reference (Lead I equivalent)  
- **Data format:** TXT files  

### ECG Files
- `01_ECG_1min_1kHz-Rest.txt`
- `02_ECG_1min_1kHz-Stress.txt`

---

## Signal Processing Pipeline
1. **Data Import**
   - Conversion of European decimal format (comma to dot)
   - Import as NumPy arrays

2. **Filtering**
   - Band-pass filter (0.5–40 Hz) to remove baseline drift and high-frequency noise
   - 50 Hz notch filter to remove power-line interference
   - Zero-phase filtering to preserve waveform morphology

3. **Feature Extraction**
   - R-peak detection using a QRS enhancement approach
   - RR interval calculation
   - Heart rate calculation using:
     ```
     HR = 60 / RR (seconds)
     ```
   - Heart rate variability (SDNN)

4. **Visualization**
   - Raw vs filtered ECG signals
   - R-peak detection overlays
   - Annotated P-QRS-T components and RR intervals

---

## Results Summary
- Heart rate increased after exercise
- RR intervals shortened post-exercise
- SDNN decreased, indicating reduced short-term heart rate variability
- Results are consistent with normal physiological responses to acute aerobic exercise

---

## Limitations
- Single subject (n = 1)
- Short recording duration (60 seconds)
- Results are descriptive and not generalizable to a population

---

## Technologies Used
- Python
- NumPy
- SciPy
- Matplotlib
- Pandas

---


