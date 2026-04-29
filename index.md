---
layout: default
title: Home
nav_order: 1
description: "Official documentation for the BlastCAD engineering platform."
permalink: /
---

# Welcome to BlastCAD Documentation
{: .fs-9 }

The definitive engineering manual for the next-generation, web-based 3D CAD and underground blast design platform.
{: .fs-6 .fw-300 }

[Start Drafting](/drafting/){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }
[Charging Logic](/charging/){: .btn .fs-5 .mb-4 .mb-md-0 }

---

## 🚀 The Engineering Hub
{: .mt-6 }

BlastCAD is built to bridge the gap between traditional desktop mining software and modern cloud architecture. Explore the core modules below to master the platform.

### 📐 [Drafting & Modification](/drafting/)
Discover the robust geometric kernel. Learn how to use the Command Terminal, execute AutoCAD-like modifications (Trim, Extend, Offset), and utilize the precision OSNAP engine.

### 💥 [Charging & Volumetric Calculations](/charging/)
Dive into the mathematics behind BlastCAD. Understand how the 3D rendering engine calculates segment volumes, explosive mass, and handles complex decking rules.

### 🔄 [Data Interoperability](/data-exchange/)
Stop locking your data into proprietary files. Learn how BlastCAD natively reads and writes industry standards like **GEOVIA Surpac (.str)**, **Micromine**, and **AutoCAD (.dxf)**.

### 🔒 [AuthGuard Security](/security/)
Your engineering data is critical. Read about our underlying session management system that freezes your workspace and prevents data loss during background token expirations.

---

## 🖥️ System Requirements

BlastCAD relies heavily on hardware-accelerated 3D graphics (WebGL). To ensure maximum performance with large geological models and complex ring designs:

* **Browser:** Google Chrome, Brave, or Microsoft Edge (Latest versions strongly recommended).
* **Device:** Desktop or Laptop only. Mobile access is restricted to ensure engineering precision.
* **Network:** A stable connection is required for initial login, but the core 3D engine processes data locally on your machine.