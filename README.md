# Arrhythmia Detection and other analysis 💟🩺
<img src="https://cdn.discordapp.com/attachments/1117028520313491526/1307351310512951407/image.png?ex=6739fd49&is=6738abc9&hm=1c2c2c587e8ff009d28c011a15320df39582657e6daf968908fe72916111b827&">
<p align="center">📈10 sec ECG REPORT📈</p>
<img src="https://cdn.discordapp.com/attachments/1117028520313491526/1307353376098488460/Figure_1.png?ex=6739ff36&is=6738adb6&hm=1ca8ad4dec603fbbd67bd0d411e96b65b7dfb6ac0193d00990b493d0eeaea673&">

<p align="center">📉OUTPUT AFTER ANALYSIS📉</p>

## ❣Overview❣
This project processes ECG data (10 sec)📈 to detect heartbeats, calculate heart rate, and assess potential arrhythmia. The code uses wavelet transforms to analyze high-frequency components of the ECG signal, such as R-peaks, and provides insights into heart rate and rhythm analysis.

## ❣Key Concepts❣:
1. 🧹**Data Loading and Cleaning**:
   - Load ECG data from a CSV file.
   - Clean the data and prepare it for further analysis.

2. 👩‍💻**Wavelet Transform (MODWT)**:
   - Perform a 4-level undecimated wavelet transform using the `sym4` wavelet.
   - Focus on **high-frequency components** to capture sharp R-peaks.
   - Filter out lower-frequency components, which represent baseline wander.

3. 🗻**R-Peak Detection**:
   - Square the magnitude of the wavelet-reconstructed signal to emphasize the R-peaks.
   - Use `scipy.signal.find_peaks` to detect R-peaks and analyze heartbeats.

4. 🩺**RR Intervals and Heart Rate Calculation**:
   - Calculate RR intervals (time between consecutive R-peaks) to measure heart rate variability.
   - Compute the heart rate in beats per minute (BPM).

5. 🩺**Arrhythmia Detection**:
   - Calculate the coefficient of variation (CV) of RR intervals to assess arrhythmia.
   - Compare CV to a predefined threshold to flag potential arrhythmic conditions.

6. 📊**Visualization**:
   - Plot the original ECG signal.
   - Mark detected R-peaks on the graph for visualization.

## Dependencies in python🐍:
- `numpy`
- `pandas`
- `matplotlib`
- `scipy`
- `pywt`



