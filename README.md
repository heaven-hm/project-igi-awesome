# Project I.G.I. Reverse Engineering & Source Ports

A curated directory of open-source reverse engineering, decompilation, static recompilation, engine reconstruction, macOS/Linux ports, console ports, and browser playable projects for the **Project I.G.I.** series developed by Innerloop Studios.

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

### [re-igi / reimagine-igi (Web Browser Reimplementation)](https://github.com/Haseebraza12/reimagine-igi)
* **Repository:** [https://github.com/Haseebraza12/reimagine-igi](https://github.com/Haseebraza12/reimagine-igi)
* **Author:** [@Haseebraza12](https://github.com/Haseebraza12)
* **Approach:** Browser-native reimplementation in TypeScript, Vite, and Three.js reading original retail files directly at runtime without pre-converting assets.
* **Platforms:** Web Browsers (Web only).
* **Features:**
  - Loads and plays all 14 missions of the full game decoded at runtime from legally owned retail files.
  - Faithful octree terrain with LOD transitions, vertex geomorph, ground relief, and lightmaps.
  - Complete 49-state player movement graph, 3-ray character collision sweep, and original 4:3 camera optics (90° × 73.74°).
  - Recovered vehicle physics (moving trains, helicopters), patrol AI, and dynamic sound mixing.

---

## 🎯 I.G.I.-2: Covert Strike (IGI 2 - 2003)

### [IGI 2: Covert Strike Web Port (Static Recompilation to WebAssembly & Mac)](https://github.com/swampodsarkar321/IGI-WEB)
* **Repository:** [https://github.com/swampodsarkar321/IGI-WEB](https://github.com/swampodsarkar321/IGI-WEB)
* **Live Demo / Web Port:** [https://iglweb-olive.vercel.app/](https://iglweb-olive.vercel.app/)
* **Author:** [@swampodsarkar321](https://github.com/swampodsarkar321)
* **Approach:** Static binary recompilation of the retail x86 executable into portable C via Ghidra and custom tooling (31,547 recovered functions, ~1.3 million instructions), compiled to WebAssembly via Emscripten and native macOS via Clang.
* **Platforms:** Web Browsers (WebAssembly & WebGPU) and macOS (native Apple Silicon).
* **Features:**
  - Direct3D 8 pipeline translated to WebGPU and WGSL shaders.
  - DirectSound mapped to Web Audio; DirectInput mapped to Web Gamepad API, mouse, and keyboard.
  - Online 1v1 multiplayer with deterministic lockstep netplay.
  - Full memory layout preservation matching original pointer and C++ vtable structures.

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

## 🍏 macOS & Linux Ports

Standalone desktop ports and native distributions for macOS and Linux:

### [Project I.G.I. macOS Standalone App](https://github.com/rishabhgupta3107/igi-browser)
* **Repository:** [https://github.com/rishabhgupta3107/igi-browser](https://github.com/rishabhgupta3107/igi-browser)
* **Author:** [@rishabhgupta3107](https://github.com/rishabhgupta3107)
* **macOS Download (Apple Silicon M1+):** [`Project-IGI-Mac-Apple-Chip.zip`](https://github.com/rishabhgupta3107/igi-browser/releases/latest/download/Project-IGI-Mac-Apple-Chip.zip)
* **macOS Download (Intel):** [`Project-IGI-Mac-Intel.zip`](https://github.com/rishabhgupta3107/igi-browser/releases/latest/download/Project-IGI-Mac-Intel.zip)
* **Description:** Native macOS app bundle (`Project IGI.app`) powered by WebGPU, featuring widescreen, sharper graphics, gamepad controller support, and dive mechanics without requiring an emulator.

### [OpenIGI Desktop (macOS & Linux Client)](https://openigi.com/)
* **Website:** [https://openigi.com/](https://openigi.com/)
* **Repository:** [https://github.com/OpenIGI/OpenIGI/](https://github.com/OpenIGI/OpenIGI/)
* **Author:** [@ShahriyarB](https://github.com/ShahriyarB)
* **macOS & Linux Terminal Installation:**
  ```bash
  curl -fsSL https://openigi.com/install.sh | bash
  ```
* **Description:** Clean-room engine reimplementation running natively on macOS and Linux desktop via an automated launcher and updater.

---

## 🌐 Multi-Game / Unified Engines (IGI 1 & IGI 2)

### [OpenIGI (Clean-Room Engine Reimplementation)](https://github.com/OpenIGI/OpenIGI/)
* **Repository:** [https://github.com/OpenIGI/OpenIGI/](https://github.com/OpenIGI/OpenIGI/)
* **Author:** [@ShahriyarB](https://github.com/ShahriyarB)
* **Approach:** Clean-room reimplementation of Innerloop Studios' engine in C# on .NET 10.
* **Platforms:** Windows, macOS, and Linux desktop (`curl -fsSL https://openigi.com/install.sh | bash` via [openigi.com](https://openigi.com/)), and Web.
* **Description:** An open-source engine for *Project I.G.I.: I'm Going In* (2000) and *I.G.I. 2: Covert Strike* (2003). Runs the original games from your own retail installation. The original missions, scripts, and AI play as they did in 2000, with a modern renderer, launcher, and modding platform built around them.

---

## 🌍 Browser Playable Ports & Web Implementations

> 📊 **In-Depth Comparison:** See [IGI_1_WEB_PORTS_COMPARISON.md](IGI_1_WEB_PORTS_COMPARISON.md) for a technical breakdown, architecture analysis, and comparison ratings across all web ports.

Directly playable browser-based implementations and web ports:

### [PlayIGI (Mobile Browser)](https://playigi.com/play)
* **Website / Play:** [https://playigi.com/play](https://playigi.com/play)
* **Category:** Mobile-only browser-playable entry
* **Platform:** Mobile web browsers (iOS Safari and Android browsers; compatibility should be verified on the target device)
* **Description:** Opens the hosted PlayIGI experience directly in a browser. Listed as a mobile-focused option; this repository does not host the game or its assets, and mobile-device compatibility has not been independently tested.

### [re-igi / reimagine-igi (Web Only Reimplementation)](https://github.com/Haseebraza12/reimagine-igi)
* **Repository:** [https://github.com/Haseebraza12/reimagine-igi](https://github.com/Haseebraza12/reimagine-igi)
* **Author:** [@Haseebraza12](https://github.com/Haseebraza12)
* **Target Game:** *Project I.G.I.: I'm Going In* (2000)
* **Platform:** Web Browsers (Web only)
* **Description:** Browser-native vertical slice and full reimplementation built on TypeScript, Vite, and Three.js. Loads and plays all 14 original missions by reading the player's retail files directly at runtime in the browser.

### [Project I.G.I. Browser Port (Web & macOS)](https://rishabhgupta3107.github.io/igi-browser/)
* **Website:** [https://rishabhgupta3107.github.io/igi-browser/](https://rishabhgupta3107.github.io/igi-browser/)
* **Repository:** [https://github.com/rishabhgupta3107/igi-browser](https://github.com/rishabhgupta3107/igi-browser)
* **Author:** [@rishabhgupta3107](https://github.com/rishabhgupta3107)
* **macOS Standalone Build:** [`Project-IGI-Mac-Apple-Chip.zip`](https://github.com/rishabhgupta3107/igi-browser/releases/latest/download/Project-IGI-Mac-Apple-Chip.zip)
* **Description:** Playable in-browser port running via WebGPU with widescreen support, sharper graphics, gamepad controller support, and standalone desktop builds for macOS and Windows.

### [IGI 2: Covert Strike Web Port](https://iglweb-olive.vercel.app/)
* **Website:** [https://iglweb-olive.vercel.app/](https://iglweb-olive.vercel.app/)
* **Repository:** [https://github.com/swampodsarkar321/IGI-WEB](https://github.com/swampodsarkar321/IGI-WEB)
* **Author:** [@swampodsarkar321](https://github.com/swampodsarkar321)
* **Description:** Playable in-browser port of *I.G.I.-2: Covert Strike* running via WebAssembly, WebGPU, and Web Audio with 1v1 online multiplayer and game controller support.

### [OpenIGI Web (Enhanced Version)](https://openigi.com/)
* **Website:** [https://openigi.com/](https://openigi.com/)
* **Author:** [@ShahriyarB](https://github.com/ShahriyarB)
* **Description:** Enhanced browser-based version powered by the OpenIGI engine with modern visual improvements and web rendering.


### [Project I.G.I. Web (Vanilla Version)](https://project-igi.pages.dev/)
* **Website:** [https://project-igi.pages.dev](https://project-igi.pages.dev/)
* **Description:** Faithful, vanilla web browser port running original Project I.G.I. assets and gameplay directly in the browser.


### [Project I.G.I. Web (ReComp)](https://github.com/sagarinfosec/project-igi-browser)
* **Website:** [project-igi-browser](https://igi.sagarinfosec.site)
* **Description:** Faithful, vanilla web browser port running original Project I.G.I. assets and gameplay with source code recompiled.


---

## 📌 Status & Future Updates

More reverse engineering projects, tools, file format specifications, and research resources will be updated in the future.

---




## ⚖️ License & Disclaimer

* This repository is licensed under the [MIT License](LICENSE).
* Project I.G.I. and I.G.I.-2 are trademarks and intellectual property of Innerloop studios and This project is unaffiliated with Innerloop Studios, Eidos Interactive, or Codemasters.
