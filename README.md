# Nebula Custom Boot Animation for Android💙🎇

An elegant, premium custom Android boot animation and splash screen sequence featuring fluid droplet physics and minimalist branding.

---

## 🎨 Design Source

* *Figma Project File:* [View Design Concept on Figma] (https://www.figma.com/proto/9rEKlmrrViJ2qV5NbDtDtc/Untitled?node-id=55-2&p=f&t=M4BSB0G9dRj7yOEi-0&scaling=scale-down&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=1%3A2)

---

## 📖 Project Overview

The *Nebula* boot sequence is designed around fluid simulation kinetics. It consists of multiple stages, seamlessly moving from minimalist fluid movement to an high-energy ignition, and finally presenting a refined brand lockup before revealing the home screen.

### Animation Stages

1. *Stage A (The Kinetic Droplets):* A deep blue fluid droplet moves from top to bottom, eventually creating a secondary droplet. They stretch and merge in the center of a dark void, creating a perfect circular orb of energy.
2. *Stage B (The Flash):* The orb expands to engulf the screen in a solid, vibrant blue canvas.
3. *Stage C (The Ignition):* A bright blue gradient fades in, revealing the state indicator: IGNITING...
4. *Stage D (Nebula Reveal):* The transition clears to reveal the primary branding, *"NEBULA"*, typeset in a sophisticated serif typeface centered over a rich, deep blue gradient.
5. *Stage E (The Hand-off):* The animation fades out cleanly as the Android System Server hands over the display control to the SystemUI launcher.

---

## 🛠️ Features

* *Fluid Framerate:* Rendered at a solid 60 FPS for desktop-grade fluidity.
* *Resolution Agnostic:* Packaged for multiple standard Android resolutions (1080x2400, 1440x3200, etc.).
* *Modular Architecture:* Easily customizable frame sequences and color palettes.
* *Magisk Ready:* Includes template files to flash instantly as a systemless Magisk module.

---

## 🚀 Installation Methods

Select the method that best matches your device setup. 

> ⚠️ *Disclaimer:* Modifying system files carries a risk of soft-bricking or bootloops. Ensure you have a custom recovery (like TWRP or OrangeFox) and a full system backup before proceeding.

### Method 1: Magisk Module (Recommended)
1. Download the nebula-bootanimation-magisk.zip from the *Releases* tab.
2. Open the *Magisk App* on your rooted Android device.
3. Navigate to the *Modules* tab, tap *Install from storage*, and select the zip.
4. Reboot your device to enjoy Nebula.

### Method 2: Manual Installation (Root Required)
If you prefer to manually place the animation file:
1. Download the raw bootanimation.zip from the /build directory.
2. Using a root-enabled file explorer (e.g., Solid Explorer or MiXplorer), navigate to /system/media/ (or /product/media/ depending on your ROM).
3. Copy and replace the existing bootanimation.zip.
4. Change file permissions to *rw-r--r-- (0644)*.
5. Reboot your device.

---

## ⚙️ Technical Structure & Customization

The root folder of the boot animation is built inside a standard bootanimation.zip container compressed strictly with *"Store" (0% compression)*:

```text
bootanimation.zip
├── desc.txt            # Animation speed, loop parameters, and resolution
├── part0/              # Stage A: Merging droplet frames (000.png - 045.png)
├── part1/              # Stage B: Solid flash & IGNITING sequence
└── part2/              # Stage C: "NEBULA" splash & fade-out
