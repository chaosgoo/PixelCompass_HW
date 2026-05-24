# PixelCompass File & Build Guide

[![English](https://img.shields.io/badge/Language-English-blue.svg)](#)
[![Chinese](https://img.shields.io/badge/%E8%AF%AD%E8%A8%80-%E7%AE%80%E4%BD%93%E4%B8%AD%E6%96%87-red.svg)](./README_CN.md)

Welcome to the PixelCompass hardware repository! This repo contains the full set of open-source production files needed to build a real-life Minecraft Lodestone Compass.
![img/better-minecraft-compass-irl](img/better-minecraft-compass-irl.jpg)
Full illustrated tutorial: For the detailed soldering steps, BOOT flashing screenshots, and the rest of the walkthrough, please see my blog post: [PixelCompass: A Low-Cost, Web-Configurable Minecraft Compass IRL](https://chaosgoo.com/en/pixelcompass-a-better-minecraft-compass-irl/).

This repository includes the Gerber files for PCB manufacturing, the circuit schematic, and a few helper files for assembly and soldering.

* **`Gerber` folder:** Production files for PCB fabrication. Upload them to any PCB prototyping service, such as JLCPCB, PCBWay, or a similar vendor, and place the board order directly.
* **`ibom.html` (Interactive BOM):** A handy helper for hand soldering. It can also export the bill of materials as an `.xlsx` spreadsheet.
    * **Note:** Click a component in the interactive BOM page to highlight its position on the PCB.
    * The part marked **"ANT-F-2-2.4G-1.0mmFR4-WCH"** in the BOM is only an **on-board antenna placeholder**. It does not correspond to any physical electronic component and can simply be ignored.
* **`Acrylic_Panel_2026-05-23.epanm`:** File for producing the acrylic front panel, exported from EasyEDA.
* **`PET.dwg`:** Drawing for cutting the PET diffusion film used in the middle layer.

---

# 3D Printed Housing and Structural Parts

All 3D printing files are hosted on **MakerWorld**:
[Get the 3D printing files on MakerWorld](https://makerworld.com/en/models/2834513-minecraft-compass-irl%23profileId-3158927)

**This version is not compatible with the previous ESP32C3 version.**

The print plates are split into the following parts:

* **Plate 1 (Standard version - semi-transparent acrylic build):** Includes the standard `body` part. This is intended to be used with a **1 mm thick black semi-transparent acrylic front panel with UV printing on the top surface**. A sheet of **PET LGT075J diffusion film** should be placed in the middle layer.
* **Plate 2 (Multi-color version - no acrylic needed):** Includes a complete `faceplate` structural part, suitable for multi-color printing. Recommended filament colors, based on TiX's color scheme:
    * Black and white: no specific brand requirement.
    * Dark gray: **Bambu Lab official filament 10105** or an equivalent color.
    * Light gray: **Bambu Lab official filament 16101** or an equivalent color.
* **Plate 3 (Experimental dual-AMS six-color version):** This was my early dual-AMS test setup. I bought a pile of filament to test the final look, but never quite found the "perfect" result, so this plate is provided for reference only.

---

## Additional Hardware Notes

* **Battery size:** The battery space inside the shell is designed specifically for a **601535 Li-Po battery (280 mAh)**. If you want to use a larger battery for longer runtime, you will need to modify the 3D shell source files yourself to fit the larger cell.

---

## Firmware and Activation

* **On the [Release](https://github.com/chaosgoo/PixelCompass_HW/releases) page:** You can download the precompiled firmware. Please flash it to the board using WCH's official **WCHISPTool**.
* **Web Dashboard:** [https://dash.chaosgoo.com/pixelcompass/](https://dash.chaosgoo.com/pixelcompass/)
* **Activation:** The first time the device connects to the Dashboard, it will ask for a free activation code. You can get one directly from my Ko-fi shop for free, and the system will send it automatically: **[Get a free activation code on Ko-fi](https://ko-fi.com/s/ba9368da91)**.

For more details, please visit the blog post: **Read [PixelCompass: A Low-Cost, Web-Configurable Minecraft Compass IRL](https://chaosgoo.com/en/pixelcompass-a-better-minecraft-compass-irl/)**
