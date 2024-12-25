# Frequency Measurement System for Cyber-Physical Systems

## Overview

This project involves the design and implementation of a **frequency measurement system** for cyber-physical systems (CPS). The focus is on measuring frequencies between **0 and 400 kHz** using **Analog-to-Digital Converters (ADCs)** while adhering to precise sampling principles and selecting the most suitable ADC for the application.

### Key Features
- **Sampling Frequency Determination**: Based on the Nyquist criterion to avoid aliasing.
- **ADC Selection**: Evaluation of ADCs with various specifications, including resolution, sampling rate, and input voltage range.
- **Frequency Measurement**: Real-time measurement for CPS applications.

---

## How It Works

1. **Nyquist Criterion**:
   - Ensures the sampling frequency is at least twice the maximum signal frequency.
   - Minimum sampling frequency: `fsampling ≥ 2 × fmax = 800 kHz`.

2. **Aliasing Prevention**:
   - Anti-aliasing filters eliminate high-frequency components before ADC sampling.
   - Example: Incorrect sampling of a 10 kHz signal with 15 kHz leads to distorted frequencies.

3. **ADC Parameters**:
   - Resolution: Minimum 12-bit resolution for precise signal representation.
   - Sampling Rate: At least 1 MSPS (Mega Samples per Second).
   - Input Voltage Range: Matches the signal range (e.g., 0–5V).
   - Interface: SPI for fast and reliable communication.

---

## Components and Tools

### Hardware
- **ADCs Evaluated**:
  1. **ADS7038**: 12-bit, 1 MSPS, 8 configurable channels.
  2. **AD7265**: 12-bit, 1 MSPS, dual simultaneous sampling.
  3. **ADS7952**: 12-bit, 1 MSPS, 12 channels.

### Software
- **Programming Language**: Python
- **Libraries**: NumPy, Matplotlib, and SPI communication libraries.
- **Platform**: Ubuntu

---

## How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/frequency-measurement-cps.git
