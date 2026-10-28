<div align="center">

# Awesome Project I.G.I.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![Tracked Projects](https://img.shields.io/badge/Tracked%20Projects-15+-brightgreen.svg)]()
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

A curated directory of awesome reverse engineering (RE), static recompilations, decompilations, source ports, reimplementations, and remasters for the **Project I.G.I.** series (*Project I.G.I.: I'm Going In* and *I.G.I.-2: Covert Strike*) developed by Innerloop Studios.

</div>

---

> [!NOTE]
> This repository hosts no proprietary game code, binaries, or copyrighted assets. All listed projects require a legally owned retail installation of the original games for asset extraction or runtime verification.

---

> ## 🌟 Featured: PlayIGI (By Neonix Team)
>
> ### **[PlayIGI](https://playigi.com/)** • [Play In Browser](https://playigi.com/play)
>
> **PlayIGI** is a massive, full-featured **Project I.G.I. 1 Reimplementation** by the **Neonix Team** featuring:
> - 🚀 **High Uncapped FPS & Smooth Gameplay** — Modern high-tick engine loop with zero stutter.
> - 💾 **In-Game Save System** — Save and resume your mission progress anytime.
> - 🎨 **Enhanced HD Textures** — Crisp, high-resolution remastering of classic terrain and weapon textures.
> - 📱 **Cross-Platform Availability** — Fully playable on **Windows PC**, desktop **Web Browsers**, and **Mobile Web Browsers (iOS Safari & Android)** with responsive touch controls!

---

## Contents

- [Web](#web)
- [Android / iOS Mobile](#android--ios-mobile)
- [PC](#pc)
- [Recomp](#recomp)
- [Decomp](#decomp)
- [Hybrid](#hybrid)
- [Reimplementation](#reimplementation)
- [Remastered](#remastered)
- [Contributing](#contributing)
- [License & Disclaimer](#license--disclaimer)

---

## Web

Playable ports and browser-native reimplementations running inside web browsers via WebAssembly, WebGPU, WebGL, and Web Audio.

- **[PlayIGI Web](https://playigi.com/play)** `Web` `WebGL` `Mobile Friendly` — Full-featured in-browser reimplementation by the Neonix Team with smooth high-FPS gameplay, save game functionality, HD textures, and responsive controls across desktop and mobile browsers.
- **[re-igi / reimagine-igi](https://github.com/Haseebraza12/reimagine-igi)** `TypeScript` `Three.js` `Vite` — Browser-native reimplementation reading retail game files directly at runtime without pre-converting assets. Loads and plays all 14 missions with octree terrain LOD geomorph, 49-state player movement graph, 3-ray character collision, 4:3 camera optics, vehicle physics, and patrol AI. By [@Haseebraza12](https://github.com/Haseebraza12).
- **[Project I.G.I. Browser Port](https://rishabhgupta3107.github.io/igi-browser/)** `WebGPU` `In-Browser` — Playable browser port running via WebGPU with widescreen support, high-resolution rendering, gamepad controller support, and dive mechanics. By [@rishabhgupta3107](https://github.com/rishabhgupta3107).
- **[IGI 2: Covert Strike Web Port](https://iglweb-olive.vercel.app/)** `WebAssembly` `WebGPU` `Multiplayer` — In-browser port of *I.G.I.-2: Covert Strike* translated to WebAssembly and WebGPU with 1v1 online deterministic lockstep multiplayer. By [@swampodsarkar321](https://github.com/swampodsarkar321) ([repo](https://github.com/swampodsarkar321/IGI-WEB)).
- **[OpenIGI Web](https://openigi.com/)** `WebGL` `WebRuntime` — Browser-based version powered by the OpenIGI engine with modernized visuals and web rendering. By [@ShahriyarB](https://github.com/ShahriyarB).
- **[Project I.G.I. Web (Vanilla)](https://project-igi.pages.dev/)** `Vanilla` `Web` — Faithful, vanilla web browser port running original Project I.G.I. assets directly in the browser.
- **[project-igi-browser (ReComp)](https://github.com/sagarinfosec/project-igi-browser)** `Wasm` `Recompiled` — Recompiled web browser port running original Project I.G.I. assets and gameplay with recompiled source code ([demo](https://igi.sagarinfosec.site)). By [@sagarinfosec](https://github.com/sagarinfosec).

---

## Android / iOS Mobile

Mobile-ready ports and touch-optimized implementations designed for smartphones and tablets.

- **[PlayIGI Mobile](https://playigi.com/play)** `iOS Safari` `Android Browser` `Touch UI` — Mobile browser reimplementation by the Neonix Team designed specifically for iOS Safari and Android browsers. Features touch-screen controls, smooth performance, save game states, and HD graphics without requiring any app store install.

---

## PC

Native desktop distributions and source ports for Windows, macOS, and Linux without emulation.

- **[PlayIGI Windows](https://playigi.com/)** `Windows` `Native` — Standalone native Windows PC release by the Neonix Team featuring high FPS, save games, HD texture packs, and ultra-smooth keyboard/mouse controls.
- **[igi-recomp macOS & PC](https://github.com/HenryKun55/igi-recomp)** `macOS ARM64` `Windows` `Linux` — Native desktop executables produced via Ahead-of-Time static recompilation with uncapped 60+ FPS, true widescreen, Direct3D 7 to OpenGL translation, and native Indeo 5 AVI cutscene playback. By [@HenryKun55](https://github.com/HenryKun55).
- **[Project I.G.I. macOS Standalone App](https://github.com/rishabhgupta3107/igi-browser)** `macOS Apple Silicon` `macOS Intel` — Native macOS standalone app bundle (`Project IGI.app`) powered by WebGPU with gamepad controller support. Prebuilt downloads for [Apple Silicon M1+ (ARM64)](https://github.com/rishabhgupta3107/igi-browser/releases/latest/download/Project-IGI-Mac-Apple-Chip.zip) and [Intel (x86-64)](https://github.com/rishabhgupta3107/igi-browser/releases/latest/download/Project-IGI-Mac-Intel.zip). By [@rishabhgupta3107](https://github.com/rishabhgupta3107).
- **[OpenIGI Desktop Client](https://openigi.com/)** `Windows` `macOS` `Linux` — Multi-game desktop client for Windows, macOS, and Linux with automated terminal installation (`curl -fsSL https://openigi.com/install.sh | bash`) and built-in auto-updater. By [@ShahriyarB](https://github.com/ShahriyarB).
- **[IGI 2: Covert Strike Native macOS](https://github.com/swampodsarkar321/IGI-WEB)** `macOS Apple Silicon` — Native macOS Apple Silicon build of *I.G.I.-2: Covert Strike* compiled via Clang from recompiled C source. By [@swampodsarkar321](https://github.com/swampodsarkar321).

---

## Recomp

Ahead-of-Time (AOT) static binary recompilations translating original compiled x86 machine instructions into native C/C++ source code.

- **[igi-recomp](https://github.com/HenryKun55/igi-recomp)** `C` `x86-to-C` `AOT` — Ahead-of-Time static binary recompilation of retail `IGI.exe` (2000) into portable C. 100% playable game logic, uncapped 60+ FPS, widescreen FOV, Direct3D 7 to OpenGL, and FFmpeg video playback. Runs on macOS (Apple Silicon ARM64), PS Vita, and PC. By [@HenryKun55](https://github.com/HenryKun55).
- **[IGI 2: Covert Strike Web Recomp](https://github.com/swampodsarkar321/IGI-WEB)** `C` `AOT` `Ghidra` — Static binary recompilation of retail x86 `igi2.exe` into portable C via Ghidra and custom tooling (31,547 recovered functions, ~1.3M instructions), targeting WebGPU and macOS ARM64. By [@swampodsarkar321](https://github.com/swampodsarkar321).
- **[project-igi-browser (ReComp)](https://github.com/sagarinfosec/project-igi-browser)** `Wasm` `AOT` — Static binary recompiled web browser port running Project I.G.I. with recompiled source logic. By [@sagarinfosec](https://github.com/sagarinfosec).

---

## Decomp

Projects focused on source code recovery, Ghidra decompilation, and function-by-function matching against the original binary.

- **[IGI-RE](https://github.com/slickdaddyy/IGI-RE)** `C` `Ghidra` `1:1 Matching` — Decompilation and reverse engineering project targeting retail `IGI.exe` (2000), rewriting game functions into clean, human-readable C with structure recovery and game loop analysis. By [@slickdaddyy](https://github.com/slickdaddyy).
- **[igi2-decomp](https://github.com/ShahriyarB/igi2-decomp)** `C++` `Decompilation` — Reverse engineering and decompilation project targeting the *I.G.I.-2: Covert Strike* executable. Focuses on data structure recovery, calling conventions, and engine subsystems. By [@ShahriyarB](https://github.com/ShahriyarB).

---

## Hybrid

Projects combining multiple techniques (such as static recompilation with custom assembly kernels, or native desktop wrappers around web rendering pipelines).

- **[IGI Vita](https://github.com/HenryKun55/igi-vita)** `C` `ARM Assembly` `vitaGL` `Handheld` — Hybrid native PlayStation Vita / PSTV port combining static recompilation with hand-tuned ARM assembly routines for terrain, skinning, and culling. Locked 30 FPS at 444 MHz, dual-analog stick controls, front touchscreen aiming, rear touchpad scope zoom, and widescreen options. By [@HenryKun55](https://github.com/HenryKun55).
- **[Project I.G.I. WebGPU Hybrid Port](https://github.com/rishabhgupta3107/igi-browser)** `WebGPU` `Native Wrapper` — Hybrid architecture running a high-performance WebGPU rendering pipeline packaged into standalone native desktop apps for macOS and Windows. By [@rishabhgupta3107](https://github.com/rishabhgupta3107).

---

## Reimplementation

Clean-room engine rewrites recreating the game engine from scratch while reading original retail game data files directly.

- **[PlayIGI](https://playigi.com/)** `Windows` `Web` `Mobile` — Massive IGI 1 reimplementation by the Neonix Team with high FPS, save games, HD textures, and smooth gameplay across PC and browsers.
- **[re-igi / reimagine-igi](https://github.com/Haseebraza12/reimagine-igi)** `TypeScript` `Three.js` `Vite` — Browser-native reimplementation reading retail game files directly at runtime without pre-converting assets. Loads all 14 missions, octree terrain with LOD geomorph, 49-state player movement graph, 3-ray character collision, 4:3 camera optics, vehicle physics, and patrol AI. By [@Haseebraza12](https://github.com/Haseebraza12).
- **[OpenIGI](https://github.com/OpenIGI/OpenIGI/)** `C#` `.NET 10` `Multi-Game` — Clean-room engine reimplementation supporting both *Project I.G.I.: I'm Going In* (2000) and *I.G.I.-2: Covert Strike* (2003) from retail game files with a modern renderer, launcher, and modding platform. By [@ShahriyarB](https://github.com/ShahriyarB).

---

## Remastered

Projects providing enhanced visual fidelity, modern textures, lighting improvements, and quality-of-life upgrades.

- **[PlayIGI HD Remaster](https://playigi.com/)** `HD Textures` `High FPS` `QoL` — Remastered experience by the Neonix Team featuring enhanced HD terrain and weapon textures, high uncapped FPS, smooth modern mouse/touch responsiveness, and an integrated save game system.
- **[OpenIGI Enhanced](https://openigi.com/)** `Modern Renderer` `High Res` — Modernized presentation of both IGI 1 and IGI 2 with enhanced rendering, widescreen support, high resolutions, and an active modding foundation. By [@ShahriyarB](https://github.com/ShahriyarB).

---

## Contributing

Contributions are warmly welcomed! Please read the [Contribution Guidelines](CONTRIBUTING.md) for details on proposing new ports, decompilations, recompilations, or remasters.

---

## License & Disclaimer

- This repository is licensed under the [MIT License](LICENSE).
- *Project I.G.I.* and *I.G.I.-2: Covert Strike* are trademarks and intellectual property of Innerloop Studios, Eidos Interactive, and Codemasters. This curated directory is an independent community effort and is completely unaffiliated with the original developers or publishers.
