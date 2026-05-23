# PixelCompass File & Build Guide

[![English](https://img.shields.io/badge/Language-English-blue.svg)](#)
[![Chinese](https://img.shields.io/badge/%E8%AF%AD%E8%A8%80-%E7%AE%80%E4%BD%93%E4%B8%AD%E6%96%87-red.svg)](./README_CN.md)

Welcome to the PixelCompass repository! This repository contains all the open-source production files needed to build your own real-life Minecraft Lodestone Compass.

Complete Documentation: For the step-by-step assembly guide and screenshots, please visit the [PixelCompass: A Low-Cost, Web-Configurable Minecraft Compass IRL](https://chaosgoo.com/en/pixelcompass-a-better-minecraft-compass-irl/).

The hardware package includes the production-ready Gerber files needed for PCB manufacturing, the circuit schematics, and the soldering tools.

* **`Gerber` Folder:** If you do not intend to modify the circuit design, you can directly use the zip files inside the Gerber folder to place an order at any PCB prototyping factory (like JLCPCB, PCBWay, etc.).
* **`ibom.html` (Interactive BOM):** A fantastic tool to assist with hand-soldering (it also allows you to export the BOM as an `.xlsx` file). 
  * *Note:*  Simply click a component to highlight its exact physical location on the board. The item labeled **"ANT-F-2-2.4G-1.0mmFR4-WCH"** in the BOM is a placeholder and does not correspond to any physical component.
* **`Acrylic_Panel_2026-05-23.epanm`:** The dedicated panel engineering file for JLCPCB (Panel Customization service). You can upload this file directly to the platform for hassle-free ordering.
* **`PET.dwg`:** The vector drawing file designed for cutting the internal PET light diffusion mask.

---

# 3D Printed Housing & Enclosure

All 3D printing files and print profiles are hosted on **MakerWorld**:
[Get 3D Printable Files on MakerWorld](https://makerworld.com/en/models/2834513-minecraft-compass-irl#profileId-3158927)

This enclosure is specifically optimized and rebuilt for the Minecraft Compass v2. The print profiles are split into different plates:

* **Plate 1 (Standard Build - Semi-Transparent Look):** Contains the standard `body` parts. This configuration is designed to be paired with a **1mm thick, UV-printed semi-transparent black acrylic panel** on the front surface. For optimal light diffusion, you should place a sheet of **PET LGT075J diffusion film** in the interlayer.
* **Plate 2 (Multi-Color Version - No Acrylic Needed):** Features a split version with a full `faceplate` file for multi-color printing. You can easily color-match the iconic Minecraft pixel textures here. Filament color recommendations (referencing TiX's scheme):
  * White & Black: No specific brand requirements.
  * Dark Grey: **Bambu Lab 10105** (or equivalent).
  * Light Grey: **Bambu Lab 16101** (or equivalent).
* **Plate 3 (Experimental Dual-AMS Version):** This was my earlier dual-AMS test setup. I spent a lot of time testing numerous color combinations and buying a mountain of filament, but never quite found the "perfect" look. Provided purely for reference.

---

## Additional Hardware Notes

* **Battery Specs:** The internal compartment is designed for a **601535 Li-Po battery (280mAh)**. If you plan to use a larger battery for longer runtime, you will need to modify the 3D housing/case source files to fit the increased dimensions.


---

## Firmware & Activation

* **`PixelCompass_Firmware_v1.0.bin`:** The pre-compiled binary file. Use the official **WCHISPTool** to flash it onto your board.
* **Web Dashboard:** [https://dash.chaosgoo.com/pixelcompass/](https://dash.chaosgoo.com/pixelcompass/)
* **Activation:** To connect with the Web Dashboard, grab your free activation code instantly from the Ko-fi shop: **[PixelCompass Activation Code on Ko-fi](https://ko-fi.com/s/ba9368da91)**.
* **Need help with Flashing or Activation?** 
  If you are confused about how to enter BOOT mode, flash the chip, or get your free activation code, we have covered every single detail with screenshots in the blog post:
  **Read the [PixelCompass: A Low-Cost, Web-Configurable Minecraft Compass IRL](https://chaosgoo.com/en/pixelcompass-a-better-minecraft-compass-irl/)**

