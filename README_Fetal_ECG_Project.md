
# 🫀 Fetal ECG Extraction using MATLAB (DSP Project)

This project focuses on extracting the **fetal ECG (fECG)** signal from a mixed abdominal ECG using **advanced signal processing techniques in MATLAB**. The signal is often dominated by the maternal ECG (mECG) and noise, making separation a challenging task.

Our approach combines **wavelet transforms**, **adaptive filtering using RLS**, and **threshold-based denoising** to extract the fetal ECG signal from the maternal ECG. We also reverse the process to isolate the maternal ECG using the fetal ECG as a reference.


## 🎯 Objectives

- Extract a clean fetal ECG signal from a noisy abdominal signal
- Improve **Signal-to-Noise Ratio (SNR)** and minimize overlap with maternal signal
- Visualize and detect **QRS peaks**
- Extract maternal ECG back from fetal reference


## 🧰 Tools & Techniques Used

- MATLAB R2023
- Stationary Wavelet Transform (SWT) using **Daubechies (db4)**
- Recursive Least Squares (RLS) adaptive filter
- Hard Thresholding
- Signal reconstruction using Inverse SWT
- QRS Peak detection using `findpeaks()`
- Correlation analysis & SNR evaluation



## 🧠 Dataset Used

- `r01.edf` signal from **PhysioNet’s Abdominal and Direct Fetal ECG Database**
  - Signal Length: 1920 samples
  - Signals used:
    - Thoracic ECG (reference)
    - Abdominal ECG (mixed maternal + fetal)


### ✅ Extracted Signals:
- Clean fetal ECG with R and S peaks labeled
- Extracted maternal ECG from the same mixed signal

### 📊 Performance Metrics:
- **SNR (fetal ECG)** improved from **1.14 dB** → **1.63 dB**
- **SNR (maternal ECG)** improved from **1.32 dB** → **4.49 dB**
- **Correlation coefficient (fECG vs mECG)** ≈ **0.0058**
- **Correlation coefficient (mECG vs thoracic ECG)** ≈ **0.8111**


## 📄 Full Report

For detailed block diagrams, waveform outputs, and analysis:
👉 [Refer to the full project report](Fetal_ECG_Project_Report.pdf)


## 🧾 Future Work

- Implement simultaneous signal separation (instead of sequential extraction)
- Use **standardized reference signals** instead of dependent ones
- Explore **deep learning** for automatic ECG component detection


## 📚 References

1. [IEEE Paper: Hybrid Wavelet Denoising for fECG Extraction](https://ieeexplore.ieee.org/document/10229148)
2. [Elsevier: Denoising using Adaptive Wavelet Thresholding](https://www.sciencedirect.com/science/article/pii/S1875389212001435)


