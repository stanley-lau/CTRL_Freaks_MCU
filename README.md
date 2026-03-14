# Team CTRL Freaks - PSAT MCU V2 PCB

## Overview
This repository contains the design for the Microcontroller Unit (MCU) V2 PCB developed by Team CTRL Freaks.

The MCU PCB is the main controller for the on-board flight computer, interfacing with all payload components, including the **PSU PCB**, **Beacon PCB**, and the **Nichrome wire plume mechanism** in the PSAT mission.

Built around the **MSP430 microcontroller**, the board integrates sensors, operational amplifiers, and protective sensing circuitry to control and monitor the plume mechanism.

## Features

- **MSP430 Microcontroller Core** for low-power, high-reliability embedded control  
- **Sensor Integration**  
  - Interfaces with barometric, IMU, and other payload sensors  
- **Operational Amplifiers**  
  - For signal conditioning and amplification of analog sensor signals
- **Protective Sensing Circuitry**  
  - Monitors critical parameters (temperature, current) to protect the plume mechanism  
- **CTRL Freaks PSU PCB Interface**  
  - Conencts to the CTRL Freaks PSU PCB to power the Nichrome wire for plume mechanism with additional safety measures
- **Beacon PCB Interface**  
  - Connects to an external Beacon PCB allowing for GPS collection and transmission over LoRa  

## Technical Overview

| Function                  | Description |
|---------------------------|-------------|
| Microcontroller           | MSP430 - main control and processing unit |
| Sensor interfaces         | Integrated connections for BMP and IMU sensors |
| Signal conditioning       | Operational amplifiers for accurate analog readings |
| Protective sensing        | Current and temperature monitoring circuitry for plume safety |
| PSU PCB Interface         | Compatible with CTRL Freaks PSU PCB for Nichrome wire high-current draw|
| Beacon PCB Interface      | Compatible with beacon PCB to transmit GPS over LoRa |



## Usage

1. Connect the PCB to the **PSU board** for regulated power supply.  
2. Attach the Nichrome Wire (plume mechanism) as per design schematics.  
3. Attach the thermistors as per design schematics.
3. Program the MSP430 firmware via CCS using a Spy-Bi-Wire (SBW) adapter. 
4. Verify sensor readings and protective circuits before operation.  