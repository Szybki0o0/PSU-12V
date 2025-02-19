# Dual Power Supply Circuit

## Overview
This schematic represents a **dual power supply circuit** that converts **12V AC** input into **regulated ±12V DC output**. It uses **linear voltage regulators (7812 and 7912)** to provide stable positive and negative 12V outputs.

![image](https://github.com/user-attachments/assets/cb0e4a89-64ae-46c4-be5b-2c74fb865e48)

## Main Components
1. **Power Input:**
   - **J1 (Barrel Jack Connector)**: Accepts **12V AC** input.
   - **D1, D2 (1N4007 Diodes)**: Forms a **bridge rectifier** for AC-to-DC conversion.

2. **Filtering Section:**
   - **C1, C2, C3, C4, C5, C6 (4700µF capacitors)**: Large **electrolytic capacitors** used for smoothing rectified DC voltage.
   - **C7, C8, C9, C10 (1µF capacitors)**: Additional filtering for improved stability.

3. **Voltage Regulators:**
   - **U1 (7812 Voltage Regulator)**: Provides a regulated **+12V DC output**.
   - **U2 (7912 Voltage Regulator)**: Provides a regulated **-12V DC output**.

4. **Protection Components:**
   - **D3 (1N4007 Diode)**: Protection diode to prevent reverse polarity damage.

## How It Works
1. **AC to DC Conversion**  
   - The **12V AC input** is rectified using **D1 and D2**, converting AC voltage to **pulsating DC**.
   - The **large electrolytic capacitors (C1-C6)** smooth the voltage to **reduce ripple**.

2. **Voltage Regulation**  
   - The **7812 regulator (U1)** outputs a steady **+12V DC**.
   - The **7912 regulator (U2)** outputs a steady **-12V DC**.
   - Small capacitors (C7-C10) help improve transient response and further reduce noise.

3. **Output**  
   - The final output at the **VoltageOut** terminal provides **+12V, GND, and -12V**, suitable for powering **operational amplifiers, audio circuits, and other dual-supply electronics**.

## Psysical implementation
Project has't been implemented on PCB but tested on a breadboard.

![image](https://github.com/user-attachments/assets/de4b62d5-953b-42f1-acee-1222a9dff5d4)

## Possible Improvements
- Adding **heat sinks** to the **7812 and 7912** for better thermal management. (It's mandatory)
- Using **fast-recovery diodes (e.g., UF4007)** instead of **1N4007** to improve efficiency.
- Implementing a **fuse** at the input for added protection.

## Applications
- **Operational amplifier circuits**
- **Audio amplifier power supplies**
- **Analog signal processing systems**
- **Dual-rail power supply requirements**

## Author
Jakub Konior

