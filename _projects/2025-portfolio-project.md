---
layout: project
title: Residential Vapor-Compression Air Conditioning System
description: Thermodynamic performance analysis of a common residential cooling system
image: /assets/images/ac-condenser.jpg
---

## Overview

A residential air conditioning (AC) system is a closed-loop system designed to take heat from an indoor space and move it to an outdoor space. It operates continuously with steady-state conditions and is commonly modeled as a control volume (CV) having steady mass flow. The system relies on phase changes, pressure differences, and inputting mechanical work to transfer heat from cold to hot, against the natural direction.

## System Description

A standard residential air conditioning system consists of four main components:

- **Evaporator**: Absorbing heat from indoor air as the refrigerant (working liquid) evaporates
- **Compressor**: Raising the pressure and temperature of the refrigerant vapor with the mechanical work
- **Condenser**: Rejecting heat to the outdoor environment as the working liquid condenses
- **Expansion Valve**: Reducing the refrigerant pressure, preparing it for the next cycle, ending back where we started

The system operates as a steady-flow control volume with continuous mass flow of the working liquid.

<img src="{{ "/assets/images/schematic.jpg" | relative_url }}" alt="System diagram" width="500">

## System Diagrams and Energy Interactions

The air conditioner is modeled as a control volume with the following interactions:

- **Work input** at the compressor
- **Heat absorption** in the evaporator
- **Heat rejection** in the condenser
- **Negligible kinetic and potential energy changes**

<img src="{{ "/assets/images/system-diagram.jpg" | relative_url }}" alt="System diagram" width="500">

Mass flow is constant throughout the cycle under steady operating conditions.

## Governing Equations

### Mass Balance
For steady operation:
ṁ_in = ṁ_out = ṁ

### Energy Balance
Applied to each component:
Q̇ − Ẇ + ṁ h_in − ṁ h_out = 0

Applied to individual components: 
Compressor:
Ẇ_comp = ṁ (h₂ − h₁)

Evaporator:
Q̇_evap = ṁ (h₁ − h₄)

Condenser: 
Q̇_cond = ṁ (h₂ − h₃)

### Entropy Balance
For each component:
Ṡ_gen = ṁ (s_out − s_in) − Q̇ / T

Entropy generation accounts for irreversibilities such as friction, non-ideal compression, and finite temperature heat transfer.

For all real processes: 
Ṡ_gen ≥ 0

## Performance Metrics

The primary measure of system performance is the **Coefficient of Performance (COP)**:
COP = Q̇_evap / Ẇ_comp

A higher COP indicates more effective cooling per unit of work done.

## Effect of Operating Condition Changes

One important operating condition is **outdoor air temperature**. As outdoor temperature increases:

- Condenser pressure rises
- Compressor work increases
- COP decreases
- Entropy generation increases

This explains why air conditioners perform worse during very hot days.

## Design Modification Analysis

Improving condenser heat transfer, such as by increasing surface area or airflow, reduces condenser pressure. This lowers compressor work and improves overall COP. While this increases system size, complexity, and cost (both in construction and maintenance), it results in higher efficiency and improved performance under high thermal loads.

## Conclusion

The vapor-compression air conditioning system demonstrates how thermodynamic principles directly influence real engineering performance and how they have a direct effect on everyday lives. Changes in operating conditions and component design significantly affect efficiency, energy consumption, and entropy generation. Understanding these tradeoffs is crucial for designing and evaluating practical systems that impact millions.

