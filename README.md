# 📸 PhotoPrint Studio — Brother DCP-T820DW & Multi-Paper Layout Engine

> **Professional photo printing studio for A4, Letter, and custom photo papers.**  
> Built with 100% pure client-side web technologies — zero server, zero installation, privacy-preserving, and mathematically exact.

![License](https://img.shields.io/badge/License-MIT-blue.svg)
![Platform](https://img.shields.io/badge/Platform-Browser%20%7C%20Windows-green.svg)
![Printer](https://img.shields.io/badge/Printer-Brother%20DCP--T820DW%20Ready-purple.svg)
![AI Clean](https://img.shields.io/badge/Gemini%20Watermark-Lossless%20Removal-orange.svg)

---

## ✨ Features Overview

### 1. 🖨️ Multi-Paper & Brother DCP-T820DW Optimization
* **Hardware-Calibrated Layouts:** Specifically designed with 3mm safety margins and paper feed orientation optimized for the **Brother DCP-T820DW** Ink Tank printer.
* **Paper Library:** Supports **A4** (210×297 mm), **US Letter** (8.5×11.0 in), **US Legal** (8.5×14.0 in), **A3**, **A5**, **B5**, **4×6" / 5×7" Dedicated Photo Papers**, and **Custom W×H**.
* **Quick Layout Templates:**
  * **3-Photo Combo:** 2× 4×6" Portrait + 1× 5×7" Landscape (or 1× 5×7" Portrait + 2× 4×6" Landscape).
  * **2× 5×7" Full-Bleed Sheet**.
  * **2× 4×6" Sheet**.
  * **4× 3.5×5" Sheet**.
  * **Standard Grids:** 2×2, 3×3, 4×4, and Passport/ID photo matrices.
* **Instant Orientation Toggle:** Seamlessly switch between **Portrait** and **Landscape** paper orientation with live re-pack.

### 2. ⚡ Smart 2D Guillotine Packing Engine
* **Mathematical Bin Packing:** Uses a 2D recursive Guillotine packing algorithm with Best Short-Side Fit (BSSF) and Split-Minimize rules.
* **Straight-Line Cutting:** Generates cut lines guaranteed to extend edge-to-edge for fast trimming with physical blade guillotines, scissors, or rotary trimmers.
* **Live Slot Inspector:** Click any photo slot on the sheet to manually customize its physical dimensions (in inches or cm), change rotation (90°), tweak positioning, or adjust fit modes (Cover vs. Contain).

### 3. ✨ Gemini Watermark Remover (Reverse Alpha Blending)
* **100% Mathematical & Lossless:** Recovers the true underlying pixels beneath Google Gemini's visible sparkle watermark using reverse alpha blending:
  $$\text{Pixel}_{\text{original}} = \frac{\text{Pixel}_{\text{watermarked}} - \alpha \times 255}{1 - \alpha}$$
* **No Generative AI Hallucinations:** Unlike inpainting, reverse alpha blending accurately restores original textures with zero blurriness.
* **Embedded High-Precision Profiles:** Contains calibrated $96 \times 96$ and $48 \times 48$ alpha maps with spatial cross-correlation auto-detection.
* **Photo-Level Workflow:** Watermarks can be cleaned automatically on upload or on-demand in the Photo Pool tray *before* assigning photos to print slots.

### 4. 🧹 Interactive Magic Eraser & Touch-up Brush
* **In-Canvas Texture Inpainting:** Brush over unwanted text, timestamps, photobombers, or non-standard watermarks with an adjustable size brush ($6\text{ px}$ to $70\text{ px}$).
* **Multi-Pass Dirichlet-Poisson Solver:** Propagates surrounding textures and colors into the masked region smoothly and naturally.
* **Undo/Redo & Direct Synchronization:** Instant live preview with one-click synchronization to all assigned layout slots.

### 5. 📄 High-Res Print & Word (.doc) Export
* **Native Browser Print:** Press <kbd>Ctrl</kbd> + <kbd>P</kbd> for 300+ DPI direct hardware output with exact millimeter CSS coordinates.
* **Microsoft Word Export:** Generates an editable `.doc` file with tables and dimensions pre-configured to physical printer specs.

---

## 🚀 Getting Started

### Method 1: Instant Launch (Windows)
Double-click [`PhotoPrint_Studio.bat`](PhotoPrint_Studio.bat) or open `index.html` in any modern web browser (Google Chrome, Microsoft Edge, Mozilla Firefox, Brave).

### Method 2: Host via GitHub Pages
1. In your GitHub repository settings, go to **Settings &rarr; Pages**.
2. Select the `main` branch as the build source and save.
3. Your photo printing studio is now accessible online anywhere from your phone, tablet, or PC!

---

## 🔧 Technical Details
* **Technology Stack:** Pure HTML5, Vanilla JavaScript (ES6+), Canvas API, and Vanilla CSS.
* **Dependencies:** None. Completely standalone and self-contained in a single file.
* **Data Privacy:** All photo rendering, image cropping, and watermark removal execute strictly inside your local browser memory. No photos are ever uploaded to an external server.

---

## 📄 License
This project is licensed under the [MIT License](LICENSE).
