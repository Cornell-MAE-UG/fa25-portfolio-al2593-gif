---
title: Macadamia Nutcracker Design
layout: project
description: Lever and beam design for an actuator powered macadamia nutcracker
image: /assets/images/nutcracker_actuator_beam_design.svg
---

## Problem Statement

The objective of this design is to create a simple lever based nutcracker capable of cracking a macadamia nut. The original design used human grip strength as the input force. This updated design replaces the hand input with a linear actuator, then checks whether the nutcracker handles can be treated as elastic beams without excessive deflection.

The required cracking force is assumed to be:

\[
F_o = 222.18 \text{ N}
\]

The nut is modeled as being located 4 cm from the pivot. The handle is modeled as a cantilever beam fixed at the pivot, with transverse loads from the nut and actuator.

---

## Linear Actuator Selection

A compact actuator is preferred because the required force is not extremely large. I selected a Progressive Automations PA-01 style mini linear actuator with:

- Stroke: 1 in = 25.4 mm
- Rated force: 16 lb
- Actuator force:

\[
F_i = 16(4.448) = 71.17 \text{ N}
\]

The lever relationship is:

\[
F_iL_c = F_oL_n
\]

Solving for the actuator connection distance from the pivot:

\[
L_c = \frac{F_oL_n}{F_i}
\]

\[
L_c = \frac{(222.18)(0.04)}{71.17}
\]

\[
L_c = 0.125 \text{ m} = 12.5 \text{ cm}
\]

Therefore, the actuator should connect approximately 12.5 cm from the pivot. This gives a mechanical advantage of:

\[
MA = \frac{L_c}{L_n} = \frac{12.5}{4} = 3.125
\]

The resulting output force is:

\[
F_o = (71.17)(3.125) = 222.4 \text{ N}
\]

This is slightly above the required cracking force, so the actuator has enough force capacity.

---

## Beam Model and Assumptions

The nutcracker handle is no longer treated as rigid. Instead, each handle is modeled as a cantilever beam fixed at the pivot.

Assumptions:

- The handle is straight and prismatic.
- The pivot behaves like a fixed support for beam deflection analysis.
- Only transverse force components are considered.
- The actuator load is applied at the end of the handle, 12.5 cm from the pivot.
- The nut load is applied 4 cm from the pivot.
- The handle material is 6061-T6 aluminum.
- The beam has a rectangular cross section.
- Deflection must be less than 2 percent of handle length.

The maximum elastic deflection occurs at the free end of the handle because that point is farthest from the pivot and receives the largest displacement from bending.

The allowable deflection is:

\[
\delta_{allow} = 0.02L = 0.02(0.125) = 0.00250 \text{ m}
\]

or:

\[
\delta_{allow} = 2.50 \text{ mm}
\]

---

## Deflection Analysis

For a cantilever beam with an end load:

\[
\delta_{end} = \frac{FL^3}{3EI}
\]

For a point load applied at distance \(a\) from the fixed end, the deflection at the free end is:

\[
\delta_{point} = \frac{Pa^2(3L-a)}{6EI}
\]

Using a conservative estimate where both loads contribute to downward deflection:

\[
\delta_{max} = \frac{F_iL^3}{3EI} + \frac{F_oa^2(3L-a)}{6EI}
\]

where:

\[
F_i = 71.17 \text{ N}
\]

\[
F_o = 222.18 \text{ N}
\]

\[
L = 0.125 \text{ m}
\]

\[
a = 0.040 \text{ m}
\]

\[
E = 69 \text{ GPa}
\]

Solving for the minimum required second moment of area:

\[
I_{req} = 3.84 \times 10^{-10} \text{ m}^4
\]

---

## Cross Section Selection

For a rectangular beam:

\[
I = \frac{bh^3}{12}
\]

A mass efficient rectangular cross section should place more material vertically, because bending stiffness scales with \(h^3\). A thin flat strip would be much worse. Basically, geometry is doing the heavy lifting here, not vibes.

Selected cross section:

\[
b = 10 \text{ mm}
\]

\[
h = 8 \text{ mm}
\]

\[
I = \frac{(0.010)(0.008)^3}{12}
\]

\[
I = 4.27 \times 10^{-10} \text{ m}^4
\]

Since:

\[
4.27 \times 10^{-10} > 3.84 \times 10^{-10}
\]

this cross section satisfies the deflection requirement.

The predicted maximum deflection is:

\[
\delta_{max} = 0.00225 \text{ m} = 2.25 \text{ mm}
\]

The percent deflection is:

\[
\frac{2.25}{125}(100) = 1.80\%
\]

This is below the 2 percent limit.

---

## Strength Check

The conservative maximum bending moment at the pivot is:

\[
M_{max} = F_iL + F_oa
\]

\[
M_{max} = (71.17)(0.125) + (222.18)(0.040)
\]

\[
M_{max} = 17.78 \text{ N}\cdot\text{m}
\]

The maximum bending stress is:

\[
\sigma = \frac{Mc}{I}
\]

where:

\[
c = \frac{h}{2} = 0.004 \text{ m}
\]

\[
\sigma = \frac{(17.78)(0.004)}{4.27 \times 10^{-10}}
\]

\[
\sigma = 166.7 \text{ MPa}
\]

6061-T6 aluminum has a yield strength of about 276 MPa, so the factor of safety is:

\[
FS = \frac{276}{166.7} = 1.66
\]

This is acceptable for a classroom prototype and keeps the handle lightweight.

---

## Final Design

Final design dimensions:

- Nut distance from pivot: 4.0 cm
- Actuator connection distance from pivot: 12.5 cm
- Handle length: 12.5 cm minimum, with extra length optional for mounting hardware
- Actuator: 1 inch stroke, 16 lb rated force
- Beam material: 6061-T6 aluminum
- Beam cross section: 10 mm wide by 8 mm tall rectangular bar
- Predicted maximum deflection: 2.25 mm
- Percent deflection: 1.80 percent of handle length
- Factor of safety against yielding: 1.66

This design is feasible because the actuator supplies enough force through the lever arm, while the aluminum handle remains below the required 2 percent elastic deflection limit.

---

## Final Design Drawing

![Actuator powered nutcracker beam design]({{ site.baseurl }}/assets/images/nutcracker_actuator_beam_design.svg)

---

## Conclusion

The updated actuator powered nutcracker uses a 16 lb linear actuator connected 12.5 cm from the pivot to generate the required 222.18 N cracking force at a nut located 4 cm from the pivot. Treating the handle as an elastic beam shows that a 6061-T6 aluminum rectangular cross section of 10 mm by 8 mm keeps the maximum vertical deflection to approximately 2.25 mm, or 1.80 percent of the handle length. The design also has a bending factor of safety of about 1.66, making it realistic for a simple prototype.

Technologies Used: Statics, Mechanics of Solids, Beam Deflection, Linear Actuator Selection, Mechanical Design
