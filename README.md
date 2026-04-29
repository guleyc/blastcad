# 💥 BlastCAD

![BlastCAD Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![React](https://img.shields.io/badge/React-18.x-61dafb.svg?logo=react)
![Three.js](https://img.shields.io/badge/Three.js-WebGL-black.svg?logo=three.js)

**BlastCAD** is a next-generation, high-performance, web-based 3D CAD platform specifically engineered for underground mining and drill & blast design. 

By bridging the gap between traditional desktop mining software and modern cloud architecture, BlastCAD provides millimeter-precision drafting, complex volumetric explosive calculations, and seamless industry data interoperability.

📚 **[Read the Official Documentation](https://docs.blastcad.com)**

---

## ✨ Core Features

* **📐 Advanced Drafting & Modification Kernel:** Draft, edit, and manipulate boundaries and drill rings directly in your browser. Features AutoCAD-like terminal commands, precision OSNAP, Trim, Extend, and Offset algorithms.
* **💥 High-Fidelity 3D Charging Engine:** Design complex explosive columns, air decks, and stemming layers with real-time feedback on segment volumes ($m^3$) and explosive masses ($kg$).
* **🔄 Industry Interoperability:** Stop locking your data into proprietary formats. Natively import and export **GEOVIA Surpac (.str)**, **Micromine**, and **AutoCAD (.dxf)** files.
* **🔒 AuthGuard Security:** A robust JWT-based session management system that protects your unsaved engineering data from background token expirations and network timeouts.

---

## 🛠️ Tech Stack

BlastCAD is built for maximum browser performance using modern web technologies:

* **Frontend Framework:** React 18 with TypeScript
* **3D Graphics Engine:** Three.js & React Three Fiber (R3F)
* **State Management:** Zustand
* **Styling:** CSS Modules & FontAwesome
* **Data Handling:** SheetJS (XLSX) & Custom CAD/STR Parsers

---

## 👨‍💻 Author
J. Guley - Mining Engineer & Developer Perth, Western Australia