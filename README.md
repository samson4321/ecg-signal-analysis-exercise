# ECG Signal Analysis Before and After Exercise

## Overview
This project presents a Python-based biomedical signal processing analysis of electrocardiogram (ECG) recordings acquired at rest and immediately after aerobic exercise. The work was conducted as part of my MSc training in Biomedical Engineering to strengthen practical understanding of ECG preprocessing, feature extraction, and physiological interpretation.

The analysis follows a complete ECG processing pipeline, including data cleaning, filtering, R-peak detection, heart rate (HR) calculation, and heart rate variability (HRV) assessment (SDNN), with a comparison between resting and post-exercise conditions.

---

## Aim
To study short-term cardiovascular responses to aerobic exercise by comparing ECG-derived parameters recorded at rest and immediately after a 20-minute jogging session.

---

## Objectives
- Acquire 60-second ECG recordings at rest and post-exercise  
- Preprocess ECG signals using band-pass and notch filtering  
- Detect R-peaks and extract RR intervals  
- Compute heart rate and short-term HRV (SDNN)  
- Compare ECG features between resting and post-exercise conditions  

---

## Data Description
- **Sampling frequency:** 1000 Hz  
- **Recording duration:** 60 seconds per condition  
- **Electrode configuration:** Three-electrode limb setup (Lead I equivalent)  
- **Data format:** TXT files  

### ECG Files
- `01_ECG_1min_1kHz-Rest.txt`
- `02_ECG_1min_1kHz-Stress.txt`

---

## Signal Processing Pipeline
1. **Data Import & Cleaning**
   - Conversion of European decimal format (comma to dot)
   - Import into NumPy arrays for processing

2. **Filtering**
   - Band-pass filter (0.5–40 Hz) to remove baseline drift and high-frequency noise  
   - 50 Hz notch filter to suppress power-line interference  
   - Zero-phase filtering to preserve ECG waveform morphology  

3. **Feature Extraction**
   - R-peak detection using a QRS enhancement approach  
   - RR interval computation  
   - Heart rate calculation:
     ```
     HR = 60 / RR (seconds)
     ```
   - Heart rate variability assessment using SDNN  

4. **Visualization**
   - Raw vs filtered ECG signals  
   - R-peak detection overlays  
   - Visualization of RR intervals and ECG morphology  

---

## Results Summary
- Increased heart rate after exercise  
- Shortened RR intervals post-exercise  
- Reduced SDNN, indicating decreased short-term HRV  
- Observed trends are consistent with expected physiological responses to acute aerobic exercise  

---

## Limitations
- Single-subject analysis (n = 1)  
- Short recording duration  
- Results are descriptive and not intended for population-level inference  

---

## Technologies Used
- Python  
- NumPy  
- SciPy  
- Pandas  
- Matplotlib  

---

## Learning Outcomes
- Practical implementation of ECG preprocessing and filtering techniques  
- Hands-on experience with R-peak detection and HR/HRV analysis  
- Improved understanding of physiological signal interpretation in response to exercise  
