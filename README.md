<div align="center">

# Awesome Project I.G.I.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![Tracked Projects](https://img.shields.io/badge/Tracked%20Projects-25+-brightgreen.svg)]()
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

A curated list of awesome reverse engineering projects, static recompilations, decompilations, source ports, custom level editors, QVM bytecode utilities, file format specifications, and research for the **Project I.G.I.** series (*Project I.G.I.: I'm Going In* and *I.G.I.-2: Covert Strike*) developed by Innerloop Studios.

</div>

---

> [!NOTE]
> This repository hosts no proprietary game code, binaries, or copyrighted assets. All listed projects require a legally owned retail installation of the original games for asset extraction or runtime loading.

---

## Contents

- [Static Binary Recompilation (AOT)](#static-binary-recompilation-aot)
- [Decompilation & Reverse Engineering](#decompilation--reverse-engineering)
- [Engine Reconstructions & Source Ports](#engine-reconstructions--source-ports)
- [Multi-Game & Unified Engines](#multi-game--unified-engines)
- [Console & Handheld Ports](#console--handheld-ports)
- [Desktop Native Ports (macOS & Linux)](#desktop-native-ports-macos--linux)
- [Browser & Web Playable Ports](#browser--web-playable-ports)
- [Level, Mission & Graph Editors](#level-mission--graph-editors)
- [QVM Bytecode & Scripting Tools](#qvm-bytecode--scripting-tools)
- [Asset Converters & File Utilities](#asset-converters--file-utilities)
- [Native Hooking & DLL Injection](#native-hooking--dll-injection)
- [File Formats & Research Specifications](#file-formats--research-specifications)
- [Comparative Benchmarks & Architecture Notes](#comparative-benchmarks--architecture-notes)
- [Contributing](#contributing)
- [License & Disclaimer](#license--disclaimer)

---

## Static Binary Recompilation (AOT)

Ahead-of-Time (AOT) recompilation translates original x86 machine instructions directly into native C/C++ or WebAssembly, producing independent native host binaries with zero emulation overhead.

- **[igi-recomp](https://github.com/HenryKun55/igi-recomp)** `C` `x86-to-C` `macOS` `PS Vita` `PC` — Ahead-of-Time static binary recompilation of retail `IGI.exe` (2000) into portable C. Delivers 100% playable game logic, 60+ FPS uncapped framerates, true widescreen support, Direct3D 7 to modern OpenGL translation, and native Indeo 5 AVI cutscene playback via FFmpeg. By [@HenryKun55](https://github.com/HenryKun55) ([fork](https://github.com/heaven-hm/igi-recomp)).
- **[IGI 2: Covert Strike Web Port](https://github.com/swampodsarkar321/IGI-WEB)** `C` `Wasm` `WebGPU` `macOS` — Static binary recompilation of the retail x86 `igi2.exe` into portable C via Ghidra and custom tooling (31,547 recovered functions, ~1.3 million instructions), compiled to WebAssembly/WebGPU and native macOS Apple Silicon. Features 1v1 online multiplayer with deterministic netplay. Live demo at [iglweb-olive.vercel.app](https://iglweb-olive.vercel.app/). By [@swampodsarkar321](https://github.com/swampodsarkar321).
- **[project-igi-browser (ReComp)](https://github.com/sagarinfosec/project-igi-browser)** `Wasm` `Web` — Recompiled web browser port running original Project I.G.I. assets and gameplay with source logic recompiled. Live demo at [igi.sagarinfosec.site](https://igi.sagarinfosec.site). By [@sagarinfosec](https://github.com/sagarinfosec).

---

## Decompilation & Reverse Engineering

Projects focused on recovering source code, data structures, and disassembled engine routines from original executables.

- **[IGI-RE](https://github.com/slickdaddyy/IGI-RE)** `C` `Ghidra` `Decompilation` — Full reverse engineering and decompilation project targeting the original Project I.G.I. (2000) executable. Focuses on rewriting game functions into clean, human-readable C, recovering file formats, and documenting internal game loops and subsystem logic. By [@slickdaddyy](https://github.com/slickdaddyy) ([fork](https://github.com/heaven-hm/IGI-RE)).
- **[igi2-decomp](https://github.com/ShahriyarB/igi2-decomp)** `C++` `Decompilation` — Reverse engineering and decompilation project targeting the *I.G.I.-2: Covert Strike* executable. Recovers engine data structures, calling conventions, and subsystems. By [@ShahriyarB](https://github.com/ShahriyarB).

---

## Engine Reconstructions & Source Ports

Clean-room engine rewrites and reimplementations reading original game data files directly at runtime.

- **[project-open-igi](https://github.com/heaven-hm/project-open-igi)** `C++20` `Cross-Platform` `OpenGL/Vulkan` — Modern C++20 clean-room engine reconstruction and native source port for Project I.G.I. Features clean architecture, modern CMake/Clang toolchain integration, cross-platform gameplay reproduction, and extensive developer telemetry. By [@heaven-hm](https://github.com/heaven-hm).
- **[re-igi / reimagine-igi](https://github.com/Haseebraza12/reimagine-igi)** `TypeScript` `Three.js` `Vite` — High-fidelity browser-native reimplementation reading retail game files directly at runtime without pre-converting assets. Loads and plays all 14 missions, featuring faithful octree terrain with LOD geomorph and lightmaps, complete 49-state player movement graph, 3-ray character collision, original 4:3 camera optics (90° × 73.74°), vehicle physics, patrol AI, and dynamic sound mixing. By [@Haseebraza12](https://github.com/Haseebraza12).

---

## Multi-Game & Unified Engines

Unified engines engineered to run both *Project I.G.I.: I'm Going In* (2000) and *I.G.I.-2: Covert Strike* (2003) under a single modern runtime.

- **[OpenIGI](https://github.com/OpenIGI/OpenIGI/)** `C#` `.NET 10` `Windows` `macOS` `Linux` `Web` — Clean-room multi-game engine reimplementation in C# on .NET 10. Runs original missions, scripts, and AI from retail installations with a modern renderer, dedicated launcher, and modular modding platform. Available for desktop ([openigi.com](https://openigi.com/)) and browser. By [@ShahriyarB](https://github.com/ShahriyarB).

---

## Console & Handheld Ports

Targeting dedicated gaming consoles and handheld hardware.

- **[IGI Vita](https://github.com/HenryKun55/igi-vita)** `C` `vitaGL` `PS Vita` `PSTV` — Native PlayStation Vita port built from static recompilation. Replaces Direct3D 7, DirectSound, and DirectInput with vitaGL and native Vita OS APIs. Includes hand-tuned ARM assembly routines for terrain, skinning, and culling; locked 30 FPS at 444 MHz; dual-analog stick controls, front touchscreen aiming, rear touchpad scope zoom, and 16:9 widescreen or original 4:3 modes. By [@HenryKun55](https://github.com/HenryKun55).

---

## Desktop Native Ports (macOS & Linux)

Standalone desktop applications running natively on modern UNIX-like operating systems without Wine or Rosetta.

- **[Project I.G.I. macOS Standalone App](https://github.com/rishabhgupta3107/igi-browser)** `WebGPU` `macOS Native` — Native macOS standalone app bundle (`Project IGI.app`) powered by WebGPU. Features widescreen resolution, sharper graphics, gamepad controller support, and dive mechanics without requiring an emulator. Prebuilt downloads for [Apple Silicon M1+ (ARM64)](https://github.com/rishabhgupta3107/igi-browser/releases/latest/download/Project-IGI-Mac-Apple-Chip.zip) and [Intel (x86-64)](https://github.com/rishabhgupta3107/igi-browser/releases/latest/download/Project-IGI-Mac-Intel.zip). By [@rishabhgupta3107](https://github.com/rishabhgupta3107).
- **[OpenIGI Desktop Client](https://openigi.com/)** `macOS` `Linux` `Desktop` — Native desktop client for macOS and Linux with automated terminal installation (`curl -fsSL https://openigi.com/install.sh | bash`) and built-in auto-updater. By [@ShahriyarB](https://github.com/ShahriyarB).

---

## Browser & Web Playable Ports

Playable versions running directly inside web browsers via modern Web APIs (WebAssembly, WebGPU, Web Audio).

- **[re-igi / reimagine-igi](https://github.com/Haseebraza12/reimagine-igi)** `Web Only` — Complete browser-native reimplementation reading retail game files directly at runtime in the client. By [@Haseebraza12](https://github.com/Haseebraza12).
- **[Project I.G.I. Browser Port](https://rishabhgupta3107.github.io/igi-browser/)** `WebGPU` — In-browser port running via WebGPU with widescreen support, high-resolution rendering, and gamepad controls. By [@rishabhgupta3107](https://github.com/rishabhgupta3107).
- **[IGI 2: Covert Strike Web Port](https://iglweb-olive.vercel.app/)** `WebGPU` `WebAssembly` — Playable in-browser port of *I.G.I.-2: Covert Strike* with WebAssembly, Web Audio, and 1v1 online multiplayer. By [@swampodsarkar321](https://github.com/swampodsarkar321).
- **[OpenIGI Web](https://openigi.com/)** `WebGL` — Enhanced browser-based version powered by the OpenIGI engine with modern visuals. By [@ShahriyarB](https://github.com/ShahriyarB).
- **[Project I.G.I. Web (Vanilla)](https://project-igi.pages.dev/)** `Web` — Faithful, vanilla web browser port running original Project I.G.I. assets directly in the browser.
- **[PlayIGI](https://playigi.com/play)** `Mobile Web` — Mobile browser-optimized port playable on iOS Safari and Android browsers.

---

## Level, Mission & Graph Editors

Tooling for inspecting, modifying, and creating levels, missions, AI patrol routes, and world geometry.

- **[project-igi-editor](https://github.com/heaven-hm/project-igi-editor)** `C++` `Qt` `3D Editor` — Professional 3D level editor for Project IGI 1. Inspect level geometry, place objects and items, edit trigger volumes, and construct complex multi-stage missions. By [@heaven-hm](https://github.com/heaven-hm).
- **[project-igi-toolkit](https://github.com/heaven-hm/project-igi-toolkit)** `GUI` `Modding` — All-in-one IGI 1 toolkit capable of editing Maps, AI patrol paths, Graphs, Levels, and Missions. By [@heaven-hm](https://github.com/heaven-hm).
- **[project-igi-studio](https://github.com/heaven-hm/project-igi-studio)** `Mission Designer` — Mission building environment for Project I.G.I. Features a tactical map computer interface, 3D close-up viewport, AI designer, and custom mission script compiler. By [@heaven-hm](https://github.com/heaven-hm).
- **[project-igi-graph-editor](https://github.com/heaven-hm/project-igi-graph-editor)** `AI / Navigation` — Specialized editor for IGI navigation graphs, waypoint networks, and patrol node connections used by NPC AI. By [@heaven-hm](https://github.com/heaven-hm).
- **[project-igi-blender-plugin](https://github.com/heaven-hm/project-igi-blender-plugin)** `Python` `Blender Addon` — Blender integration for importing and exporting Project IGI 3D models, level geometry, and animation hierarchies. By [@heaven-hm](https://github.com/heaven-hm).

---

## QVM Bytecode & Scripting Tools

Editors, assemblers, and decompilers for the Quake / Innerloop Virtual Machine (QVM) bytecode powering mission objectives and AI scripts.

- **[project-igi-qvm-editor-web](https://github.com/heaven-hm/project-igi-qvm-editor-web)** `Web` `IDE` — Online QVM script editor, compiler, and decompiler with syntax highlighting, opcode verification, and live bytecode disassembly. By [@heaven-hm](https://github.com/heaven-hm).
- **[project-igi-qvm-editor](https://github.com/heaven-hm/project-igi-qvm-editor)** `Desktop` `QVM` — Desktop QVM editor and bytecode utility for analyzing and modifying game logic scripts in Project IGI 1 & 2. By [@heaven-hm](https://github.com/heaven-hm).

---

## Asset Converters & File Utilities

Utilities for packing, unpacking, and converting proprietary Innerloop Studios file formats.

- **[project-igi-converter](https://github.com/heaven-hm/project-igi-converter)** `CLI & GUI` `Assets` — Universal asset converter for Project IGI 1 and IGI 2 supporting 2D textures, 3D meshes (TLW/OPT), sound archives, and binary configuration files. By [@heaven-hm](https://github.com/heaven-hm).

---

## Native Hooking & DLL Injection

Runtime hooking, memory injection, and symbol introspection for the retail PC executables.

- **[project-igi-natives](https://github.com/heaven-hm/project-igi-natives)** `C++` `DLL Injection` — Intercepts and exposes internal native engine methods in retail `IGI.exe` at runtime via DLL injection, mapping game symbols and internal APIs for modding and instrumentation. By [@heaven-hm](https://github.com/heaven-hm).
- **[project-igi-injector](https://github.com/heaven-hm/project-igi-injector)** `GUI` `Injector` — Dedicated GUI DLL injector for launching and injecting custom mods, diagnostic tools, and hooks into Project I.G.I. By [@heaven-hm](https://github.com/heaven-hm).

---

## File Formats & Research Specifications

Documentation and technical research dissecting Innerloop Studios' proprietary engine formats.

- **[project-igi-research](https://github.com/heaven-hm/project-igi-research)** `Documentation` `Specs` — Comprehensive repository of reverse engineering research, file format breakdowns (RES, DAT, TLW, OPT, QVM), memory layouts, and protocol notes for educational preservation. By [@heaven-hm](https://github.com/heaven-hm).

---

## Comparative Benchmarks & Architecture Notes

- **[IGI 1 Web Ports Technical Comparison](IGI_1_WEB_PORTS_COMPARISON.md)** — In-depth architectural comparison, technical trade-offs, and feature ratings across all browser and web-based implementations.

---

## Contributing

Contributions are warmly welcomed! Please read the [Contribution Guidelines](CONTRIBUTING.md) for details on how to propose new projects, tools, or research papers.

---

## License & Disclaimer

- This repository is licensed under the [MIT License](LICENSE).
- *Project I.G.I.* and *I.G.I.-2: Covert Strike* are trademarks and intellectual property of Innerloop Studios, Eidos Interactive, and Codemasters. This curated directory is an independent community effort and is completely unaffiliated with the original developers or publishers.
