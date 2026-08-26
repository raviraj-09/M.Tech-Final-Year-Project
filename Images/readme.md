# Project Images

This document contains the major circuit schematics, architectures, simulation waveforms, MTCMOS implementations, and performance analysis figures associated with the project.

---

# 1. Design Methodology

## 1.1 Overall Design Methodology Flowchart

The overall design flow adopted for the transistor-level implementation, MTCMOS integration, sleep transistor optimization, simulation, and performance evaluation of RCA and CSLA architectures.

<img width="749" height="1079" alt="image" src="https://github.com/user-attachments/assets/db08bb80-5109-40be-9a36-f2b3eac74195" />


---

# 2. Full Adder Design

## 2.1 Gate-Level Representation of 1-bit Full Adder

Gate-level representation of the 1-bit Full Adder used as the fundamental arithmetic building block.

<img width="459" height="198" alt="image" src="https://github.com/user-attachments/assets/af731b2d-9409-4f05-9e25-dba1d6bc3ba4" />
<img width="940" height="351" alt="image" src="https://github.com/user-attachments/assets/33c1296d-ad3a-4a2b-8fe9-f9c1bbeb6678" />


## 2.2 Transistor-Level Schematic of CMOS 1-bit Full Adder

Transistor-level implementation of the 1-bit CMOS Full Adder designed using the GPDK090 technology library.

The Full Adder forms the basic building block for the higher-order RCA and CSLA architectures.

<img width="940" height="505" alt="image" src="https://github.com/user-attachments/assets/c9f56f9c-ca02-4b25-b116-b3dec4aa728c" />


## 2.3 CMOS 1-bit Full Adder – Cadence Virtuoso

Cadence Virtuoso schematic of the implemented 28T CMOS Full Adder.

<img width="1173" height="628" alt="image" src="https://github.com/user-attachments/assets/5340abce-b9fb-45bc-9608-ad66000ce95c" />
<img width="1407" height="521" alt="image" src="https://github.com/user-attachments/assets/b203c6d7-bccf-4615-b73a-8647ee3e3b85" />



# 3. Transmission-Gate Based Multiplexer

## 3.1 Gate-Level Representation of 2:1 Multiplexer

Gate-level representation of the 2:1 Multiplexer used for carry selection in the CSLA architecture.

<img width="507" height="76" alt="image" src="https://github.com/user-attachments/assets/0a60765d-aa5d-4e43-a7bc-f25f53a56aac" />
<img width="593" height="322" alt="image" src="https://github.com/user-attachments/assets/6cb16d49-bd45-415a-b137-b6db9b8df504" />


## 3.2 Transmission-Gate Based 2:1 Multiplexer

Transistor-level implementation of the Transmission-Gate-based 2:1 Multiplexer.

The transmission gate uses parallel PMOS and NMOS devices to provide efficient transmission of both logic HIGH and logic LOW levels.

<img width="822" height="584" alt="image" src="https://github.com/user-attachments/assets/3e483cfd-91bf-4c03-9a44-1cf9804a2453" />


## 3.3 2:1 Multiplexer – Cadence Virtuoso

Cadence Virtuoso schematic of the Transmission-Gate-based 2:1 Multiplexer used in the CSLA implementation.

 <img width="785" height="545" alt="image" src="https://github.com/user-attachments/assets/6198464e-ad79-4dd7-953e-66b8baace150" />
 <img width="1714" height="918" alt="image" src="https://github.com/user-attachments/assets/a8b3c325-a18e-4e61-aa82-453dc06e1690" />


---

# 4. Ripple Carry Adder (RCA)

## 4.1 Structure of 4-bit Ripple Carry Adder

Basic 4-bit RCA architecture constructed by cascading Full Adder stages.

The carry output of each stage is propagated to the next stage, resulting in a sequential carry propagation path.

<img width="790" height="279" alt="image" src="https://github.com/user-attachments/assets/33a0c4be-07cd-42cb-81bb-1fb133a233dd" />


