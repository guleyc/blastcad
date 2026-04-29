---
title: Workspace Overview
parent: User Guide
nav_order: 1
---

# Workspace Overview
{: .no_toc }

<details open markdown="block">
  <summary>Table of contents</summary>
  {: .text-delta }
- TOC
{:toc}
</details>

---

## Layout

When you open a document in BlastCAD, the window is divided into four main areas:

```
┌──────────────────────────────────────────────────────────┐
│  Menu Bar                                                │
├────────┬─────────────────────────────────┬───────────────┤
│        │                                 │               │
│  Left  │           Canvas                │  Properties   │
│ Toolbar│                                 │    Panel      │
│        │                                 │               │
├────────┴─────────────────────────────────┴───────────────┤
│  Status Bar                                              │
└──────────────────────────────────────────────────────────┘
```

---

## Menu Bar

The **Menu Bar** at the top contains the main application menus:

| Menu | Contents |
|:-----|:---------|
| **File** | New, Open, Save, Export, Document Settings |
| **Edit** | Undo, Redo, Cut, Copy, Paste, Select All |
| **View** | Zoom, Pan, Grid, Snap, Layer Visibility |
| **Draw** | All drawing tools (also accessible from the toolbar) |
| **Modify** | Move, Rotate, Scale, Mirror, Trim, Extend, Offset |
| **Dimension** | Linear, Angular, Radial, Diameter dimensions |
| **Help** | Documentation, Keyboard Shortcuts, About |

---

## Left Toolbar

The **Left Toolbar** gives quick access to the most-used tools. Tools are grouped into sections:

### Selection & View
| Icon | Tool | Shortcut |
|:-----|:-----|:---------|
| Arrow | Select | `V` or `Esc` |
| Hand | Pan | `H` or middle-mouse-drag |
| Magnifier | Zoom | `Z` |

### Drawing
| Icon | Tool | Shortcut |
|:-----|:-----|:---------|
| / | Line | `L` |
| □ | Rectangle | `R` |
| ○ | Circle | `C` |
| ⌒ | Arc | `A` |
| … | Polyline | `P` |
| T | Text | `T` |

### Modify
| Icon | Tool | Shortcut |
|:-----|:-----|:---------|
| ↕ | Move | `M` |
| ↻ | Rotate | `O` |
| ↔ | Mirror | `I` |
| ⬡ | Offset | `F` |
| ✂ | Trim | `X` |

---

## Canvas

The **Canvas** is the drawing area. You interact with it using the mouse or touch:

- **Left-click** — place points, select objects.
- **Right-click** — context menu with quick actions.
- **Scroll wheel** — zoom in and out.
- **Middle-mouse drag** — pan the view.
- **Double-click** — finish a polyline or enter edit mode for text.

### Coordinate Display

The bottom-left of the canvas shows the cursor's current X/Y coordinates in the document's units. Coordinates are displayed relative to the document origin (0, 0).

### Snap Indicators

When **Snap** is enabled (default), small coloured icons appear on the canvas showing what the cursor will snap to:

| Colour | Snap type |
|:-------|:----------|
| 🟡 Yellow | Grid snap |
| 🔵 Blue | Endpoint |
| 🟢 Green | Midpoint |
| 🔴 Red | Intersection |
| ⚪ White | Perpendicular / Tangent |

---

## Properties Panel

The **Properties Panel** on the right shows and lets you edit the properties of whatever is currently selected:

- **No selection** — shows document properties (units, page size).
- **Single object** — shows that object's layer, colour, line weight, and geometry values (e.g. length, radius).
- **Multiple objects** — shows shared properties; changing a value updates all selected objects.

---

## Status Bar

The **Status Bar** at the bottom shows:

- Active tool name and a short usage hint.
- Current snap mode.
- Current layer name.
- Zoom level.

---

## Keyboard Shortcuts Reference

Press `?` at any time to open the full keyboard shortcut reference overlay.

Common shortcuts:

| Action | Windows / Linux | macOS |
|:-------|:----------------|:------|
| New document | `Ctrl+N` | `⌘N` |
| Open | `Ctrl+O` | `⌘O` |
| Save | `Ctrl+S` | `⌘S` |
| Export | `Ctrl+E` | `⌘E` |
| Undo | `Ctrl+Z` | `⌘Z` |
| Redo | `Ctrl+Y` | `⌘⇧Z` |
| Select All | `Ctrl+A` | `⌘A` |
| Delete selected | `Delete` | `Delete` / `Fn+⌫` |
| Zoom to fit | `Ctrl+Shift+H` | `⌘⇧H` |
| Toggle grid | `G` | `G` |
| Toggle snap | `S` | `S` |
