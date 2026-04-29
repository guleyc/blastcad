---
layout: page
title: Data Exchange & Interoperability
nav_order: 5
---

# Data Exchange & Interoperability
{: .no_toc }

BlastCAD is engineered to function as a seamless bridge between major mining software suites. Instead of locking your data into proprietary formats, BlastCAD reads and writes open, industry-standard string and geometry files.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 1. Supported Import Formats

BlastCAD automatically parses and converts the following formats into a 3D web environment:

| Format | Extension | Origin Software | Description |
|:---|:---|:---|:---|
| **String Files** | `.str` | GEOVIA Surpac | Supports `ID, Y, X, Z` formatted lines. |
| **String Files** | `.str` | Micromine | Supports variable-spaced `X Y Z Color ID` formats. |
| **Comma Separated**| `.csv` | Universal | Imports hole collars, surveys, and toe coordinates. |
| **Excel Project** | `.xlsx`| BlastCAD | Loads complete project state including holes, layers, and global origins. |

### Coordinate Transformation Logic
Mining software typically uses coordinates in the order of **Northing (Y), Easting (X), and Elevation (Z)**. 

When importing a file, BlastCAD parses these coordinates and translates them into the Three.js 3D space using a dynamic **Global Origin** to ensure millimeter precision without floating-point errors:
* 3D `X` = Easting
* 3D `Y` = Elevation (Z)
* 3D `Z` = -Northing (-Y)

## 2. Supported Export Formats

You can export either your entire project or selectively export specific rings and geometries using the **Export Panel**.

* **AutoCAD DXF (`.dxf`):** Exports holes as 3D lines and polygons as `POLYLINE` entities. Perfect for handing over drill plans to site surveyors.
* **Surpac STR (`.str`):** Generates a clean string file compatible with any traditional mining software.
* **BlastCAD 3D Model (`.tmd`):** Compiles high-fidelity triangulated mesh data for physics simulations and advanced rendering.

> **Selection-Based Export:** If no entities are selected in the viewport, BlastCAD exports the entire visible scene. If specific holes or lines are selected, only those items are exported.