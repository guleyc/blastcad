---
layout: page
title: Charging Design (Beta)
nav_order: 4
---

# Charging & Explosives Design <span class="label label-yellow">Beta</span>
{: .no_toc }

The Charging Module allows engineers to define complex explosive columns with real-time feedback on density and quantities.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

> **Beta Notice:** The 3D Charge UI is currently in Beta. You may experience minor UI updates as we optimize the rendering engine for massive drill patterns.

## 1. High-Fidelity 3D Sectional View
BlastCAD introduces a dedicated **Charge Design Mode**. When activated, the camera locks orthogonally to the selected ring. 
Explosive segments are rendered as distinct, color-coded 3D cylinders directly inside the hole body, using advanced polygon offsets to ensure visual precision without rendering artifacts (z-fighting).

## 2. Explosives Database & Decking
Engineers can build multi-deck charges utilizing a built-in material database:
* **Bulk Explosives:** E.g., Emulsion 1.2 ($1.2 \text{ kg/m}^3$), ANFO 0.8.
* **Inert Materials:** Stemming (Gravel) and Air Decks are visually represented but do not contribute to the total explosive mass.

### Segment Adjustments
Charge boundaries can be adjusted mathematically via the Inspector Panel or by utilizing dynamic dragging in future updates. BlastCAD instantly recalculates the **Quantity (kg)** based on the hole diameter, segment length, and material density.

## 3. Primer & Detonator Rules
Initiation logic is critical for blast performance. 
* **Manual Placement:** Add primers at absolute distances from either the **Collar** or the **Toe**.
* **Rule-Based Auto-Apply:** Create logical conditions (e.g., "If charge length > 5m, place a primer 1m from the toe"). BlastCAD can batch-apply these rules to entire rings simultaneously.
* **Visual Highlights:** Primers are rendered as glowing red spheres ($\color{red}{\bullet}$) within the explosive column.

## 4. Proximity Analysis (Burden Circles)
To prevent underloading or overloading near free faces, the Charge Panel includes an interactive **Proximity Circle Editor**.
Engineers can project up to 5 custom-radius concentric circles (e.g., 2m, 3m, 4m) onto the ring plane. These circles act as a visual guide for burden checking against adjacent holes and digitized drive profiles.