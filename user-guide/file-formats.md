---
title: File Formats
parent: User Guide
nav_order: 3
---

# File Formats
{: .no_toc }

BlastCAD can import and export a variety of common CAD and graphics file formats.

<details open markdown="block">
  <summary>Table of contents</summary>
  {: .text-delta }
- TOC
{:toc}
</details>

---

## BlastCAD Native Format (`.blastcad`)

The native format stores all document data — geometry, layers, dimensions, text, and settings — in a structured JSON file with the `.blastcad` extension.

- **Use this format** when you want to continue editing the file in BlastCAD later.
- Files can be opened in any text editor, making them easy to version-control with Git.

**To save as `.blastcad`:**
- `File → Save` (`Ctrl+S`) saves in native format by default.

---

## DXF — Drawing Exchange Format (`.dxf`)

DXF is the industry-standard interchange format for CAD data, originally developed by Autodesk. BlastCAD supports **DXF R12** through **DXF 2018**.

### Importing DXF
1. Click **File → Open** (`Ctrl+O`).
2. Select a `.dxf` file from your computer.
3. BlastCAD will import all supported entities (lines, arcs, circles, polylines, text, dimensions, blocks, and layers).

{: .note }
Some advanced DXF features — such as 3D mesh entities, OLE objects, and proprietary extensions — are not yet supported. Unsupported entities are skipped with a warning in the import log.

### Exporting DXF
1. Click **File → Export** (`Ctrl+E`).
2. Choose **DXF** and select a version (default: **DXF 2013**).
3. Click **Export** and save the file.

---

## SVG — Scalable Vector Graphics (`.svg`)

SVG is an XML-based vector format widely used for web graphics, laser cutting, and vinyl cutting.

### Exporting SVG
1. Click **File → Export** (`Ctrl+E`).
2. Choose **SVG**.
3. Options:
   - **Page size** — export to the document page size or fit to drawing extents.
   - **Units** — choose `px`, `mm`, or `in` for the SVG coordinate system.
4. Click **Export**.

{: .note }
Dimensions and hatch patterns are rasterised in SVG exports. Only geometry and text are exported as true SVG paths.

### Importing SVG
BlastCAD can import SVG files containing paths, rectangles, circles, ellipses, and lines. Complex SVG features such as filters, gradients, and scripts are ignored.

---

## PDF (Export Only) (`.pdf`)

BlastCAD can export drawings as PDF for printing or sharing.

1. Click **File → Print / Export PDF** (`Ctrl+P`).
2. Configure page size, orientation, and scale.
3. Click **Export PDF**.

{: .note }
PDF import is not currently supported.

---

## PNG / JPEG (Export Only)

Export a rasterised image of your drawing.

1. Click **File → Export** (`Ctrl+E`).
2. Choose **PNG** or **JPEG**.
3. Set the **resolution** (DPI) and the area to export (current view or full drawing).
4. Click **Export**.

---

## Format Support Summary

| Format | Import | Export | Notes |
|:-------|:------:|:------:|:------|
| `.blastcad` | ✅ | ✅ | Full fidelity native format |
| `.dxf` | ✅ | ✅ | DXF R12 – DXF 2018 |
| `.svg` | ✅ | ✅ | Path-level geometry only |
| `.pdf` | ❌ | ✅ | Export / print only |
| `.png` | ❌ | ✅ | Raster image export |
| `.jpg` | ❌ | ✅ | Raster image export |
