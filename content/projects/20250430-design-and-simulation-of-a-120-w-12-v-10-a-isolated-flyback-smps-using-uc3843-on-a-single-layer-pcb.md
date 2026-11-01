---
title: Design and Simulation of a 120 W (12 V, 10 A) Isolated Flyback SMPS Using UC3843 on a Single-Layer PCB
date: 2025-04-30
pinned: false
category: Academic Project
custom_category: ''
research_interests:
  - PCB design
image: /assets/images/pasted-image-1793516214670.png
issuer: Power Electronics
issuer_label: Part of
gallery:
  - /assets/images/pasted-image-1793516258271.svg
  - /assets/images/pasted-image-1793516268888.svg
  - /assets/images/pasted-image-1793516280946.svg
  - /assets/images/pasted-image-1793516288392.svg
description: I designed a 120 W offline flyback power supply that converts 220 V AC mains to an isolated 12 V, 10 A DC output using KiCad software.
youtube: ''
link: ''
pdf_file: ''
pdf_title: ''
---

## Overview and specifications

The supply delivers 12.0 V at 10 A (120 W) from 220 V AC, with full galvanic isolation between mains and output. Values marked _simulated_ come from my ngspice run; _estimate_ values are design targets not yet measured on hardware.

### Input

| Parameter | Value | Basis |
| --- | --- | --- |
| Input voltage | 220 V AC nominal | Design / simulated |
| Input range | \~180–265 V AC | Design target |
| Line frequency | 50 Hz | Design |
| Rectified DC bus | \~310 V DC (281 V min at 10 A) | Simulated |
| Input power at full load | \~140 W | Estimate (\~85% efficiency) |
| Input current | \~1.1–1.3 A rms | Estimate |
| Fuse | T2.5 A 250 V slow-blow (F1) | Design |
| Inrush limiting | NTC 5 Ω, 5D-11 (RT1) | Design |
| Surge protection | MOV 14D471K (VR1) | Design |
| EMI filter | X2 220 nF + common-mode choke + Y1 2.2 nF | Design |

### Output

| Parameter | Value | Basis |
| --- | --- | --- |
| Output voltage | 12.02 V DC | Simulated |
| Output current | 10 A max | Design |
| Output power | 120 W | Design |
| Ripple at 10 A | 167 mV p-p (\~1.4%) | Simulated |
| Load regulation, 10 A → 1 A | < 0.1% | Simulated |
| Start-up overshoot | 13.3 V peak | Simulated |
| Output adjustment | ±\~0.5 V via RV1 trimpot | Design |
| Output capacitance | 3 × 2200 µF 25 V low-ESR | Design |

### Converter

| Parameter | Value |
| --- | --- |
| Topology | Isolated flyback, peak current-mode control |
| Controller | UC3843 |
| Switching frequency | 65 kHz (R8 12 kΩ, C5 2.2 nF) |
| Power MOSFET | SPP11N80C3, 800 V |
| MOSFET Vds peak | 512 V, 64% of rating (simulated) |
| Primary current limit | \~3 A peak (1 V / 0.33 Ω) |
| Transformer | ETD39, Lp 1.3 mH, 84 : 11 : 13 turns (pri : sec : aux) |
| Output rectifier | MBR30100PT dual Schottky, 30 A 100 V |
| Feedback | TL431 reference + PC817 opto-coupler |
| UC3843 VCC minimum | 8.97 V vs 7.6 V UVLO-off (simulated) |

### Isolation and PCB

| Parameter | Value |
| --- | --- |
| Primary–secondary clearance | 4.0 mm |
| Primary–secondary creepage | 6.4 mm, with routed slot |
| PCB | Single layer, 2 oz copper, 190 × 105 mm |
| High-current traces | Sized to IPC-2221 for 10 A |

## Architecture: four PCB zones

[embed: node/c6cfc85d-117b]

Zones A and B carry mains-referenced high voltage; Zone D is the safe low-voltage side. Only the transformer and opto-coupler cross Zone C, so no copper connects primary and secondary.

## Work done

I took the design from calculation through block tests, full-circuit simulation and PCB layout.

### 1. Design calculations

- Sized the flyback transformer for 120 W at 65 kHz: primary inductance 1.3 mH, turns 84 : 11 : 13, on an ETD39 core.
- Selected an 800 V MOSFET so the reflected voltage plus leakage spike stays well below rating.
- Set the current-sense resistor (0.33 Ω) for a \~3 A primary peak limit and sized the RCD clamp (4.7 nF, 10 kΩ 10 W, UF4007).
- Chose the feedback divider (10 k / 2.2 k + 1 k trim) to set 12.0 V with the TL431's 2.495 V reference.
- Sized traces and isolation distances to IPC-2221 and the 4 mm / 6.4 mm safety targets.

### 2. Block-wise testing in Proteus

I tested each functional block in Proteus 8 Professional before joining them. _Fill in your measured result for each block._

| Block | What I tested | Result |
| --- | --- | --- |
| Rectifier + bulk capacitor | 220 V AC in, DC bus level and ripple | [fill] |
| UC3843 oscillator + PWM | 65 kHz clock, gate pulse, current-limit cutoff | [fill] |
| MOSFET + RCD clamp | Drain waveform and clamp voltage | [fill] |
| Output rectifier + filter | DC output level and ripple | [fill] |
| TL431 + PC817 feedback | Response of COMP to output change | [fill] |

### 3. Full-schematic simulation in ngspice

I exported the KiCad netlist and built a complete ngspice deck from it, keeping every connection and component value from the schematic. Behavioral models represent the UC3843, TL431 and PC817; the transformer is three coupled inductors (k = 0.995). The run covers 30 ms with a load step from 10 A to 1 A at 20 ms.

| Measurement | Result |
| --- | --- |
| Output at 10 A | 12.02 V |
| Ripple at 10 A | 167 mV p-p |
| Output at 1 A | 12.02 V |
| Start-up peak | 13.3 V |
| MOSFET Vds peak | 512 V |
| Bulk capacitor minimum | 281 V |
| UC3843 VCC minimum | 8.97 V |

I also built a KiCad Simulator version of the schematic, so waveforms can be probed directly on the drawing.

### 4. PCB design in KiCad 10

- Drew the full schematic and passed ERC.
- Placed parts in four zones, left to right: AC input, primary switching, isolation barrier, secondary output.
- Routed a single-layer board (190 × 105 mm, 2 oz copper) with wide copper for the 10 A output path.
- Wrote custom design rules: 4 mm primary–secondary clearance, 6.4 mm creepage, 1.5 mm spacing on high-voltage tracks.
- Added an isolation slot under the transformer and opto-coupler, heatsinks for Q1 and D4, and M3 mounting holes.
- Passed DRC and generated Gerber files for fabrication.

## Results and next steps

Simulation confirms the design regulates 12.0 V from no-load to 10 A with safe MOSFET stress and stable controller supply. Three items remain before the board is mains-ready:

1. Add soft-start (a diode and \~2.2 µF capacitor on COMP) to cut the 13.3 V start-up overshoot to below 12.6 V.
2. Build and wind the ETD39 transformer, then measure efficiency, temperature rise and line regulation over 180–265 V AC.
3. Have the board reviewed and tested with an isolation transformer before any direct connection to 220 V mains.
