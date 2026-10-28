# Project I.G.I. Reverse Engineering & Source Ports

A curated directory of open-source reverse engineering, decompilation, static recompilation, engine reconstruction, console/mobile ports, and browser playable projects for the **Project I.G.I.** series developed by Innerloop Studios.

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

## 🕹️ Console, Handheld & Mobile Ports

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

### [Project I.G.I. CPU Port & Android Universal APK](https://github.com/beraslarang544-sketch/BerasXcorps/tree/fb9946e443405fcd5a6d1cd1fefd16ff47e39bd1/igi-cpu-port)
* **Repository Tree:** [BerasXcorps/igi-cpu-port](https://github.com/beraslarang544-sketch/BerasXcorps/tree/fb9946e443405fcd5a6d1cd1fefd16ff47e39bd1/igi-cpu-port)
* **Author:** [@beraslarang544-sketch](https://github.com/beraslarang544-sketch) / BerasXcorps
* **Target Game:** *Project I.G.I.: I'm Going In* (2000)
* **Platform:** Android 7.0 – Android 15+ (`arm64-v8a` and `x86_64`)
* **Ready-to-Install APK:** [`ProjectIGI-CPU-Port-v0.6.0-universal.apk`](https://github.com/beraslarang544-sketch/BerasXcorps/blob/fb9946e443405fcd5a6d1cd1fefd16ff47e39bd1/igi-cpu-port/releases/ProjectIGI-CPU-Port-v0.6.0-universal.apk)
* **Approach:** Static recompilation of retail `IGI.exe` (`x86` PE32 → `C11`, 5,712 recovered functions) paired with a pure CPU-based Direct3D 7 software rasterizer with zero GPU/OpenGL/Vulkan hardware acceleration dependency (`android:hardwareAccelerated="false"`).
* **Features:**
  - Universal dual-ABI Android native libraries (`libigi_cpu_port.so` for `arm64-v8a` and `x86_64`) built against Bionic NDK with 16 KB page alignment for Android 15+.
  - Pure CPU Direct3D 7 software 3D rasterizer with perspective-correct texture mapping, 32-bit float Z-buffer, Gouraud vertex shading, alpha blending, and linear distance fog.
  - Mission 01 ("Trainyard") compound entities, terrain elevation (`terrain.hmp` 128×128), and textures directly embedded for zero external storage permission requirement.
  - Interactive touch HUD with virtual movement D-Pad (left) and drag-to-look camera rotation (right).
  - Dual signature scheme passing Android v1 (JAR PKCS#7) and v2 (`APK Sig Block 42`) verification.

---

## 🌐 Multi-Game / Unified Engines (IGI 1 & IGI 2)

### [OpenIGI (Clean-Room Engine Reimplementation)](https://github.com/OpenIGI/OpenIGI/)
* **Repository:** [https://github.com/OpenIGI/OpenIGI/](https://github.com/OpenIGI/OpenIGI/)
* **Author:** [@ShahriyarB](https://github.com/ShahriyarB)
* **Approach:** Clean-room reimplementation of Innerloop Studios' engine in C# on .NET 10.
* **Description:** An open-source engine for *Project I.G.I.: I'm Going In* (2000) and *I.G.I. 2: Covert Strike* (2003). Runs the original games from your own retail installation. The original missions, scripts, and AI play as they did in 2000, with a modern renderer, launcher, and modding platform built around them.

---

## 🌍 Browser Playable Ports & Web Implementations

Directly playable browser-based implementations and web ports:

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
