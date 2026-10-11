---
layout: home
permalink: index.html
repository-name: e22-3yp-Ventra
title: Ventra - BVM Ventilation Feedback and Training System
---

# Ventra

### Design and Evaluation of a Low-Cost, Real-Time Multimodal Feedback System for Bag-Valve-Mask Ventilation Training

**Third Year Project | Department of Computer Engineering | University of Peradeniya**

**Group Name:** TechWhiz  
**Group Number:** 15

---

## Team

- E/22/397 - R. Thilakshan
- E/22/381 - S. Monisha
- E/22/337 - K. Sadurshika
- E/22/409 - S. Vikashan

---

## Table of Contents

1. [Introduction](#introduction)
2. [Objectives](#objectives)
3. [Solution Architecture](#solution-architecture)
4. [Hardware and Software Designs](#hardware-and-software-designs)
5. [Testing and Validation](#testing-and-validation)
6. [Detailed Budget](#detailed-budget)
7. [Expected Outcomes](#expected-outcomes)
8. [Conclusion](#conclusion)
9. [Links](#links)

---

## Introduction

Bag-Valve-Mask (BVM) ventilation is an important emergency medical procedure used to provide breathing support. During conventional training, trainees rely mainly on visual chest movement, bag compression feel, and instructor observation.

However, conventional BVM devices do not directly display important ventilation parameters such as delivered air volume, ventilation rate, airway pressure, and mask leakage.

**Ventra** is a proposed low-cost, real-time ventilation feedback and assessment system designed to improve BVM training using objective measurements and corrective feedback.

The system will measure airflow and airway pressure, calculate breath-by-breath ventilation parameters, and provide immediate feedback to trainees.

An offline instructor dashboard will support training performance analysis, session recording, and objective OSCE assessments.

The initial system will be developed for adult BVM training using a manikin.

## Objectives

The main objectives of Ventra are:

1. Measure airflow and airway pressure during BVM ventilation.
2. Calculate inspired and expired tidal volume.
3. Determine ventilation rate, inspiratory time, and peak airway pressure.
4. Estimate air leakage and volume differences.
5. Provide immediate corrective feedback to trainees.
6. Develop an offline instructor monitoring dashboard.
7. Record ventilation data for performance evaluation and OSCE assessment.
8. Validate the system against calibrated reference equipment.
9. Investigate whether feedback improves ventilation consistency.

## Solution Architecture

The proposed system will use a sensor adapter positioned between the BVM patient valve and the training mask.

### Ventilation Circuit

BVM Bag → Patient Valve → Ventra Sensor Adapter → Mask → Training Manikin

### Data Processing

Flow and Pressure Sensors → ESP32-S3 → Signal Processing → Ventilation Parameter Calculation → Real-Time Feedback

### Communication

ESP32-S3 → Wi-Fi/USB → LocalHub → Instructor Dashboard

The system will operate locally without requiring an internet connection.

Sensor placement will be carefully designed to minimize interference with normal BVM ventilation and mask positioning.

## Hardware and Software Designs

### Hardware Components

| Component | Purpose |
|---|---|
| ESP32-S3 | Main processing and communication |
| Bidirectional airflow sensor | Measure inspiratory and expiratory airflow |
| Airway pressure sensor | Measure airway pressure |
| OLED display | Display measurements |
| RGB LEDs | Provide immediate visual feedback |
| Buzzer | Provide optional timing and warning cues |
| Sensor adapter | Connect sensors to the ventilation circuit |
| Power supply | Provide portable power |

### Software Design

The embedded firmware will perform:

- Sensor calibration
- Real-time data acquisition
- Signal filtering
- Breath detection
- Tidal-volume calculation
- Pressure and ventilation-rate calculation
- Estimated leakage calculation
- Rule-based feedback generation

### Instructor Dashboard

The proposed Ventra LocalHub dashboard will provide:

- Live ventilation measurements
- Training session monitoring
- Individual breath analysis
- Performance history
- Ventilation consistency analysis
- OSCE assessment support
- Data export

## Testing and Validation

### Phase 1: Engineering Validation

The prototype will be tested against calibrated reference equipment.

Planned measurements include:

- Airflow accuracy
- Tidal-volume accuracy
- Pressure accuracy
- Ventilation-rate accuracy
- Estimated leakage accuracy
- Feedback response time
- Measurement repeatability

Tests will also compare ventilation with and without the sensor adapter to evaluate its effect on normal airflow, pressure, and mask positioning.

### Phase 2: Training Evaluation

A controlled manikin-based training study is proposed, subject to the necessary approvals.

Two training conditions will be compared:

- Conventional BVM training without real-time feedback
- BVM training with Ventra feedback enabled

The study will investigate ventilation consistency, measurement errors, and compliance with selected training targets.

**Status:** Testing and validation are planned. Experimental results will be added after implementation.

## Detailed Budget

The budget will be finalized after component selection and supplier quotations.

| Component | Quantity | Estimated Cost |
|---|---:|---|
| ESP32-S3 | 1 | To be confirmed |
| Airflow sensor | 1 | To be confirmed |
| Airway pressure sensor | 1 | To be confirmed |
| OLED display | 1 | To be confirmed |
| LEDs and buzzer | As required | To be confirmed |
| Sensor adapter and enclosure | 1 | To be confirmed |
| Power supply | 1 | To be confirmed |

## Expected Outcomes

The project aims to deliver:

- A functional BVM ventilation measurement prototype
- Real-time corrective feedback
- A local instructor dashboard
- Recorded ventilation datasets
- Experimental validation results
- An evaluation of feedback effectiveness

## Conclusion

Ventra aims to improve the objectivity and consistency of BVM ventilation training through affordable sensing, real-time feedback, and performance analysis.

The system is intended for manikin-based education and research only. It is not designed or certified for clinical use on patients.

## Links

- [Project Repository](https://github.com/cepdnaclk/e22-3yp-Ventra)
- [Project Webpage](https://cepdnaclk.github.io/e22-3yp-Ventra/)
- [Department of Computer Engineering](https://www.ce.pdn.ac.lk/)
- [University of Peradeniya](https://eng.pdn.ac.lk/)
