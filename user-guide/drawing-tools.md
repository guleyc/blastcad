---
title: Drawing Tools
parent: User Guide
nav_order: 2
---

# Drawing Tools
{: .no_toc }

<details open markdown="block">
  <summary>Table of contents</summary>
  {: .text-delta }
- TOC
{:toc}
</details>

---

## Line

**Shortcut:** `L`

Draws straight line segments between two or more points.

**Usage:**
1. Press `L` or click the **Line** icon in the toolbar.
2. Click to place the start point.
3. Click to place the end point (or type a distance + `Enter` for exact length).
4. Continue clicking to draw connected segments, or press `Escape` to finish.

**Tips:**
- Hold `Shift` to constrain the line to 0°, 45°, or 90° angles.
- Type a value and press `Tab` to switch between X and Y coordinate inputs.

---

## Rectangle

**Shortcut:** `R`

Draws an axis-aligned rectangle by specifying two opposite corners.

**Usage:**
1. Press `R` or click the **Rectangle** icon.
2. Click to place the first corner.
3. Move the cursor and click to place the opposite corner — or type `width,height` + `Enter` for exact dimensions.

**Tip:** Press `Ctrl` while placing the second corner to draw from the center outward.

---

## Circle

**Shortcut:** `C`

Draws a circle by center and radius.

**Usage:**
1. Press `C` or click the **Circle** icon.
2. Click to set the center point.
3. Move the cursor and click to set the radius — or type a radius value + `Enter`.

**Alternate methods** (available in the **Draw → Circle** menu):
- **3-Point Circle** — passes through three specified points.
- **2-Point Circle** — diameter defined by two points.

---

## Arc

**Shortcut:** `A`

Draws a circular arc.

**Usage (3-point arc, default):**
1. Press `A` or click the **Arc** icon.
2. Click to set the start point.
3. Click to set a point on the arc.
4. Click to set the end point.

**Alternate methods** (Draw → Arc menu):
- **Center, Start, End** — specify center, then start angle, then end angle.
- **Center, Start, Length** — specify center, start, and chord length.

---

## Polyline

**Shortcut:** `P`

Draws a connected sequence of line and arc segments as a single entity.

**Usage:**
1. Press `P` or click **Polyline**.
2. Click successive points to add line segments.
3. Press `A` mid-sequence to switch to arc mode for the next segment.
4. Press `L` to switch back to line mode.
5. Press `C` or click the start point to **close** the polyline.
6. Press `Escape` to finish without closing.

---

## Text

**Shortcut:** `T`

Places a text annotation on the drawing.

**Usage:**
1. Press `T` or click **Text**.
2. Click to place the text insertion point.
3. Type your text in the input box that appears.
4. Press `Enter` to confirm; press `Escape` to cancel.

In the **Properties Panel** you can change the font, size, alignment, and rotation.

---

## Dimensions

Dimensions measure and annotate geometry. All dimension tools are in the **Dimension** menu and the toolbar's **Dimension** group.

### Linear Dimension
Measures the horizontal or vertical distance between two points.
1. Select **Dimension → Linear** (or shortcut `D L`).
2. Click the first point.
3. Click the second point.
4. Click to place the dimension line.

### Aligned Dimension
Like Linear but measures along the line connecting the two points.
Shortcut: `D A`

### Radial Dimension
Measures the radius of a circle or arc.
1. Select **Dimension → Radial** (or `D R`).
2. Click on the circle or arc.
3. Click to place the dimension label.

### Diameter Dimension
Measures the diameter of a circle.
Shortcut: `D D`

### Angular Dimension
Measures the angle between two lines.
Shortcut: `D N`

---

## Modify Tools

### Move — `M`
Moves selected objects to a new position.
1. Select one or more objects.
2. Press `M`.
3. Click a base point.
4. Click the destination — or type `dx,dy` for an exact offset.

### Rotate — `O`
Rotates selected objects around a pivot.
1. Select objects, press `O`.
2. Click the pivot point.
3. Click or type an angle.

### Scale — `K`
Scales selected objects from a base point.
1. Select objects, press `K`.
2. Click the base point.
3. Type a scale factor (e.g. `2` for 200%) and press `Enter`.

### Mirror — `I`
Mirrors selected objects across a line.
1. Select objects, press `I`.
2. Click two points that define the mirror axis.
3. Choose whether to **copy** or **move** the objects.

### Offset — `F`
Creates a parallel copy of a line, arc, circle, or polyline at a specified distance.
1. Press `F`, then type the offset distance + `Enter`.
2. Click the object to offset.
3. Click on the side you want the new object to appear.

### Trim — `X`
Trims objects to a cutting edge.
1. Press `X`.
2. Click the cutting-edge objects (the boundaries to trim to), then press `Enter`.
3. Click the parts of objects you want to remove.

### Extend — `E`
Extends objects to a boundary edge.
1. Press `E`.
2. Click boundary objects, then press `Enter`.
3. Click the ends of objects you want to extend.