## 4.2 4-bit RCA – Cadence Virtuoso

Transistor-level schematic of the implemented 4-bit Ripple Carry Adder.

<img width="940" height="360" alt="image" src="https://github.com/user-attachments/assets/5b60f2dc-aace-459a-a6c8-ec701f385d97" />



## 4.3 8-bit RCA – Cadence Virtuoso

Transistor-level schematic of the implemented 8-bit Ripple Carry Adder.
<img width="940" height="193" alt="image" src="https://github.com/user-attachments/assets/a0402855-364e-497d-a6d7-796069876eec" />




## 4.4 16-bit RCA – Cadence Virtuoso

Transistor-level schematic of the implemented 16-bit Ripple Carry Adder.

<img width="940" height="353" alt="image" src="https://github.com/user-attachments/assets/63bcf4d8-835e-49a8-9ea3-8a261fa7cabb" />



## 4.5 32-bit RCA – Cadence Virtuoso

Transistor-level schematic of the implemented 32-bit Ripple Carry Adder.

As the bit width increases, the carry propagation path becomes longer, resulting in increased propagation delay.

<img width="940" height="710" alt="image" src="https://github.com/user-attachments/assets/8862bba7-77f1-4b05-bce2-a42d3d75c45f" />


---

# 5. Carry Select Adder (CSLA)

## 5.1 Basic Structure of Carry Select Adder

Basic CSLA architecture illustrating parallel carry computation and carry selection.

<img width="566" height="348" alt="image" src="https://github.com/user-attachments/assets/38bd6024-90a5-4d71-be18-914835923520" />


## 5.2 Variable Block Carry Select Adder Architecture

Variable block CSLA architecture used to improve the trade-off between carry propagation delay and hardware overhead.

<img width="940" height="198" alt="image" src="https://github.com/user-attachments/assets/29a26a3c-b14c-4b03-ade6-71b9c6cc872e" />

## 5.3 4-bit CSLA – Cadence Virtuoso

Transistor-level schematic of the implemented 4-bit Carry Select Adder.

<img width="940" height="592" alt="image" src="https://github.com/user-attachments/assets/2a5acf27-c039-4bc4-b586-5965bc9fed1b" />


## 5.4 8-bit CSLA – Cadence Virtuoso

Transistor-level schematic of the implemented 8-bit Carry Select Adder.

<img width="905" height="384" alt="image" src="https://github.com/user-attachments/assets/826c4fa9-2ba3-480e-9fe9-9a146a43a121" />


## 5.5 16-bit Variable Block CSLA

The 16-bit Variable Block CSLA uses the grouping:

**2-2-3-4-5**

The variable block arrangement is used to distribute carry propagation more efficiently across the architecture.

<img width="1006" height="725" alt="image" src="https://github.com/user-attachments/assets/318cd122-f6dc-4038-9e02-3b56d6aaf3ad" />


## 5.6 32-bit Variable Block CSLA

The 32-bit Variable Block CSLA uses the grouping:

**2-2-3-4-5-6-10**

The larger variable-block arrangement is used to support 32-bit operation while maintaining a balanced delay-performance trade-off.
<img width="940" height="316" alt="image" src="https://github.com/user-attachments/assets/db30d1cf-7d08-47c1-804f-017fca95d0cf" />
<img width="940" height="299" alt="image" src="https://github.com/user-attachments/assets/b6e4dc24-45a9-4eec-838f-4d5a5e3b4045" />
<img width="940" height="386" alt="image" src="https://github.com/user-attachments/assets/37a2167f-bd03-4c89-b9c4-0862d00499bc" />
<img width="940" height="308" alt="image" src="https://github.com/user-attachments/assets/d9e4f32b-24a0-4abd-bb6e-08352f318a65" />



---

# 6. MTCMOS Power Gating

## 6.1 Basic MTCMOS Architecture with PMOS Header Sleep Transistor

