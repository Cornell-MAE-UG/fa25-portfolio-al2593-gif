---
title: Macadamia Nutcracker Design
layout: project
description: Lever and beam design for an actuator powered macadamia nutcracker
image: /assets/images/nutcracker_actuator_beam_design.svg
---

## Given

Macadamia nut cracking force:
F_nut ≈ 250 lbf ≈ 1110 N

Nutcracker geometry:
Handle length: L = 0.25 m
Distance from pivot to nut: d = 0.02 m

Mechanical advantage:
MA = L / d = 12.5

Handles are no longer rigid → modeled as cantilever beams

Material assumption:
Aluminum, E = 70 GPa

Deflection constraint:
δ_max ≤ 2% of length = 0.005 m

Only transverse forces considered for beam bending

---

## Find

a) Location of maximum elastic deflection in the handles

b) Beam design (cross-section and material) such that:

Deflection ≤ 2% of length
Mass-efficient

c) Final system design using a linear actuator instead of hand force

---

## Approach

Use lever mechanics to determine required input force
Model each handle as a cantilever beam with end load
Use beam deflection equation to size cross-section
Choose geometry that maximizes stiffness per mass
Select a linear actuator based on force and stroke requirements

---

## Solution

1. Force Analysis

Required nut force:

Fnut = 1110 N

Input force:

Finput = Fnut / MA = 1110 / 12.5 ≈ 89 N

2. Beam Model

Each handle:

Fixed at pivot
Load applied at free end
Acts as a cantilever beam

Maximum deflection occurs at the free end.

3. Deflection Equation

δ = FL^3/3EI

4. Cross-Section Selection

I = bh^3/12

Trial dimensions:

b=0.02m
h=0.01m

I = 1.67 × 10^−9 m4

5. Deflection Calculation



















