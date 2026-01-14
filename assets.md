# Simulation Results

<img width="1363" height="659" alt="Image" src="https://github.com/user-attachments/assets/dbabbaca-4c3e-49ae-bf08-992f67e2eb28" />

**Performance Breakdown:**
* **Input Signal:** 1mV Peak (2mV Peak-to-Peak).
* **Output Signal (Red Trace):** Swings from ~0.9V to 1.35V.
* **Peak-to-Peak Output ($V_{pp}$):** Approximately **450mV**.

**Gain Calculation:**
$$Gain (A_v) = \frac{V_{out(pp)}}{V_{in(pp)}} = \frac{450mV}{2mV} \approx 225$$
$$Gain (dB) = 20 \log(225) \approx \mathbf{47 dB}$$

**Verdict:**
* ✅ **Pass:** The calculated gain of **47dB** exceeds the project requirement of >40dB.
* ✅ **Signal Health:** The output waveform shows no clipping at the peaks or troughs, indicating that the transistors are correctly biased in the active region.
* ✅ **Efficiency:** The circuit achieves a clean 450mV swing using only a 1.5V supply, validating the low-power design.
