# PCB Design for Desktop Lighting Lamp

## Introduction
PCB Design is a crucial skill for electrical engineers, necessary for executing practical projects. This project focuses on designing a PCB for a desktop lighting lamp, emphasizing the essential considerations in the PCB design process. Additionally, the project addresses cost estimation, highlighting factors that influence manufacturing costs, such as board size, layer count, and components. Understanding these factors empowers informed decision-making regarding design trade-offs, ensuring both functionality and cost-effectiveness.

## Objectives
In this project, you will utilize **KiCad** to design a PCB for a desktop lighting lamp. The schematic of the circuit is presented in **Figure 1**.

![Schematic diagram for the desktop lighting lamp 1 (1)-1](https://github.com/user-attachments/assets/7352d64d-0e5a-413b-8a51-51c567da62e3)
Figure 1: Schematic of circuit

### Circuit Details
The circuit includes the **A6211** IC along with passive elements. It features three inputs: the input voltage, ground (GND), and LED dimming. Brightness control of the LED is achieved through a PWM signal by varying the duty cycle. The specifications of the circuit are summarized in **Table 1**.

#### Specifications
| Parameter          | Value         |
|--------------------|---------------|
| Input Voltage      | 6V – 48V     |
| Output Voltage     | -             |
| Output Current     | 2A           |
| Switching Frequency | 1 MHz        |

**Table 1: Specifications of the circuit**

### Components
The elements in the circuit are listed in **Table 2**. Some components may not be available in KiCad libraries, requiring you to create your own library for adding schematics and footprints. For standard packages, refer to the datasheets for suitable footprints.

#### Component List
| Reference | Description                          | Part Number           | Notes                                                     |
|-----------|--------------------------------------|-----------------------|-----------------------------------------------------------|
| C1        | CAP 47 μF, 50 V, ELECT MZA SMD      | 565-2568-1-ND         | VIN filter electrolytic cap (exactly value not critical) |
| C2        | CAP CER 4.7 μF, 50 V, X5R 1206      | 587-1962-1-ND         | VIN filter ceramic cap                                    |
| C3        | 0.1 μF, 10 V, X7R, ceramic          | 399-1095-1-ND         | Noise reduction                                           |
| C4        | 0.047 μF, 50 V, X7R 0603            | 445-5095-1-ND         | BOOT cap                                                 |
| C5        | 0.1 μF, 10 V, X7R ceramic           | 399-1095-1-ND         | VCC filter cap                                           |
| C6        | 10 nF, 50 V, X7R                     | 490-1511-1-ND         | Optional input cap for EN (can be used for 10 kΩ pulldown resistor instead) |
| C7        | 2.2 μF, 50 V, X5R                    | 587-2402-1-ND         | Optional filter cap across LED string. Try 0.47 μF to 4.7 μF |
| D1        | B560C-13-F DIODE SCHOTTKY 5 A, 60 V  | B560C-FDICT-ND        | For LED current up to 3 A                                 |
| L1        | NR8040T100M (10 μH, 3.4 A, 20%)      | 587-2001-1-ND         | 8 mm inductor                                            |
| J1        | Pin Header, 3-Pin                    |                       |                                                          |
| J2        | Pin Header, 2-Pin                    |                       |                                                          |
| R1        | 63.4 kΩ, 0.1 W, 1%                   | P63.4KHDKR-ND         | RON = 63.4 kΩ gives fSW = 1 MHz                         |
| R2        | 0.1 Ω, 0.5 W, 1%                     | CRM1206-FX-R100ELF    |                                                          |
| U1        | A6211/A6213                          |                       |                                                          |

**Table 2: List of elements**

## Goals
The goals of this project include:
- Implementing routing techniques and adhering to established rules for drawing tracks to ensure proper signal integrity and minimize interference.
- Finding appropriate schematics and footprints for all components or designing a custom library if necessary for accurate representation and compatibility.
- Developing a well-organized floor plan for component placement on the board.
- Achieving efficient space utilization, creating a compact and appropriately sized PCB layout without unnecessary layers.
- Optimizing the design for cost by carefully selecting components and boards, considering their cost-effectiveness, availability, and suitability for the application.

## Repository Structure
The repository contains three folders:
- **3d-view-diagram**: Includes the 3D view of the PCB for the desktop lighting lamp.
- **pcb-sketch**: Contains the PCB sketch of the desktop lighting lamp.
- **schematic-diagram**: Includes the schematic diagram for the desktop lighting lamp.

## Conclusion
By completing this project, we gain valuable skills in PCB design, cost estimation, and the critical considerations necessary for electrical engineering projects. The knowledge acquired enable me to make informed decisions that enhance the functionality and cost-effectiveness of my designs.

