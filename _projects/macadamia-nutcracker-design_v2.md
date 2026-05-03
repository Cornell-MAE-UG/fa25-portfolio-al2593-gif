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

*Force Analysis:*

Required nut force:

Fnut = 1110 N

Input force:

Finput = Fnut / MA = 1110 / 12.5 ≈ 89 N

*Beam Model:*

Each handle:
Fixed at pivot
Load applied at free end
Acts as a cantilever beam

Maximum deflection occurs at the free end.

*Deflection Equation:*

δ = FL^3/3EI

*Cross-Section Selection:*

I = bh^3/12

Trial dimensions:

b=0.02m
h=0.01m

I ≈ 1.67 × 10⁻⁹ m⁴

*Deflection Calculation:*

δ = (89 × 0.25³) / (3 × 70×10⁹ × 1.67×10⁻⁹) = 0.004 m 

Therefore design satisfies constraint.

*Mass Efficiency Insight:*

I scales with h³
Increasing height is far more effective than width

Conclusion:
A tall, narrow beam is most efficient

*Linear Actuator Selection:*

Requirements:

Minimum force ≈ 89 N
With safety factor → ≥ 200 N
Stroke ≈ 50 mm

Selected actuator:

Force capacity ≈ 220 N
Stroke ≈ 50 mm
12V system

*Final Design:*
Mechanical advantage: 12.5
Actuator replaces hand force
Aluminum beam handles
Cross-section: 20 mm × 10 mm
Max deflection: 4 mm

System behavior:

Actuator applies force
Lever amplifies force
Nut is cracked
Handles remain within elastic limits












