---
layout: page
title: Charging Logic & Volumetric Calculations
nav_order: 4
---

# Charging Logic & Volumetric Calculations
{: .no_toc }

BlastCAD features a high-fidelity 3D charging engine that provides real-time volumetric feedback for every charge segment defined in your blast holes. This page explains the underlying mathematics and logic BlastCAD uses to calculate explosive masses and volumes.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 1. Hole Geometry and Volume

In BlastCAD, every drill hole is treated as a perfect cylinder in 3D space. When you assign an explosive or stemming material to a specific segment of the hole, the software first calculates the exact volume of that segment.

The volumetric calculation uses the standard cylindrical volume formula:

$$V_{seg} = \frac{\pi \cdot d^2}{4} \cdot (z_{end} - z_{start})$$

**Where:**
* $V_{seg}$: Volume of the charge segment ($m^3$)
* $d$: Diameter of the drill hole (converted from mm to meters)
* $z_{end} - z_{start}$: Vertical length of the column ($L_{seg}$) in meters

## 2. Explosive Mass Calculation

Once the volume is determined, BlastCAD calculates the total mass of the explosive for that segment. This relies on the specific gravity (density) of the material selected from your **Explosives Database** (e.g., Emulsion 1.2, ANFO 0.8).

$$M_{seg} = V_{seg} \cdot \rho_{exp}$$

**Where:**
* $M_{seg}$: Total mass of the explosive in the segment (kg)
* $\rho_{exp}$: Density of the explosive ($kg/m^3$)

### Linear Charge Concentration (LCC)
For quick engineering checks, BlastCAD also utilizes the Linear Charge Concentration (kg/m), which simplifies the mass calculation per meter of the hole:

$$LCC = \frac{\pi \cdot d^2}{4} \cdot \rho_{exp}$$

## 3. Multi-Segment Charging (Decking)

BlastCAD is fully equipped to handle complex loading rules, including multiple explosive decks, stemming layers, and air decks within a single hole. 

The total explosive mass per hole is simply the summation of all active explosive segments (excluding inert materials like stemming):

$$M_{total} = \sum_{i=1}^{n} M_{i}$$

## 4. 3D Rendering & Visual Precision

To ensure clear visibility in the 3D viewport, BlastCAD uses an advanced rendering technique. Charge segments and primers are generated using **Polygon Offsets**. 

This prevents *z-fighting* (flickering between the hole line and the 3D cylinder), ensuring that your explosive columns are always rendered millimeter-perfectly slightly ahead of the hole's center line.

> **Note:** Primers are visually represented as solid spheres and are placed exactly at the depth values specified in your primer rules. Their volumes are considered negligible and are not subtracted from the total explosive mass.