# Project I.G.I. Reverse Engineering & Source Ports

A curated directory of open-source reverse engineering, decompilation, static recompilation, engine reconstruction, console ports, and browser playable projects for the **Project I.G.I.** series developed by Innerloop Studios.

> **Note:** This repository hosts no game code, binaries, or copyrighted assets. All listed projects require a legally owned retail installation of the original games.

---

## 🎮 Project I.G.I.: I'm Going In (IGI 1 - 2000)

### [IGI Recomp (Static Recompilation)](https://github.com/HenryKun55/igi-recomp)
* **Repository:** [https://github.com/HenryKun55/igi-recomp](https://github.com/HenryKun55/igi-recomp)
* **Author:** [@HenryKun55](https://github.com/HenryKun55)
* **Approach:** Ahead-of-Time (AOT) static binary recompilation of retail `IGI.exe` to portable C.
* **Platforms:** macOS (native Apple Silicon ARM64), PlayStation Vita, and PC.
* **Features:** Full 100% playable game logic, 60+ FPS uncapped framerates, widescreen support, Direct3D 7 to modern OpenGL translation, and native Indeo 5 AVI cutscene playback via FFmpeg.

### [IGI-RE (Decompilation)](https://github.com/slickdaddyy/IGI-RE)
* **Repository:** [https://github.com/slickdaddyy/IGI-RE](https://github.com/slickdaddyy/IGI-RE)
* **Author:** [@slickdaddyy](https://github.com/slickdaddyy)
* **Approach:** Reverse engineering and decompilation project targeting the original Project I.G.I. executable.
* **Features:** Function recovery, file format documentation, and disassembled game logic analysis.

### [Project Open IGI (C++20 Reconstruction)](https://github.com/heaven-hm/project-open-igi)
* **Repository:** [https://github.com/heaven-hm/project-open-igi](https://github.com/heaven-hm/project-open-igi)
* **Author:** [@heaven-hm](https://github.com/heaven-hm)
* **Approach:** Modern C++20 engine reconstruction and source port.
* **Features:** Clean-room architecture, modern toolchain integration, cross-platform gameplay reproduction, and developer diagnostics.

---

## 🎯 I.G.I.-2: Covert Strike (IGI 2 - 2003)

### [IGI 2 Decomp (Decompilation)](https://github.com/ShahriyarB/igi2-decomp)
* **Repository:** [https://github.com/ShahriyarB/igi2-decomp](https://github.com/ShahriyarB/igi2-decomp)
* **Author:** [@ShahriyarB](https://github.com/ShahriyarB)
* **Approach:** Reverse engineering and decompilation project targeting the *I.G.I.-2: Covert Strike* executable.
* **Features:** Disassembly analysis, structure recovery, and engine subsystems documentation.

---

## 🕹️ Console & Handheld Ports

### [IGI Vita (Native PlayStation Vita Port)](https://github.com/HenryKun55/igi-vita)
* **Repository:** [https://github.com/HenryKun55/igi-vita](https://github.com/HenryKun55/igi-vita)
* **Author:** [@HenryKun55](https://github.com/HenryKun55)
* **Target Game:** *Project I.G.I.: I'm Going In* (2000)
* **Platform:** PlayStation Vita / PlayStation TV
* **Approach:** Native source port built from static recompilation with Direct3D 7, DirectSound, and DirectInput reimplemented on top of vitaGL and native PS Vita APIs. Performance-critical loops (terrain, meshes, skinning, culling) rewritten for the Vita's ARM CPU.
* **Features:** 
  - 100% playable native experience (menus, all 14 missions, saves, config).
  - Locked 30 FPS gameplay (game's native cap) with automated 444 MHz CPU clock.
  - Native sound, music, FMV cutscenes, and in-engine cutscenes.
  - Full Vita controls: dual analog sticks, front touchscreen aiming, rear touchpad scope zoom, and customizable button mappings.
  - 16:9 widescreen or original 4:3 aspect ratio options.
  - Built-in updater and performance overlay support.

---

## 🌐 Multi-Game / Unified Engines (IGI 1 & IGI 2)

### [OpenIGI (Clean-Room Engine Reimplementation)](https://github.com/OpenIGI/OpenIGI/)
* **Repository:** [https://github.com/OpenIGI/OpenIGI/](https://github.com/OpenIGI/OpenIGI/)
* **Author:** [@ShahriyarB](https://github.com/ShahriyarB)
* **Approach:** Clean-room reimplementation of Innerloop Studios' engine in C# on .NET 10.
* **Description:** An open-source engine for *Project I.G.I.: I'm Going In* (2000) and *I.G.I. 2: Covert Strike* (2003). Runs the original games from your own retail installation. The original missions, scripts, and AI play as they did in 2000, with a modern renderer, launcher, and modding platform built around them.

---

## 🌍 Project I.G.I. in the Browser

Directly playable browser-based implementations and web ports:

### [OpenIGI Web (Enhanced Version)](https://openigi.com/)
* **Website:** [https://openigi.com/](https://openigi.com/)
* **Author:** [@ShahriyarB](https://github.com/ShahriyarB)
* **Description:** Enhanced browser-based version powered by the OpenIGI engine with modern visual improvements and web rendering.

### [Project I.G.I. Web (Vanilla Version)](https://project-igi.pages.dev/)
* **Website:** [https://project-igi.pages.dev/](https://project-igi.pages.dev/)
* **Description:** Faithful, vanilla web browser port running original Project I.G.I. assets and gameplay directly in the browser.

---

## 📌 Status & Future Updates

More reverse engineering projects, tools, file format specifications, and research resources will be updated in the future.

---

## 📬 Submitting to Recompedia

### What to send
Send the repository URL and, if the README does not make it clear, which game version or region it targets. Corrections to existing rows are welcome in the same way; include the line in the repository that shows the change.

**Email:** [submit@recompedia.com](mailto:submit@recompedia.com)

> Recompedia does not host or link to ROMs, BIOS files or game assets. Every project listed requires a copy of the original game owned by the player.

---

## ⚖️ License & Disclaimer

* This repository is licensed under the [MIT License](LICENSE).
* Project I.G.I. and I.G.I.-2 are trademarks and intellectual property of their respective rights holders. This project is unaffiliated with Innerloop Studios, Eidos Interactive, or Codemasters.
