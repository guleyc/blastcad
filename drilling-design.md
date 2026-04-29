---
layout: page
title: Drilling Design (Beta)
nav_order: 3
---

# Drilling Design & Ring Layout <span class="label label-yellow">Beta</span>
{: .no_toc }

BlastCAD is currently testing its advanced **Drill Design Module**. This module allows engineers to construct, visualize, and manipulate 3D drill rings natively in the web browser.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

> **Beta Notice:** The Drilling Design module is actively under development. While core visualization and parameter tracking are functional, some advanced automated layout tools are still being refined.

## 1. 3D Ring Visualization
Drill holes are not just lines; they are fully realized 3D cylinders in the BlastCAD spatial engine. 
* **Dynamic Ring Planes:** BlastCAD automatically computes the orthogonal plane of a drill ring based on the collar coordinates, allowing the camera to snap to a perfect 2D sectional view for editing.
* **Interactive Selection:** Clicking on any hole in the 3D viewport instantly highlights it and pulls its engineering parameters into the right-hand Inspector Panel.

## 2. Core Hole Parameters
Every drill hole in the database tracks the following critical metrics:
* **Collar Coordinates (X, Y, Z):** The start point of the drill hole.
* **Toe Coordinates (X, Y, Z):** The end point of the drill hole.
* **Length & Diameter:** Defines the total drilled length (meters) and bit size (millimeters).
* **Dip & Dump Angles:** Essential for accurate rig alignment and operator handover.

## 3. Distance & Proximity Tracking
To ensure safe burdens and prevent hole deviation issues, BlastCAD features a real-time proximity tracker. Hovering near holes in the 3D view will project dashed distance lines from your cursor to the nearest hole, calculating the exact spatial distance in meters.