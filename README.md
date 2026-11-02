# Low-Pass Filter (LPF) Design and AC Simulation Using Cadence Virtuoso

## 📌 Project Overview

This project demonstrates the mathematical design and AC simulation of a first-order RC Low-Pass Filter (LPF) using **Cadence Virtuoso**.

The objective is to calculate the theoretical cutoff frequency of an RC low-pass filter and verify its frequency response through AC analysis.

## ⚙️ Circuit Specifications

| Parameter | Value |
|---|---:|
| Resistor (R) | 1 MΩ |
| Capacitor (C) | 1 pF |
| AC Input Voltage | 1 V |
| Filter Type | First-Order RC Low-Pass Filter |
| Simulation Type | AC Analysis |
| Simulation Tool | Cadence Virtuoso |

## 🧮 Mathematical Calculation

The cutoff frequency of a first-order RC low-pass filter is given by:

\[
f_c = \frac{1}{2\pi RC}
\]

Where:
- \(R\) = Resistance
- \(C\) = Capacitance
- \(f_c\) = Cutoff frequency

Substituting the component values:

\[
R = 1 \times 10^6 \ \Omega
\]

\[
C = 1 \times 10^{-12} \ F
\]

Therefore,

\[
f_c = \frac{1}{2\pi \times 10^6 \times 10^{-12}}
\]

\[
\boxed{f_c \approx 159.154 \text{ kHz}}
\]

## 🔌 Circuit Schematic

The RC low-pass filter consists of a resistor connected in series with the input and a capacitor connected between the output node and ground.

**Circuit configuration:**
- Input signal: AC voltage source of 1 V.
- Resistor: 1 MΩ.
- Capacitor: 1 pF.
- Output: Measured across the capacitor.

## 🖥️ Simulation Setup

The circuit was simulated using the **ADE L (Analog Design Environment L)** in Cadence Virtuoso.

### AC Analysis Configuration

| Setting | Value |
|---|---|
| Analysis Type | AC |
| Start Frequency | 1 Hz |
| Stop Frequency | 1 GHz |
| Sweep Type | Automatic |

The frequency response was observed using an AC response plot.

## 📊 Simulation Results

The AC simulation demonstrates the expected low-pass filter characteristics:

- At low frequencies, the output closely follows the input.
- Near the cutoff frequency, the output begins to decrease.
- At higher frequencies, the capacitor increasingly attenuates the output signal.

The simulated cutoff frequency is approximately **158.644 kHz**, which is close to the theoretically calculated value of **159.154 kHz**.

### Theoretical vs. Simulated Results

| Parameter | Frequency |
|---|---:|
| Theoretical Cutoff Frequency | 159.154 kHz |
| Simulated Cutoff Frequency | 158.644 kHz |
| Difference | 0.510 kHz |

The small discrepancy between theoretical and simulated results can be attributed to the ideal assumptions used in the mathematical calculation and the simulation environment.

## 🛠️ Tools and Technologies

- Cadence Virtuoso
- Analog Design Environment (ADE L)
- AC Frequency Response Analysis
- RC Circuit Design

## 📚 Key Learning Outcomes

- Understanding the operation of a first-order RC low-pass filter.
- Calculating the theoretical cutoff frequency.
- Designing an RC circuit using Cadence Virtuoso.
- Configuring AC analysis in ADE L.
- Analyzing frequency response and verifying theoretical calculations through simulation.

## 👨‍💻 Author

**Imamul Hossain Rafi**

Electrical and Electronic Engineering

Bangladesh University of Engineering and Technology (BUET)
