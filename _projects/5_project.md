---
layout: page
title: "Robot Sensing and Navigation"
published: true
group: work
permalink: /projects/robot-navigation/
img: /assets/img/projects/rsn.png
importance: 5
tags: [sensor fusion, IMU, navigation, Python, complementary filter, dead reckoning]
---
## Overview

Implemented sensor fusion techniques combining IMU (accelerometer, gyroscope, magnetometer) and GPS data to estimate vehicle trajectory through dead reckoning. The project demonstrates practical challenges in inertial navigation, sensor calibration, and the critical importance of multi-sensor fusion for accurate localization.

**Key Challenge:** Maintain accurate position and heading estimates from noisy, drifting IMU sensors over extended trajectories using only dead reckoning.

---

## Magnetometer Calibration

### Two-Step Calibration Process

**Hard-Iron Correction:** Removed constant magnetic offset from car's speakers, motors, battery, and steel chassis by centering data at origin.

**Soft-Iron Correction:** Corrected orientation-dependent scaling from ferromagnetic materials (steel body, engine block) by normalizing each axis, transforming elliptical distribution to circular.

**Result:** Successfully corrected both distortion types, enabling accurate heading computation from calibrated magnetometer data.

---

## Complementary Filter for Heading Estimation

### Sensor Fusion Strategy

Fused gyroscope and magnetometer to leverage complementary strengths:
- **Gyroscope:** High-frequency, responsive but drifts over time
- **Magnetometer:** Absolute reference, no drift but noisy

**Filter Equation:**
```
ψₖ = α·(ψₖ₋₁ + ωz·Δt) + (1-α)·ψₘₐg
```

### Alpha Optimization Results

| Alpha (α) | Path Length Error | Endpoint Error |
|-----------|------------------|----------------|
| **0.90** | 4.2 m (0.13%) | **995.3 m** |
| 0.95 | 4.2 m (0.13%) | 1000.3 m |
| 0.98 | 4.2 m (0.13%) | 1013.4 m |
| 0.99 | 4.2 m (0.13%) | 1027.5 m |

**Selected α = 0.90** for best endpoint accuracy. Cutoff frequency: ~0.64 Hz at 40 Hz sample rate provides 1.5-second drift correction window.

---

## Velocity Estimation & Correction

### Three-Stage Correction Pipeline

**1. Accelerometer Bias Correction**
```python
# Estimate bias from stationary periods
accel_bias = np.mean(ax[stationary_mask])
ax_corrected = ax - accel_bias
```

**2. Zero-Velocity Updates (ZUPT)**
```python
# Force velocity to zero during known stops
v_forward[stationary_mask] = 0.0
```

**3. Velocity Scaling**
```python
# Correct systematic scale factor error
scale_factor = 0.139  # GPS reference
v_forward_scaled = v_forward * scale_factor
```

### Performance Improvement

| Metric | Before Correction | After Correction |
|--------|------------------|------------------|
| Mean Velocity | 30.18 m/s | 4.20 m/s |
| Path Length Error | >19,000 m | **4.2 m (0.13%)** |

---

## Dead Reckoning Performance

### Trajectory Estimation vs GPS Ground Truth

| Metric | GPS | IMU Dead Reckoning |
|--------|-----|-------------------|
| **Path Length** | 3179.1 m | 3183.3 m |
| **Path Error** | - | 4.2 m (0.13%) |
| **Endpoint Error** | - | 995.3 m |
| **Agreement Duration** | - | **2.0 seconds** |

### Position Error Growth

| Time | Position Error |
|------|---------------|
| 2s | 2 m |
| 10s | 14.4 m |
| 60s | 191.7 m |
| 300s | 545.0 m |
| 757s | 1039.3 m |

**Critical Finding:** Despite 0.13% path length accuracy, position diverged within 2 seconds and accumulated to 1 km error by journey end.

---

## Key Insights

**Why Dead Reckoning Failed:**
- Small heading errors (<1°) accumulate rapidly when integrated over distance
- Excellent velocity magnitude but wrong direction → spiraling trajectory
- Complementary filter balances noise and drift but cannot eliminate accumulation

**Lateral Acceleration Analysis:**
- Expected (v·ωz) vs observed (ay) correlation: only 0.231
- Gravity from vehicle roll and road banking dominates measurements
- Suspension dynamics and sensor misalignment add significant noise

**Practical Navigation Requirements:**
- Position updates every 10-30 seconds essential
- True heading initialization critical for early accuracy
- Advanced sensor fusion (EKF) needed for GPS integration
- Additional sensors (wheel odometry, visual odometry) improve velocity estimates

---

## Technical Skills Demonstrated

- **Sensor Calibration:** Hard-iron/soft-iron magnetometer correction, accelerometer bias removal
- **Sensor Fusion:** Complementary filtering, optimal parameter tuning (α selection)
- **Signal Processing:** ZUPT, coordinate transformations, signal unwrapping
- **Navigation Algorithms:** Dead reckoning, trajectory integration, error propagation analysis
- **Data Analysis:** GPS ground truth comparison, systematic error identification
- **Tools:** Python, NumPy, SciPy, Matplotlib

---

## Conclusion

Successfully implemented complete IMU-based navigation pipeline demonstrating both the power and fundamental limitations of dead reckoning. Complementary filter reduced endpoint error by 3% compared to higher alpha values, but position accuracy degraded to 1 km over 12 minutes despite 0.13% path length accuracy.

**Key Learning:** Accurate velocity magnitude is insufficient—small heading errors dominate long-term position accuracy, making periodic absolute position updates essential for practical autonomous navigation.