Basic MTCMOS power-gating architecture using a High-Vt PMOS header sleep transistor.

The sleep transistor controls the connection between the logic block and the power supply network.

<img width="781" height="349" alt="image" src="https://github.com/user-attachments/assets/d009dfc5-64c2-422a-a22a-15e046bb4058" />


## 6.2 Active and Standby Modes of MTCMOS

Illustration of the active and standby operating modes of the MTCMOS architecture.

### Active Mode
Sleep signal = 0 → PMOS sleep transistor ON → Logic block connected to VDD.

### Standby Mode
Sleep signal = 1 → PMOS sleep transistor OFF → Logic block isolated from VDD → Standby leakage reduced.

<img width="977" height="385" alt="image" src="https://github.com/user-attachments/assets/aaaaa28c-40ce-40a8-8538-bc880760b1bc" />


## 6.3 Sleep Transistor Leakage–Delay Trade-off

Illustration of the relationship between sleep transistor width, leakage power, and propagation delay.

Increasing transistor width reduces ON resistance and delay, but excessive width can increase leakage, capacitance, and area overhead.

<img width="885" height="416" alt="image" src="https://github.com/user-attachments/assets/63392aa7-9997-4d3b-9f5e-63a54783ddf3" />


---

# 7. MTCMOS-Based RCA

## 7.1 Sleep Transistor Integrated RCA Architecture

MTCMOS-based RCA architecture incorporating a PMOS header sleep transistor between VDD and the RCA logic block.

During active mode, the sleep transistor provides the supply path to the RCA. During standby mode, it isolates the RCA from the supply to reduce leakage power.

<img width="450" height="580" alt="image" src="https://github.com/user-attachments/assets/afd50825-a759-4ea1-b75f-698e204a0b6d" />

## 7.2 MTCMOS RCA – Sleep Transistor

Cadence implementation of the High-Vt PMOS header sleep transistor used for power gating in the RCA architecture.

**Finger Width:** 2.5 µm  
**Number of Fingers:** 100  
**Effective Width:** 250 µm

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/3bce217a-3a40-4059-977e-27d827100e83" />


---

# 8. MTCMOS-Based CSLA

## 8.1 Sleep Transistor Integrated CSLA Architecture

MTCMOS-based CSLA architecture incorporating PMOS header sleep transistors for standby leakage reduction.

The sleep transistor controls the virtual VDD supplied to the parallel RCA paths and multiplexer network.

<img width="940" height="475" alt="image" src="https://github.com/user-attachments/assets/80461de5-0016-4ae3-a13a-5bc1afab2c53" />


## 8.2 MTCMOS CSLA – Sleep Transistor

Cadence implementation of the High-Vt PMOS header sleep transistor used for power gating in the CSLA architecture.

**Finger Width:** 2.5 µm  
**Number of Fingers:** 100  
**Effective Width:** 250 µm

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/973a9e60-742c-4c8f-866a-7c3fda12a2c4" />


---

# 9. Sleep Transistor Optimization

## 9.1 Sleep Transistor Width Sweep Methodology

Flowchart showing the methodology used to sweep sleep transistor width and evaluate its impact on leakage power and propagation delay.

The optimum width was selected based on the trade-off between leakage reduction and performance degradation.

<img width="940" height="1304" alt="image" src="https://github.com/user-attachments/assets/83c56dd6-0047-4b3e-8ae0-3ca3ceb04aab" />


## 9.2 Sleep Transistor Width Optimization – RCA

Variation of leakage power and propagation delay with sleep transistor width for the RCA architecture.
<img width="594" height="372" alt="image" src="https://github.com/user-attachments/assets/c6e4c0f5-7aac-42e5-a7df-95140b07f311" />
<img width="940" height="472" alt="image" src="https://github.com/user-attachments/assets/d4436aec-2e53-4a64-b242-db2f6db9ab13" />


