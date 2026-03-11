---
title: Macadamia Nutcracker Design
layout: project
description: Lever design for cracking a macadamia nut using human grip force
image: /assets/images/Macadamia_Nut.jpg
---

## Problem Statement

The objective is to design a simple lever based nutcracker capable of cracking a macadamia nut using human grip strength.

Macadamia nuts require approximately **222.18 N** of force to crack. The goal of the design is to determine appropriate nutcracker dimensions so that a user can generate this force comfortably using hand grip.

---

## Given

Required cracking force:

Fo = 222.18 N

Average human grip strength:

Fi ≈ 40 kg ≈ 392 N

Nut diameter:

2 cm

Nutcracker modeled as a **simple lever mechanism**

---

## Find

Determine the required dimensions of the nutcracker such that the output force at the nut is sufficient to crack the shell.

---

## Approach

The nutcracker can be modeled as a lever system. Using moment equilibrium:

∑M = 0

For a lever:

Fo / Fi = Lc / Ln

Where

Fo = output force at nut  
Fi = input grip force  
Lc = handle length  
Ln = distance from pivot to nut  

Mechanical advantage required:

Fo / Fi = 222.18 / 40 = 5.55

Assuming the nut contact point is:

Ln = 2 cm

Then the required handle length becomes:

Lc = (5.55)(2)

Lc = 11.11 cm

For improved ergonomics we assume:

Ln = 4 cm

Then

Lc = (5.55)(4)

Lc = 22.22 cm

---

## Nutcracker Design Diagram

<img src="{{ "/assets/images/Macademia_Nutcracker_Design.jpg" | relative_url }}" alt="System diagram" width="400">

## Usability Discussion

The calculated lever length produces a relatively large nutcracker.

A handle length of approximately **22 cm** may make the device bulky and could stretch the user's hand during operation.

However, the increased lever length significantly reduces the grip force required to crack the nut, making the device effective for typical users.

Possible usability improvements include:

- ergonomic grip surfaces  
- curved handles  
- improved pivot positioning  

---

## Linear Actuator Design

Instead of relying on grip strength, the nutcracker can be modified to use a linear actuator.

Chosen actuator:

Force output = 169 lb

This force output is significantly greater than the required cracking force of 222.18 N.

Using moment equilibrium again:

Fo / Fi = Lc / Ln

Substituting the actuator force:

222.18 / (169 × 4.448) ≈ 2.9

Assuming

Ln = 4 cm

Then

Lc = 11.59 cm

Height of actuator connection:

Hm = (Ln × Hc) / Lc

Hm ≈ 4.49 cm

---

## Conclusion

The lever based nutcracker design demonstrates how mechanical advantage can be used to convert human grip force into sufficient cracking force.

The initial manual design requires a handle length of approximately **22 cm**, which may reduce usability but provides adequate force amplification.

The actuator driven design significantly reduces the required handle length while providing more consistent cracking force.
