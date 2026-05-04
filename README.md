# 📡 Network Performance Analysis (EEN1058)
# Grade: 93%

**Author:** Kyle Sheehy  
**Date:** October 2025  

---

## 📘 Overview

This project presents a simulation-based analysis of WiFi network performance using OMNeT++ datasets and Python-based data processing.

The objective is to evaluate how key system parameters affect network behaviour, specifically:

- Bit rate  
- Distance  
- User density  
- Wireless standard (WiFi 6 vs WiFi 7)

The analysis focuses on three core performance metrics:

- Throughput  
- End-to-end delay  
- Packet Loss Ratio (PLR)

This repository is designed to highlight system behaviour, analysis methodology, and engineering insights, rather than raw implementation.

---

## ⚠️ Source Code Availability

To preserve academic integrity, full source code is not publicly available.

This repository instead provides:

- Processed datasets (CSV)  
- High-resolution visualisations  
- Simulation structure and methodology  
- Analysis outputs and key findings  

Full implementation details are available upon request for professional or academic review.

---

## 🔄 Data Processing Pipeline

```mermaid
flowchart TD
    A[OMNeT++ Simulation Outputs (.sca files)] --> B[Python Data Processing]
    B --> C[Structured Data (CSV)]
    C --> D[Metric Computation: Throughput, Delay, PLR]
    D --> E[Visualisation (Plots)]
    E --> F[Analysis & Insights]
```

---

## 🧩 Key Investigations

### 🔹 Question A — Bit Rate vs Performance

Evaluates how increasing transmission bit rate affects network performance.

**Scenarios:**
- 1 Mbps  
- 5 Mbps  
- 10 Mbps  
- 15 Mbps  
- 20 Mbps  

**Key Observations:**
- Throughput increases with bit rate until system limits are reached  
- Delay and packet loss increase under higher load  
- Diminishing returns observed at higher transmission rates  

---

### 🔹 Question B — Performance vs Distance

Analyses the effect of increasing distance between transmitter and receiver.

**Distance Range:**
- 0 m to 150 m  

**Key Observations:**
- Significant degradation beyond ~50 m  
- Connectivity breakdown observed in original simulation  
- Adjusted simulation required for controlled analysis  

**Important Distinction:**
- QuestionB-Original-Sim → real connectivity limitations  
- QuestionB-Altered-Sim → controlled evaluation  

---

### 🔹 Question C — WiFi 6 vs WiFi 7 Comparison

Compares performance across modern wireless standards.

**Parameters:**
- Distances: 0 m to 150 m  
- Users: 1, 10, 20, 50  

**Key Findings:**
- WiFi 7 achieves higher throughput under high user density  
- Lower delay in congested scenarios  
- Improved reliability (lower packet loss)  
- Performance gains increase with network load  

---

## 📊 Metrics Analysed

1. **Throughput (Kbps)**  
   Effective rate of successful data transmission  

2. **Delay (ms)**  
   Time taken for packets to traverse the network  

3. **Packet Loss Ratio (PLR)**  
   Fraction of packets lost during transmission  

---

## 🗂️ Repository Structure

- QuestionA/  
  Bit rate analysis datasets and visualisations  

- QuestionB-Original-Sim/  
  Raw simulation showing connectivity breakdown  

- QuestionB-Altered-Sim/  
  Adjusted simulation for controlled analysis  

- QuestionC/  
  WiFi 6 vs WiFi 7 datasets and comparison outputs  

- NS3-Fix/  
  Modified NS-3 files used during development  

- CSV files  
  Processed analysis outputs  

- PNG files  
  Generated plots and visualisations  

---

## 📈 Outputs

This repository includes:

- CSV datasets for all analyses  
- Throughput, delay, and PLR plots  
- Distance-based performance comparisons  
- WiFi 6 vs WiFi 7 comparative visualisations  

All figures are exported as high-resolution PNG files.

---

## ⚙️ Simulation & Data Notes

- Data is derived from OMNeT++ scalar output files (.sca)  
- Extracted values include:
  - Packet transmission counts  
  - Delay statistics  
  - Frame-level metrics  

**File Naming Convention:**
DataOfUser1-[distance]-[users]-[WiFiType]-[run].sca  

---

## 🛠️ Technical Skills Demonstrated

- Network simulation and modelling (OMNeT++, NS-3)  
- Wireless performance evaluation  
- Data extraction and processing (Python)  
- Analytical reasoning and interpretation  
- Debugging and adapting simulation environments  

---

## 📌 Summary

This project demonstrates how wireless network performance is strongly influenced by:

- Bandwidth constraints  
- Physical distance  
- Network congestion  

It highlights the importance of simulation-driven analysis when designing and evaluating communication systems.

---

## 📜 License

This work was developed as part of academic coursework at DCU.  
All rights reserved.
