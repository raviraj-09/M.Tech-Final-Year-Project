# Design and Performance Analysis of MTCMOS-Based RCA and Variable Block CSLA Architectures in 90 nm CMOS

## 📌 Project Overview

This project presents the transistor-level design and performance analysis of **Ripple Carry Adder (RCA)** and **Variable Block Carry Select Adder (CSLA)** architectures using **90 nm CMOS technology**.

The work focuses on achieving an optimized trade-off between **power consumption, propagation delay, leakage power, and energy efficiency** in low-power VLSI arithmetic circuits. To address the limitations of conventional adder architectures, **Multi-Threshold CMOS (MTCMOS)** based power gating is integrated using a **High-Vt PMOS header sleep transistor** for standby leakage reduction.

The designs were implemented and simulated using **Cadence Virtuoso and Cadence Spectre** under consistent simulation conditions.

---

## 🎯 Objectives

* Design transistor-level CMOS-based RCA and Variable Block CSLA architectures.
* Implement a **28-transistor CMOS Full Adder** as the basic arithmetic building block.
* Design a **Transmission-Gate-based 2:1 Multiplexer** for CSLA carry selection.
* Develop 4-bit, 8-bit, 16-bit, and 32-bit RCA architectures.
* Develop 2-bit, 4-bit, 8-bit CSLA architectures.
* Develop 16-bit and 32-bit Variable Block CSLA architectures.
* Integrate **MTCMOS power gating** using a High-Vt PMOS header sleep transistor.
* Analyze sleep transistor sizing and its effect on leakage and propagation delay.
* Compare architectures based on **power, leakage power, propagation delay, and Power Delay Product (PDP)**.

---

## 🏗️ Architecture

### 1. 28T CMOS Full Adder

The Full Adder is used as the fundamental building block for the RCA and CSLA architectures.

It performs the addition of:

* Input `A`
* Input `B`
* Carry input `Cin`

and generates:

* `Sum`
* `Carry-out (Cout)`

### 2. Transmission-Gate 2:1 Multiplexer

A Transmission-Gate-based 2:1 MUX is used for carry selection in the CSLA architecture.

The MUX selects the appropriate output corresponding to the actual carry input after parallel carry computation.

### 3. Ripple Carry Adder

The RCA is constructed by cascading multiple Full Adder cells, where the carry output of one stage is connected to the carry input of the next stage.

Implemented configurations:

* 4-bit RCA
* 8-bit RCA
* 16-bit RCA
* 32-bit RCA

RCA provides a simple architecture and comparatively lower power consumption, but its propagation delay increases with bit width due to sequential carry propagation.

### 4. Variable Block CSLA

The CSLA performs parallel carry computation for different carry conditions and uses multiplexers to select the correct result.

Implemented configurations:

* 2-bit CSLA
* 4-bit CSLA
* 8-bit CSLA

Variable block grouping was used to balance carry propagation and MUX selection delays.

**16-bit CSLA:**
`2-2-3-4-5`

**32-bit CSLA:**
`2-2-3-4-5-6-10`

---

## ⚡ MTCMOS-Based Power Gating

To reduce standby leakage power, a **High-Vt PMOS header sleep transistor** is integrated between the supply voltage and the logic block.

### Active Mode

`Sleep = 0`

→ PMOS sleep transistor ON
→ Low-resistance path from VDD to the logic block
→ Virtual VDD approaches VDD
→ Normal circuit operation

### Standby Mode

`Sleep = 1`

→ PMOS sleep transistor OFF
→ Logic block isolated from VDD
→ Standby leakage significantly reduced

---

## 🔧 Sleep Transistor Optimization

Sleep transistor sizing was analyzed to investigate the trade-off between leakage power and propagation delay.

The selected implementation uses:

| Parameter         |        Value |
| ----------------- | -----------: |
| Device            | High-Vt PMOS |
| Finger Width      |       2.5 µm |
| Number of Fingers |          100 |
| Effective Width   |       250 µm |
| Channel Length    |       100 nm |

