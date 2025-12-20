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

The system operates as a steady-flow control volume with continuous mass flow of refrigerant.

## System Diagram and Energy Interactions

The air conditioner is modeled as a control volume with the following interactions:

- **Work input** at the compressor
- **Heat absorption** in the evaporator
- **Heat rejection** in the condenser
- **Negligible kinetic and potential energy changes**

Mass flow is constant throughout the cycle under steady operating conditions.

## Governing Equations

### Mass Balance
For steady operation:
\[
\sum \dot{m}_{in} = \sum \dot{m}_{out}
\]

### Energy Balance
Applied to each component:
\[
\dot{Q} - \dot{W} = \dot{m}(h_{out} - h_{in})
\]

### Entropy Balance
For each component:
\[
\dot{S}_{gen} = \dot{m}(s_{out} - s_{in}) - \sum \frac{\dot{Q}}{T}
\]

Entropy generation accounts for irreversibilities such as friction, non-ideal compression, and finite temperature heat transfer.

## Performance Metrics

The primary measure of system performance is the **Coefficient of Performance (COP)**:
\[
COP = \frac{\dot{Q}_{evap}}{\dot{W}_{comp}}
\]

A higher COP indicates more effective cooling per unit of work input.

## Effect of Operating Condition Changes

One important operating condition is **outdoor air temperature**. As outdoor temperature increases:

- Condenser pressure rises
- Compressor work increases
- COP decreases
- Entropy generation increases

This explains why air conditioners perform worse during extremely hot days.

## Design Modification Analysis

Improving condenser heat transfer, such as by increasing surface area or airflow, reduces condenser pressure. This lowers compressor work and improves overall COP. While this increases system size or cost, it results in higher efficiency and improved performance under high thermal loads.

## Conclusion

The vapor-compression air conditioning system demonstrates how thermodynamic principles directly influence real engineering performance. Changes in operating conditions and component design significantly affect efficiency, energy consumption, and irreversibility generation. Understanding these tradeoffs is essential for designing and evaluating practical thermal systems.

