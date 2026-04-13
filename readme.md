# Signal Processing and Frequency Component Isolation

## Overview
This repository contains a suite of MATLAB scripts and documentation dedicated to signal processing. It explores the complete workflow of analyzing a signal, from its basic time-frequency representation through complex filtering and modulation techniques.

## Repository Structure
The project is divided into three core analytical modules:

### 1. `A1_time_frequency`
Focuses on the fundamental analysis of signals in both the time and frequency domains.
- Generation of composite sine wave signals.
- Application of Fast Fourier Transform (FFT) to visualize frequency spectrums.
- Identification of dominant frequency peaks and spectral leakage.

### 2. `A2_filtering`
Demonstrates the isolation and rejection of specific frequency components using logical filter designs.

**Input Signal:**
$$Signal = A_1\sin(2\pi \cdot 100t) + A_2\sin(2\pi \cdot 200t) + A_3\sin(2\pi \cdot 300t) + A_4\sin(2\pi \cdot 400t)$$

**Filter Design Parameters:**
| Target Frequency Component | Filter Type | Cutoff Frequency/Frequencies |
| :--- | :--- | :--- |
| **100 Hz** | Low Pass Filter (LPF) | 150 Hz |
| **400 Hz** | High Pass Filter (HPF) | 350 Hz |
| **100 Hz and 200 Hz** | Low Pass Filter (LPF) | 250 Hz |
| **200 Hz** | Band Pass Filter (BPF) | 150 Hz and 250 Hz |
| **300 Hz** | Band Pass Filter (BPF) | 250 Hz and 350 Hz |
| **300 Hz and 400 Hz** | High Pass Filter (HPF) | 250 Hz |
| **200 Hz and 300 Hz** | Band Pass Filter (BPF) | 150 Hz and 350 Hz |
| **200 Hz, 300 Hz, and 400 Hz** | High Pass Filter (HPF) | 150 Hz |
| **100 Hz and 400 Hz** | Band Stop Filter (BSF) | 150 Hz and 350 Hz |

### 3. `A3_modulation`
Explores the application of modulation techniques to prepare baseband signals for transmission.
- Implementation of carrier wave modulation.
- Visualization of the modulated signal envelope in the time domain.
- Analysis of sidebands in the frequency domain.

## Requirements
- **MATLAB** (The Signal Processing Toolbox is recommended for optimal execution of filtering and FFT functions).

## Usage
1. Clone the repository.
2. Open MATLAB and navigate to the root directory.
3. Open the respective folders (`A1_time_frequency`, `A2_filtering`, `A3_modulation`) and run the `.m` scripts to generate the signal plots and data outputs.
4. For detailed theoretical breakdowns, refer to the included `report.md`.
