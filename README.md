# Automated Pan-Tilt Camera System for Robotics Data Collection  
### UC Berkeley BEST Lab — Automated Multi-Position Capture Pipeline

[📊 Final Presentation Deck](https://docs.google.com/presentation/d/1nsxHX7we-lnv3eeDNjGJuIvo95ZkrrNJ-W7s_c3Zpow/edit?usp=sharing)

This project automates a pan-tilt camera system to collect multi-angle robotics datasets across **135 predefined positions**, reducing collection time from **2 hours → under 4 minutes**.  
Developed in the **Berkeley Emergent Space Tensegrities (BEST) Lab**, this pipeline significantly improves reliability, control accuracy, and experiment throughput.

---

## Project Overview
Manual data collection in the lab was slow, error-prone, and inconsistent.  
To solve this, I built a fully automated capture system that:
- Commands a pan-tilt rig via wireless modules  
- Captures synchronized images at each grid position  
- Implements retry logic, stuck detection, and recovery  
- Logs encoder data and performance metrics  
- Produces robust, repeatable multi-angle datasets

This system is now actively used in the BEST Lab for robotics experiments.

---

## Technical Summary

### 1. Automated Camera Motion (135 Positions)
- Python control pipeline using XBee wireless modules  
- Automatic stepping through full grid  
- Multi-threaded camera acquisition with low-latency capture  

---

### 2. Wireless Reliability Engineering
Original system had **~15% packet loss** and no recovery.

**Result:**  
- Reliability improved **85% → 100%**  
- Stuck detection improved **4s → 1s (75% faster)**  

---

### 3. PID Control Optimization
Using **950+ encoder samples**, I tuned PID gains and analyzed error distributions.

**Results:**
- Mean error: **1.93° → 0.82°** (57.5% improvement)  
- Max error: **8° → 2°** (75% improvement)  
- **87.4%** of positions within **1°** accuracy  

---

### 4. End-to-End System Speedup
- Manual workflow: ~2 hours  
- Automated system: <4 minutes  

→ **97% reduction in data collection time**

This enabled larger datasets, more trials per day, and finer-grained robotic motion studies.

---

## 📈 Key Results

| Metric | Before | After | Improvement |
|--------|--------|--------|-------------|
| Mean Error | 1.93° | 0.82° | 57.5% |
| Max Error | 8° | 2° | 75% |
| Reliability | 85% | 100% | +15% |
| Stuck Detection | 4s | 1s | 75% faster |
| Collection Time | 2 hrs | <4 mins | 97% faster |

More figures and plots are available in the presentation deck.

---

## Code Availability

This project was developed within the **Berkeley BEST Lab**.  
Due to lab policy and hardware interface confidentiality:
### Source code, firmware scripts, and control interfaces cannot be open-sourced.

This repository therefore provides:
- High-level documentation  
- System architecture  
- Final results & performance metrics  
- Presentation deck  

But does **not** include internal lab code.
