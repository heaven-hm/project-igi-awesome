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

> ## 🌟 Featured Projects
>
> ### 🎮 **[PlayIGI](https://playigi.com/)** (By Neonix Team) • [Play In Browser](https://playigi.com/play)
>
> **PlayIGI** is a massive, full-featured **Project I.G.I. 1 Reimplementation** by the **Neonix Team** featuring:
> - 🚀 **High Uncapped FPS & Smooth Gameplay** — Modern high-tick engine loop with zero stutter.
> - 💾 **In-Game Save System** — Save and resume your mission progress anytime.
> - 🎨 **Enhanced HD Textures** — Crisp, high-resolution remastering of classic terrain and weapon textures.
> - 📱 **Cross-Platform Availability** — Fully playable on **Windows PC**, desktop **Web Browsers**, and **Mobile Web Browsers (iOS Safari & Android)** with responsive touch controls!
>
> ---
>
> ### ⚡ **[OpenIGI](https://openigi.com/)** (Remastered Version by ShahriyarB) • [GitHub Repository](https://github.com/OpenIGI/OpenIGI)
>
> **OpenIGI** is a state-of-the-art **Multi-Game Remastered Engine** built in C# on .NET 10 featuring:
> - 🎯 **Dual-Game Support** — Re-engineers and plays both *Project I.G.I.: I'm Going In* (2000) and *I.G.I.-2: Covert Strike* (2003).
> - 🌟 **Modern Remastered Visuals** — Modernized graphics pipeline with true widescreen, ultra-high resolutions, and dynamic lighting.
> - 🖥️ **Native Desktop & Web Delivery** — Native client for Windows, macOS, and Linux desktop (`curl -fsSL https://openigi.com/install.sh | bash`) plus in-browser Web play.
> - 🛠️ **Integrated Modding Platform** — Built-in custom launcher, automatic updaters, and modular modding architecture.

---

## Contents

