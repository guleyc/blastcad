---
layout: page
title: Drafting & Modification Tools
nav_order: 3
---

# Drafting & Modification Tools
{: .no_toc }

BlastCAD provides a robust geometric kernel that allows you to draft, edit, and manipulate boundaries, fault lines, and drill rings with AutoCAD-like precision directly in your browser.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 1. The Command Terminal
At the bottom of the interface lies the **Command Terminal**. It accepts standard CAD commands and relative coordinate inputs.

* **Absolute Coordinates:** Type `100,50` to draw to an exact X,Y point.
* **Relative Coordinates:** Type `@10,5` to move 10 units East and 5 units North from the last point.

## 2. Modification Kernel

BlastCAD includes advanced modification algorithms for manipulating your geometry:

### Trim (`TRIM`)
Removes segments of an entity that cross a selected cutting edge. BlastCAD calculates the exact mathematical intersection point of the vectors and splits the polyline accordingly.

### Extend (`EXTEND`)
Projects a line or polyline to meet a selected boundary. The software calculates the projected trajectory and extends the vertex to the exact collision point.

### Offset (`OFFSET`)
Creates parallel lines or concentric polylines. 
* For a given line $AB$, the offset line $A'B'$ is generated at a specified distance $D$ by calculating the normal vector of $AB$.

## 3. Object Snapping (OSNAP)
Precision is critical in mining. BlastCAD's snap engine automatically detects and highlights critical geometric points when you hover near them:
* **Endpoint:** Snaps to the start or end of a line.
* **Midpoint:** Snaps exactly to the center of a segment.
* **Center:** Snaps to the center of a circle or arc.
* **Nearest:** Snaps to the closest projected point on a line.