## 9.3 Sleep Transistor Width Optimization – CSLA

Variation of leakage power and propagation delay with sleep transistor width for the CSLA architecture.

<img width="565" height="377" alt="image" src="https://github.com/user-attachments/assets/ba857efd-8c1f-42e6-856b-eee4e247e09b" />
<img width="940" height="477" alt="image" src="https://github.com/user-attachments/assets/28672ff3-bc33-44dc-89d6-592e807d7cb2" />



---

# 10. Functional Verification

## 10.1 Transient Waveform of CMOS 1-bit Full Adder

Transient simulation waveform showing the functional verification of the CMOS 1-bit Full Adder.

Different combinations of A, B, and Cin were applied to verify the Sum and Carry outputs.

<img width="940" height="391" alt="image" src="https://github.com/user-attachments/assets/3809c652-cd4c-4f16-a2da-7e3162bacb9f" />


## 10.2 Transient Waveform of 2:1 Multiplexer

Transient simulation waveform verifying the functional operation of the Transmission-Gate-based 2:1 Multiplexer.

<img width="940" height="334" alt="image" src="https://github.com/user-attachments/assets/65f7abcc-4098-4b80-84ef-b0da24f22520" />


## 10.3 Transient Waveform of 4-bit RCA

Transient simulation waveform demonstrating the functional operation of the implemented 4-bit Ripple Carry Adder.

<img width="905" height="411" alt="image" src="https://github.com/user-attachments/assets/1db36232-970c-4d28-990e-a62ca4da7a62" />


## 10.4 Transient Waveform of 8-bit RCA

Transient simulation waveform demonstrating the functional operation of the implemented 8-bit Ripple Carry Adder.

<img width="940" height="351" alt="image" src="https://github.com/user-attachments/assets/f84e6bbc-0965-4f3b-a415-09acd5447fb9" />
<img width="940" height="334" alt="image" src="https://github.com/user-attachments/assets/91d4535e-f3d9-4f85-86fb-7e93334cb946" />


## 10.5 Transient Waveform of 2-bit Conventional CSLA

Transient waveform used for functional verification of the conventional 2-bit CSLA.

<img width="940" height="286" alt="image" src="https://github.com/user-attachments/assets/a6e77b38-2994-440d-8b00-7d10d33e13a6" />



---

# 11. Performance Analysis

## 11.1 Power Consumption Comparison

Comparison of power consumption between RCA and CSLA architectures for different bit widths.

The analysis shows that power consumption increases with increasing bit width for both architectures.

<img width="904" height="491" alt="image" src="https://github.com/user-attachments/assets/822bd2d8-7b3d-47c1-a79e-0443c0074f05" />


## 11.2 Leakage and Dynamic Power Variation

Variation of leakage power and dynamic power with increasing adder bit width for RCA and CSLA architectures. 

<img width="940" height="518" alt="image" src="https://github.com/user-attachments/assets/14a8218f-a55d-4217-adc4-9c4076c195f8" />

## 11.3 Propagation Delay Variation

Variation of propagation delay with increasing bit width for RCA and CSLA architectures.

The CSLA achieves lower propagation delay through parallel carry computation.

<img width="940" height="516" alt="image" src="https://github.com/user-attachments/assets/ea2f227b-2d87-41e3-8dc0-abbcbd146cb6" />


## 11.4 Sleep Transistor Width vs Leakage and Delay – RCA

Analysis of leakage power and propagation delay as a function of sleep transistor width for the MTCMOS-based RCA.

<img width="940" height="472" alt="image" src="https://github.com/user-attachments/assets/769486dd-39a3-4bc0-971d-d96e8f83eb37" />


## 11.5 Sleep Transistor Width vs Leakage and Delay – CSLA

Analysis of leakage power and propagation delay as a function of sleep transistor width for the MTCMOS-based CSLA.

<img width="940" height="477" alt="image" src="https://github.com/user-attachments/assets/35e92914-ff18-4f99-b3bc-df307f58499e" />


