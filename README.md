# RC Low-Pass Filter Design and Analysis Using Cadence Virtuoso

## 📌 Project Overview

This project demonstrates the design, mathematical analysis, and simulation of a first-order RC Low-Pass Filter (LPF) using **Cadence Virtuoso**.

The project involves theoretical cutoff frequency calculation, circuit schematic design, AC frequency-response analysis, and pole-zero analysis using the Analog Design Environment (ADE L).

The objective is to understand the frequency-domain behavior of an RC low-pass filter and verify its theoretical characteristics through circuit simulation.

## ⚙️ Circuit Specifications

| Parameter              |                          Value |
| ---------------------- | -----------------------------: |
| Resistor (R)           |                           1 MΩ |
| Capacitor (C)          |                           1 pF |
| AC Input Voltage       |                            1 V |
| Filter Type            | First-Order RC Low-Pass Filter |
| Simulation Tool        |               Cadence Virtuoso |
| Simulation Environment |                          ADE L |

## 🧮 Mathematical Calculation

The cutoff frequency of a first-order RC low-pass filter is given by:

$$
f_c = \frac{1}{2\pi RC}
$$

Where:

- (R) = Resistance
- (C) = Capacitance
- (f_c) = Cutoff frequency

Substituting the component values:

$$
R = 1 \times 10^6 \ \Omega
$$

$$
C = 1 \times 10^{-12} \ F
$$

Therefore,

$$
f_c = \frac{1}{2\pi \times 10^6 \times 10^{-12}}
$$

The theoretical cutoff frequency is:

$$
\boxed{f_c \approx 159.154 \text{ kHz}}
$$

## 🔌 Circuit Schematic

The RC low-pass filter consists of a resistor connected in series with the input and a capacitor connected between the output node and ground.

**Circuit configuration:**

- Input signal: AC voltage source of 1 V.
- Resistor: 1 MΩ.
- Capacitor: 1 pF.
- Output: Measured across the capacitor.



## 🖥️ AC Simulation Setup

The circuit was simulated using the **ADE L (Analog Design Environment L)** in Cadence Virtuoso.

### AC Analysis Configuration

| Setting         | Value     |
| --------------- | --------- |
| Analysis Type   | AC        |
| Start Frequency | 1 Hz      |
| Stop Frequency  | 1 GHz     |
| Sweep Type      | Automatic |

### AC Simulation Results

The AC simulation demonstrates the expected low-pass filter characteristics:

- At low frequencies, the output closely follows the input.
- Near the cutoff frequency, the output begins to decrease.
- At higher frequencies, the capacitor increasingly attenuates the output signal.



### Theoretical vs. Simulated Results

| Parameter                    |   Frequency |
| ---------------------------- | ----------: |
| Theoretical Cutoff Frequency | 159.154 kHz |
| Simulated Cutoff Frequency   | 158.644 kHz |
| Difference                   |   0.510 kHz |

The simulated result closely matches the theoretical calculation. The small discrepancy is attributed to the ideal assumptions used in the mathematical calculation compared with the simulation environment.

## 📍 Pole-Zero Analysis

Pole-zero analysis was also performed using the **ADE L** environment in Cadence Virtuoso to examine the filter's pole location.

### Pole-Zero Analysis Configuration

The following settings were used:

| Parameter            | Configuration                      |
| -------------------- | ---------------------------------- |
| Analysis Type        | Pole-Zero (PZ)                     |
| Output Type          | Voltage                            |
| Positive Output Node | `/net2`                            |
| Negative Output Node | Ground (left blank)                |
| Input Source         | `/V2`                              |
| Sweep Variable       | Component/Parameter (not selected) |

### Analysis Procedure

1. Open the ADE L simulation environment.
2. Select **Pole-Zero Analysis (pz)** from the available analysis options.
3. Configure the output type as voltage.
4. Set the positive output node to `/net2`.
5. Set the input voltage source to `/V2`.
6. Leave the negative output node empty.
7. Enable the analysis and run the simulation.
8. Navigate to **Direct Plot → Main Form → PZ** to display the pole-zero plot.

### Pole-Zero Plot



The pole-zero plot provides a graphical representation of the filter's pole location in the complex frequency plane.

For an ideal first-order RC low-pass filter, the transfer function is:

$$
H(s) = \frac{1}{1+sRC}
$$

The filter has one real pole at:

$$
s = -\frac{1}{RC}
$$

This pole determines the filter's natural frequency response and contributes to its first-order roll-off characteristics.

## 🛠️ Tools and Technologies

- Cadence Virtuoso
- Analog Design Environment (ADE L)
- AC Frequency Response Analysis
- Pole-Zero Analysis
- RC Circuit Design

## 📚 Key Learning Outcomes

- Understanding the operation of a first-order RC low-pass filter.
- Calculating the theoretical cutoff frequency.
- Designing an RC circuit using Cadence Virtuoso.
- Configuring and performing AC frequency-response analysis.
- Understanding pole locations and their relationship to filter behavior.
- Performing pole-zero analysis using ADE L.
- Comparing theoretical calculations with simulation results.

## 👨‍💻 Author

**Sheikh Tariful Islam**

Electrical and Electronic Engineering

Bangladesh University of Engineering and Technology (BUET)
