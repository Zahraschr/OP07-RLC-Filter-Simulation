# OP07 RLC Filter Circuit – Step & Impulse Response Analysis

This project analyzes, simulates, and implements an RLC-based active filter using the OP07 operational amplifier. The circuit is designed to achieve a cutoff frequency near 20 kHz using an inductor-capacitor network and a precision low-offset OP07 input stage.

## Features
- RLC filter design for selective frequency attenuation
- OP07 op-amp with low offset and high stability
- Theoretical analysis using Thevenin equivalent and differential equations
- MATLAB simulation of step and impulse responses
- Frequency sweep simulation in SPICE
- Physical circuit implementation on breadboard
- Oscilloscope measurement and waveform comparison

## Component Values
| Component | Value |
|----------|--------|
| R1       | 10 kΩ  |
| R2       | 200 kΩ |
| R3       | 10 kΩ  |
| C        | 0.1 µF |
| L        | 159 µH |

## MATLAB Example Code (Step Response)
```matlab
clc; clear;
t = 0:1:100;
f = exp(-40829*t).*sin(25000*t)/25000 - exp(-21984*t).*cos(25000*t);
plot(t, f);
title('Step Response');
xlabel('Time');
ylabel('Amplitude');
