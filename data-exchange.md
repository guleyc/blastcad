---
layout: page
title: Data Exchange
---

# Data Exchange & Interoperability

BlastCAD is designed to act as a bridge between major mining software suites. It provides high-fidelity import and export capabilities for industry-standard formats.

### Supported Formats

| Format | Extension | Description |
| :--- | :--- | :--- |
| **GEOVIA Surpac** | `.str` | Full support for Y,X,Z string formats including String ID identification. |
| **AutoCAD** | `.dxf` | Export 3D rings, strings, and holes for site surveyors. |
| **Micromine** | `.str` | Import complex string variables directly into the CAD workspace. |
| **BlastCAD Project** | `.xlsx` | Comprehensive backup format that preserves layers, charging rules, and global origins. |

### Coordinate Transformations
BlastCAD automatically handles the conversion between **Mining Coordinates** (North, East, RL) and **Web Graphics Coordinates** (X, Y, Z). Upon import, a Global Origin is calculated to maintain millimeter precision in a 3D environment.