## 11.6 Power Delay Product (PDP) Comparison

Variation of Power Delay Product with increasing bit width for RCA and CSLA architectures.

<img width="940" height="530" alt="image" src="https://github.com/user-attachments/assets/d64738c6-5ac5-4298-9d5d-81960daaee69" />


---

# 12. CMOS vs MTCMOS Comparison

## 12.1 Leakage Power Comparison

Comparison of leakage power between conventional CMOS and MTCMOS-based architectures.

The MTCMOS implementation demonstrates reduced standby leakage through power gating using High-Vt PMOS sleep transistors.

<img width="835" height="539" alt="image" src="https://github.com/user-attachments/assets/9b1c8513-542e-4c71-a011-7c7d44b50ed6" />


## 12.2 Propagation Delay Comparison

Comparison of propagation delay between conventional CMOS and MTCMOS-based architectures to evaluate the performance overhead introduced by power gating.

<img width="940" height="599" alt="image" src="https://github.com/user-attachments/assets/22771a75-2998-4e65-b858-30afb21fe7ba" />


---

# 13. Additional Simulation and Testbench Images

## 13.1 Spectre Simulation Workflow

Simulation workflow showing the interaction between the Spectre netlist and vector stimulus files used for circuit simulation.

<img width="940" height="446" alt="image" src="https://github.com/user-attachments/assets/d81d3d53-c0de-402b-b182-ee9e62a87969" />


## 13.2 Cadence ADE-L Setup

Cadence ADE-L simulation setup used for the 1-bit Full Adder.

<img width="889" height="526" alt="image" src="https://github.com/user-attachments/assets/01728b35-4dec-4ec0-b807-5b15106d9a7d" />
<img width="940" height="498" alt="image" src="https://github.com/user-attachments/assets/6074cff5-304b-4ad8-9fec-95b176b5af98" />


---

# 14. MTCMOS Operational Verification

## 14.1 Active Mode Operation

Verification of the MTCMOS-based CSLA during active operation with the sleep transistor enabled.

<img width="940" height="404" alt="image" src="https://github.com/user-attachments/assets/b3b4c970-ae5b-4f4b-b4d9-d5f951f67660" />


## 14.2 Standby Mode Verification – Sleep = 0

Simulation waveform corresponding to the MTCMOS standby/operational verification condition with Sleep = 0.

<img width="940" height="357" alt="image" src="https://github.com/user-attachments/assets/222419f0-afbd-4d2a-816e-39500c9400bf" />


## 14.3 Standby Mode Verification – Sleep = 1

Simulation waveform corresponding to the MTCMOS standby verification condition with Sleep = 1.

<img width="940" height="364" alt="image" src="https://github.com/user-attachments/assets/2dd5e0aa-6d57-46e3-95e2-8ff977fc1cc3" />


---

# 15. Project Summary

The implemented transistor-level architectures demonstrate the trade-offs between power, propagation delay, leakage power, and hardware complexity in RCA and CSLA designs. MTCMOS-based power gating using High-Vt PMOS header sleep transistors provides effective standby leakage reduction, while sleep transistor sizing enables a balanced trade-off between leakage reduction and delay overhead.

The final design methodology combines architectural optimization with transistor-level leakage reduction for low-power VLSI arithmetic circuit design in 90 nm CMOS.

---

## Project Information

**Project:** Design and Performance Analysis of MTCMOS-Based RCA and Variable Block CSLA Architectures in 90 nm CMOS

**Degree:** M.Tech – VLSI Design

**Institution:** Gaya College of Engineering, Gaya

**Supervisor:** Dr. Mrinal Ranjan

**Co-Supervisor:** Dr. Rajan Sarkar

**Technology:** 90 nm CMOS

**Design Tool:** Cadence Virtuoso

**Simulator:** Cadence Spectre

**Technology Library:** GPDK090