Increasing sleep transistor width reduces its ON resistance and IR drop, improving delay. However, excessive width introduces additional area, capacitance, and leakage overhead. Therefore, an effective width of **250 µm** was selected for balanced performance.

---

## 🧪 Simulation Environment

| Parameter        | Specification      |
| ---------------- | ------------------ |
| Design Tool      | Cadence Virtuoso   |
| Simulator        | Cadence Spectre    |
| Technology       | 90 nm Bulk CMOS    |
| PDK              | GPDK090            |
| Supply Voltage   | 1 V                |
| Temperature      | 27°C               |
| Load Capacitance | 5 fF               |
| Analysis         | Transient Analysis |

The same simulation environment and operating conditions were maintained for comparative evaluation.

---

## 📊 Performance Analysis

The implemented architectures were evaluated using:

* **Total Power**
* **Dynamic Power**
* **Leakage Power**
* **Propagation Delay**
* **Power Delay Product (PDP)**

### 32-bit RCA vs CSLA

| Parameter         | 32-bit RCA | 32-bit CSLA |
| ----------------- | ---------: | ----------: |
| Total Power       |   12.40 µW |    15.65 µW |
| Leakage Power     |   1.866 µW |    4.001 µW |
| Dynamic Power     |  10.534 µW |   11.650 µW |
| Propagation Delay |    2870 ps |     1375 ps |
| PDP               |  35.588 pJ |   21.519 pJ |

### Key Observation

* **RCA** provides lower power consumption and lower hardware complexity.
* **CSLA** provides significantly improved propagation delay.
* CSLA achieves a lower PDP despite its higher power consumption because of its substantially lower delay.
* MTCMOS power gating significantly reduces standby leakage while maintaining acceptable circuit performance.

---

## 📈 Key Contributions

1. Transistor-level implementation of RCA and Variable Block CSLA architectures.
2. Design of a **28T CMOS Full Adder** and **Transmission-Gate-based 2:1 MUX**.
3. Implementation of 4-bit to 32-bit RCA architectures.
4. Implementation of variable-block 16-bit and 32-bit CSLA architectures.
5. Integration of **High-Vt PMOS-based MTCMOS power gating**.
6. Sleep transistor sizing analysis for leakage-delay optimization.
7. Comparative evaluation of power, leakage, delay, and PDP.

---

## 🛠️ Tools & Technologies

* **Cadence Virtuoso**
* **Cadence Spectre**
* **90 nm CMOS / GPDK090**
* **CMOS Transistor-Level Design**
* **MTCMOS**
* **Power Gating**
* **Ripple Carry Adder (RCA)**
* **Carry Select Adder (CSLA)**
* **Transmission Gate Logic**
* **Low-Power VLSI Design**

---

## 📂 Repository Structure

```text
MTCMOS-RCA-CSLA-90nm/
│
├── README.md
│
├── diagrams/
│   ├── 28T-full-adder/
│   ├── TG-MUX/
│   ├── RCA/
│   ├── CSLA/
│   └── MTCMOS/
│
├── simulation-results/
│   ├── RCA/
│   ├── CSLA/
│   └── MTCMOS/
│
├── results/
│   └── performance-comparison/
│
└── documentation/
```

---

## 📚 Project Information

**Degree:** M.Tech – VLSI Design
**Institution:** Gaya College of Engineering, Gaya
**Project Duration:** December 2025 – August 2026
**Supervisor:** Dr. Mrinal Ranjan
**Co-Supervisor:** Dr. Rajan Sarkar

---

## 🔮 Future Scope

Future work can focus on:

* Extension to advanced technology nodes such as 45 nm and FinFET-based technologies.
* Post-layout parasitic analysis.
* Process and temperature variation analysis.
* IR-drop and reliability analysis.
* Comparison with other high-speed adder architectures such as CLA and parallel-prefix adders.
* Adaptive and dynamic power-gating techniques.

---

## 👨‍💻 Author

**Ravi Raj**  
M.Tech – VLSI Design  
Gaya College of Engineering, Gaya  
🌐 LinkedIn: **[Ravi Raj](https://www.linkedin.com/in/ravi-raj-06s1/)**
