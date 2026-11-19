
# Multimodal Driver Health Monitoring System

### Real-Time Physiological Signal Acquisition, Sensor Fusion & Visualization

## Overview

A multimodal biomedical embedded system designed to acquire and visualize physiological and behavioral parameters during a driver monitoring session.

The platform integrates ECG, photoplethysmography (PPG), steering-wheel grip pressure, and inertial measurement data into a unified monitoring interface.

The system combines biomedical analog front-end interfacing, distributed sensor acquisition, embedded firmware, wireless communication, and real-time web-based visualization.

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/fca99be1-dbe3-48b5-91f3-a76bc96e529d" />


## Problem Statement

Driver physiological monitoring requires multiple sensing modalities to observe different aspects of a driver's physiological and physical state.

Monitoring each parameter independently makes synchronized interpretation and real-time observation difficult.

## Proposed Solution

Developed a multi-modal biosignal acquisition platform integrating:

1. ECG acquisition using the ADS1299 analog front-end.
2. Steering-wheel grip pressure measurement using a 12-channel FSR array.
3. PPG acquisition using the MAX30105 sensor.
4. Motion sensing using an IMU.
5. Arduino Due-based embedded acquisition firmware.
6. Browser-based visualization with animated biosignal waveforms and a steering-wheel pressure heatmap.

## System Architecture

```text
ADS1299 ───── ECG Acquisition ──────┐
                                    |
12-Channel FSR ─ Grip Pressure ─────┤
                                    |
MAX30105 ───── PPG Acquisition ─────┤
                                    |
IMU ────────── Motion Data ─────────┤
                                    |
                                    v
                             Arduino Due
                                    |
                                    v
                          Communication Layer
                                    |
                                    v
                          Mobile / Web Interface
                                    |
                                    v
                        Real-Time Monitoring UI
```

## Key Features

- Multi-modal physiological data acquisition.
- ECG acquisition through ADS1299.
- 12-channel steering-wheel pressure sensing.
- PPG acquisition through MAX30105.
- IMU-based motion monitoring.
- Real-time biosignal visualization.
- Animated ECG and PPG waveforms.
- Steering-wheel grip-pressure heatmap.
- Integrated driver-session monitoring interface.

## Hardware Stack

| Component | Function |
|---|---|
| Arduino Due | Main embedded controller |
| ADS1299 | Multi-channel biopotential acquisition front-end |
| MAX30105 | Optical PPG sensing |
| FSR × 12 | Steering-wheel grip-pressure sensing |
| IMU | Motion and orientation sensing |
| BLE | Wireless communication |

## Software Stack

- Embedded C / Arduino firmware.
- HTML.
- CSS.
- JavaScript.
- Browser-based visualization.
- BLE communication.

## Engineering Implementation

### 1. ECG Acquisition

Integrated the ADS1299 front-end to acquire ECG signals for physiological waveform monitoring.

### 2. Grip Pressure Monitoring

Implemented a 12-channel force-sensitive resistor array distributed across the steering wheel.

The pressure readings are mapped into a heatmap to visualize the driver's grip distribution.

### 3. PPG Acquisition

Integrated the MAX30105 optical sensor to acquire PPG signals for pulse-related waveform visualization.

### 4. Motion Monitoring

Integrated an IMU to capture motion-related measurements during the driver monitoring session.

### 5. Visualization

Developed a browser-based dashboard combining physiological waveforms, motion measurements, and spatial grip-pressure visualization.

## Project Outcome

Established a working multi-channel acquisition and visualization pipeline integrating ECG, PPG, IMU, and grip-pressure measurements into a unified driver monitoring interface.

The implementation demonstrates biomedical sensor integration, embedded acquisition, wireless communication, and real-time data visualization.

## Future Enhancements

- Physiological feature extraction.
- ECG-derived heart-rate analysis.
- PPG-based pulse analysis.
- Driver drowsiness research.
- Sensor synchronization improvements.
- Signal-quality assessment.
- Edge-based anomaly detection.

## Applications

- Driver physiological monitoring research.
- Biomedical instrumentation.
- Multimodal biosignal acquisition.
- Human-machine interaction.
- Automotive health-monitoring research.

## Disclaimer

This project is an engineering and research prototype. It is not a certified medical device and should not be used for clinical diagnosis or safety-critical driver decisions.

---

**Project Category:** Biomedical Embedded Systems | Biosignal Processing | Sensor Fusion

**Status:** Working Prototype
