# EEG-Frequency-Band-Analysis

### 🧠 Project Description
This project analyzes EEG signals from the **PhysioNet Motor Imagery Dataset (EEGMMIDB)** using the **MNE-Python** library.  
It extracts power in key brainwave frequency bands (delta, theta, alpha, beta) and visualizes their spatial distribution across scalp channels.

---

### ⚙️ Tools & Libraries
- **Python**
- **MNE-Python**
- **NumPy**, **Matplotlib**, **SciPy**

---

### 🧩 Workflow
1. **Data Loading** — EEG data downloaded via `mne.datasets.eegbci`.
2. **Preprocessing** — Notch filter (50 Hz), band-pass (0.5–45 Hz), and resampling (128 Hz).
3. **Power Spectral Density (PSD)** — Computed via Welch method.
4. **Band Power Extraction** — Integrated PSD for Delta, Theta, Alpha, and Beta bands.
5. **Visualization**
   - Topographic maps of band power across electrodes.
   - Power spectral density plot for a representative channel.
   - Alpha-band Hilbert envelope (time-domain visualization).

---

### 🎯 Objective
To understand **EEG frequency band characteristics** and visualize how brainwave power varies across different scalp regions during motor imagery tasks.

---

### 🧾 Results
| Visualization | Description |
|----------------|--------------|
| ![Topomap](https://github.com/radhikadwivedi471/EEG-Frequency-Band-Analysis/raw/main/output/topomap.png) | Relative band power distribution (delta, theta, alpha, beta) |
| ![PSD](https://github.com/radhikadwivedi471/EEG-Frequency-Band-Analysis/raw/main/output/psd_fc5.png) | Power Spectral Density (PSD) for channel FC5 |
| ![Alpha Envelope](https://github.com/radhikadwivedi471/EEG-Frequency-Band-Analysis/raw/main/output/alpha_envelope.png) | Alpha band + Hilbert envelope visualization |

---

### 🚀 How to Run
```bash
pip install mne numpy scipy matplotlib
python eeg_band_power_topomap.py
