# Analog Computer: Simulation of a Mass-Spring-Damper System

This project simulates the behavior of a second-order mechanical system using analog computation. We implemented a mass-spring-damper system using op-amp-based circuits, including summers, integrators, buffers, and a Deboo (Howland) integrator. The system's response is analyzed under free fall, damped motion, and spring oscillation scenarios.

## 📌 Abstract

Analog computing enables real-time simulation of physical systems through continuous-time electrical signals. This project leverages analog circuitry to model vertical motion governed by Newton’s second law. The simulation results are verified using LTspice and physical hardware.

## 🎯 Objectives

- Understand analog computing principles using operational amplifiers.
- Implement a second-order dynamic system using summers, integrators, and buffers.
- Explore advantages of the Deboo (Howland) integrator.
- Analyze system response under various physical scenarios.

## 📘 Theoretical Background

The governing equation is:

Where:
- `g`: gravity
- `b`: damping coefficient
- `k`: spring constant
- `m`: mass

## 🔧 Circuit Design

### Main Circuit Blocks

- **Summation Circuit**: Adds contributions from gravity, damping, and spring forces.
- **Integration Stages**: First integrator gives velocity; second gives displacement.
- **Buffer**: Prevents load effects.
- **Deboo Integrator**: Offers easy initialization and improved stability.

### Voltage Mapping

| Physical Quantity | Voltage |
|-------------------|---------|
| Acceleration (a)  | Va      |
| Velocity (v)      | Vv      |
| Displacement (y)  | Vy      |

*All voltages normalized to 1V = 1 unit.*

## 🧪 Simulation Cases

1. **Free Fall**
   - `b/m = 0`, `k/m = 0`
2. **Damped Motion**
   - `b/m = 1`, `k/m = 0`
3. **Spring Oscillation**
   - `b/m = 1`, `k/m = 5`, `g = 3.0 m/s²`

## 📊 Results Summary

| Case | Metric | Theoretical | Simulated | Experimental |
|------|--------|-------------|-----------|--------------|
| Free Fall | Velocity Saturation Time | 2.22s | 2.30s | 2.38s |
| Damped Fall | Position Saturation Time | 3.90s | 3.92s | 3.98s |
| Oscillation | Period (from y(t)) | 2.88s | 3.20s | 3.25s |

## 🧠 Key Questions

- **Why 2 integrators?**
  - Acceleration → Velocity → Displacement.
- **Why Deboo integrator?**
  - Stable, easily initialized, and capacitor-friendly.
- **Effect of damping?**
  - Higher damping → faster decay, lower terminal velocity.


## ✅ Conclusion

Analog simulation is an effective approach to model physical systems governed by differential equations. The Deboo integrator improves circuit accuracy and stability, allowing realistic visualization of mass-spring-damper dynamics.

---

