# Frequency Component Isolation - Filter Design

## Overview
This documentation outlines the theoretical filter design required to isolate specific frequency components from a composite input signal. The objective is to determine the correct filter types and cutoff frequencies to separate signals effectively.

## Input Signal
The composite input signal is defined as the sum of four distinct sine waves:

$$Signal = A_1\sin(2\pi \cdot 100t) + A_2\sin(2\pi \cdot 200t) + A_3\sin(2\pi \cdot 300t) + A_4\sin(2\pi \cdot 400t)$$

## Filter Design Parameters
The following table specifies the filter types and theoretical cutoff frequencies used to isolate or reject target components. Cutoff frequencies are placed midway between the frequencies to provide optimal separation.

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

## Technical Logic
- **LPF (Low Pass):** Used when the target signals are at the lower end of the spectrum.
- **HPF (High Pass):** Used when the target signals are at the higher end of the spectrum.
- **BPF (Band Pass):** Used to isolate a specific range or a single middle frequency.
- **BSF (Band Stop):** Used to reject middle frequencies while allowing the extremes (100 Hz and 400 Hz) to pass.
- **Cutoff Placement:** Selected at the $f \pm 50$ Hz mark to ensure the transition band does not interfere with the primary signal peaks.
