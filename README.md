# Low-Power-BJT-Audio-Amplifier


![Status](https://img.shields.io/badge/Status-Completed-success)
![Power](https://img.shields.io/badge/Power-1.5V_DC-blue)
![Simulation](https://img.shields.io/badge/Tools-LTspice-orange)

## 📌 Abstract
This project details the design, simulation, and implementation of a low-power audio amplifier circuit utilizing Bipolar Junction Transistors (BJTs). The system is designed to operate on a single 1.5V battery, making it highly suitable for portable hearing aids and headphone drivers. The design prioritizes minimal component count, energy efficiency, and high gain (>40dB) while maintaining low distortion.

---

## ⚙️ Key Features
* **Low Voltage Operation:** Optimized for a single 1.5V AA battery supply.
* **Multi-Stage Amplification:** Utilizes a pre-amplifier, intermediate gain stage, and output driver for maximum signal fidelity.
* **High Gain:** Achieves a total voltage gain exceeding 40dB.
* **Low Noise:** Integrated decoupling and bypass networks to minimize power supply noise.
* **Cost-Effective:** Total prototype estimated cost is approximately ₹142 INR.

---

## 🔧 Technical Implementation

The circuit architecture consists of four main functional blocks:

### 1. Microphone Pre-Amplifier (Stage 1)
The input signal from the electret microphone is conditioned and amplified by transistor Q1 (BC547).
* **Biasing:** A voltage divider network sets the base voltage ($V_{B1}$) to ensure operation in the active region:
  $$V_{B1} = V_{CC} \times \frac{R_2}{R_1 + R_2}$$
* **Gain:** The voltage gain ($A_v$) for this stage is defined by the collector and emitter resistances:
  $$A_v = -\frac{R_C}{R_E}$$

---

### 2. Intermediate Gain (Stage 2)
Transistor Q2 provides secondary amplification. DC components are blocked between stages using coupling capacitors to preserve the operating point of each transistor.

---

### 3. Output Driver (Stage 3 & 4)
This stage utilizes a phase splitter (Q3) to drive the final power transistor (Q4 - BC337).
* **Impedance Matching:** The output impedance ($Z_{out}$) is matched to the headphone load ($Z_{load}$) to maximize power transfer:
  $$Z_{out} = Z_{load}$$
* **Filtering:** The output coupling capacitor ($C_5$) forms a high-pass filter with the load to determine the cutoff frequency:
  $$f_c = \frac{1}{2\pi R_{load}C_5}$$

---

## 📊 Simulation & Results

The circuit was simulated using **LTspice** and **Proteus Design Suite**.

| Parameter | Specification | Observed Result |
| :--- | :--- | :--- |
| **Supply Voltage** | 1.5V DC | Stable Operation |
| **Frequency Response** | 20Hz - 20kHz | Consistent Gain |
| **Voltage Gain** | > 40dB | ~40dB |
| **THD** | < 5% | < 5% (Clear Audio) |

---

### Waveform Analysis
![Simulation Results](assets)
*Figure 1: Input signal vs. Amplified Output showing >40dB gain.*

---

## 💰 Bill of Materials (BOM) & Cost Analysis

The prototype was constructed for accessibility and low cost.

| Component | Specification | Quantity | Approx Cost (INR) |
| :--- | :--- | :--- | :--- |
| **Transistors** | BC547 (x3), BC337 (x1) | 4 | ₹40 |
| **Microphone** | Electret Condenser | 1 | ₹20 |
| **Resistors** | Various (10kΩ - 1MΩ) | 9 | ₹9 |
| **Capacitors** | 0.1µF - 470µF | 7 | ₹35 |
| **Battery** | 1.5V AA | 1 | ₹10 |
| **Misc** | Switch, Jack, PCB | - | ~₹28 |
| **Total** | | | **₹142** |

---
## 🚀 How to Run the Simulation

### Option 1: LTspice (Circuit Analysis)
1.  **Prerequisite:** Ensure you have [LTspice XVII](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html) installed.
2.  Clone this repository.
3.  Open LTspice and navigate to `File > Open`.
4.  Select the `.asc` file located in the `/src` folder.
5.  Click the **Run** icon (running person) on the toolbar.
6.  **View Results:** Click on the **Microphone Input** node and the **Headphone Output** node to compare the amplification.

---


## 👥 Contributors
* **Kavya G**
* Nidhishree
* Hemashree GN
* Madeena bi

*Dept. of Electronics and Communication, The National Institute of Engineering, Mysore.*