- [Reimplementation](#reimplementation)
- [Remastered](#remastered)
- [Recomp](#recomp)
- [Decomp](#decomp)
- [Hybrid](#hybrid)
- [Web](#web)
- [PC](#pc)
- [Android / iOS Mobile](#android--ios-mobile)
- [Contributing](#contributing)
- [License & Disclaimer](#license--disclaimer)

---

## Reimplementation

Clean-room engine rewrites recreating the game engine from scratch while reading original retail game data files directly at runtime.

- **[PlayIGI](https://playigi.com/)** `Windows` `Web` `Mobile (iOS & Android)` — Full IGI 1 Reimplementation by the Neonix Team with high FPS, Save Game system, HD textures, and smooth gameplay across Windows PC, modern Web browsers, and Mobile Web browsers (iOS Safari & Android). ([Play Online](https://playigi.com/play)).
- **[re-igi / reimagine-igi](https://github.com/Haseebraza12/reimagine-igi)** `TypeScript` `Three.js` `Vite` — Browser-native reimplementation in TypeScript & Three.js reading retail game files directly at runtime without pre-converting assets. Loads all 14 missions, octree terrain with LOD geomorph, 49-state player movement graph, 3-ray character collision, 4:3 camera optics, vehicle physics, and patrol AI. By [@Haseebraza12](https://github.com/Haseebraza12).

---

## Remastered

Projects providing enhanced visual fidelity, modern textures, updated lighting, and quality-of-life upgrades.

- **[OpenIGI](https://openigi.com/)** `C#` `.NET 10` `Multi-Game` `Remaster` — Clean-room multi-game engine reimplementation and remaster supporting both *Project I.G.I.: I'm Going In* (2000) and *I.G.I.-2: Covert Strike* (2003) from retail game files with a modern renderer, widescreen, high resolutions, dedicated launcher, and modular modding platform. Available for Windows, macOS, Linux, and Web. By [@ShahriyarB](https://github.com/ShahriyarB) ([repo](https://github.com/OpenIGI/OpenIGI)).

---

## Recomp

Ahead-of-Time (AOT) static binary recompilations translating original compiled x86 machine instructions into native C/C++ or WebAssembly source code.

- **[igi-recomp](https://github.com/HenryKun55/igi-recomp)** `C` `x86-to-C` `AOT` — Ahead-of-Time static binary recompilation of retail `IGI.exe` (2000) into portable C. 100% playable game logic, uncapped 60+ FPS, widescreen FOV, Direct3D 7 to OpenGL, and FFmpeg video playback. Runs on macOS (Apple Silicon ARM64), PS Vita, and PC. By [@HenryKun55](https://github.com/HenryKun55).
- **[IGI 2: Covert Strike Web Recomp](https://iglweb-olive.vercel.app/)** `C` `AOT` `WebGPU` `Multiplayer` — Static binary recompilation of retail x86 `igi2.exe` into portable C via Ghidra and custom tooling (31,547 recovered functions, ~1.3M instructions), targeting WebGPU (with 1v1 online multiplayer) and macOS ARM64. By [@swampodsarkar321](https://github.com/swampodsarkar321) ([repo](https://github.com/swampodsarkar321/IGI-WEB)).
- **[project-igi-browser (ReComp)](https://github.com/sagarinfosec/project-igi-browser)** `Wasm` `AOT` — Static binary recompiled web browser port running Project I.G.I. with recompiled source logic ([demo](https://igi.sagarinfosec.site)). By [@sagarinfosec](https://github.com/sagarinfosec).

---

## Decomp

Projects focused on source code recovery, Ghidra decompilation, and function-by-function matching against the original retail binary.

- **[IGI-RE](https://github.com/slickdaddyy/IGI-RE)** `C` `Ghidra` `1:1 Matching` — Decompilation and reverse engineering project targeting retail `IGI.exe` (2000), rewriting game functions into clean, human-readable C with structure recovery and game loop analysis. By [@slickdaddyy](https://github.com/slickdaddyy).
- **[igi2-decomp](https://github.com/ShahriyarB/igi2-decomp)** `C++` `Decompilation` — Reverse engineering and decompilation project targeting the *I.G.I.-2: Covert Strike* executable. Focuses on data structure recovery, calling conventions, and engine subsystems. By [@ShahriyarB](https://github.com/ShahriyarB).

---

## Hybrid

Projects combining multiple techniques (such as static recompilation paired with custom ARM assembly kernels, or native wrappers over Web pipelines).

- **[IGI Vita](https://github.com/HenryKun55/igi-vita)** `C` `ARM Assembly` `vitaGL` `Handheld` — Hybrid native PlayStation Vita / PSTV port combining static recompilation with hand-tuned ARM assembly routines for terrain, skinning, and culling. Locked 30 FPS at 444 MHz, dual-analog stick controls, front touchscreen aiming, rear touchpad scope zoom, and widescreen options. By [@HenryKun55](https://github.com/HenryKun55).

---

## Web

Playable browser ports and standalone web distributions running via WebGPU and WebAssembly.

- **[Project I.G.I. Browser Port](https://rishabhgupta3107.github.io/igi-browser/)** `WebGPU` `In-Browser` — Playable browser port running via WebGPU with widescreen support, high-resolution rendering, gamepad controller support, and dive mechanics. By [@rishabhgupta3107](https://github.com/rishabhgupta3107).
- **[Project I.G.I. Web (Vanilla)](https://project-igi.pages.dev/)** `Vanilla` `Web` — Faithful, vanilla web browser port running original Project I.G.I. assets directly in the browser.

---

## PC

Standalone native desktop applications and packages for macOS and Windows.

- **[Project I.G.I. macOS Standalone App](https://github.com/rishabhgupta3107/igi-browser)** `macOS Apple Silicon` `macOS Intel` — Native macOS standalone app bundle (`Project IGI.app`) powered by WebGPU with gamepad controller support. Prebuilt downloads for [Apple Silicon M1+ (ARM64)](https://github.com/rishabhgupta3107/igi-browser/releases/latest/download/Project-IGI-Mac-Apple-Chip.zip) and [Intel (x86-64)](https://github.com/rishabhgupta3107/igi-browser/releases/latest/download/Project-IGI-Mac-Intel.zip). By [@rishabhgupta3107](https://github.com/rishabhgupta3107).

---

## Android / iOS Mobile

Mobile-ready ports and touch-optimized implementations designed for smartphones and tablets.

- Mobile gameplay (iOS Safari and Android web browsers with touch-screen controls) is provided directly through **[PlayIGI](https://playigi.com/play)** (see details under [Reimplementation](#reimplementation)).

---

## Contributing

Contributions are warmly welcomed! Please read the [Contribution Guidelines](CONTRIBUTING.md) for details on proposing new ports, decompilations, recompilations, or remasters.

---

## License & Disclaimer

- This repository is licensed under the [MIT License](LICENSE).
- *Project I.G.I.* and *I.G.I.-2: Covert Strike* are trademarks and intellectual property of Innerloop Studios, Eidos Interactive, and Codemasters. This curated directory is an independent community effort and is completely unaffiliated with the original developers or publishers.
