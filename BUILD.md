# Build Instructions – Micromouse STM32F411 Template

This repository is a **reference template** for STM32 projects.  
New members can use it as a starting point or as a guide for making their own STM32Cube projects.  
It is not meant to be the main development repo, but a **template** showing structure and basic files.

---

## 1. Build with STM32CubeIDE (Beginner-Friendly)

1. Open **STM32CubeIDE**.  
2. Go to **File → Open Projects from File System…**  
3. Select this repository’s folder.  
4. Open the `.ioc` file (**Micromouse.ioc**) to view or modify pin configuration.  
   - CubeIDE will generate/update the code inside `Core/` and `Drivers/`.  
5. Build the project: **Project → Build Project**.  
6. Flash to the board: **Run → Debug** (green “play” button).  

---

## 2. Build with VS Code + CMake + OpenOCD (Advanced)

### Requirements
- [ARM GNU Toolchain](https://developer.arm.com/downloads/-/gnu-rm)  
- [CMake](https://cmake.org/download/)  
- [Ninja](https://ninja-build.org/)  
- [OpenOCD](https://openocd.org/) or ST-Link Utility  
- VS Code Extensions:
  - **CMake Tools**
  - **Cortex-Debug**
  - **C/C++**

### Steps
```bash
# Clone the repo
git clone https://github.com/CSULB-EATS/micromouse_25-26.git
cd micromouse_25-26

# Configure build
cmake --preset=default

# Compile
cmake --build --preset=default
```

The compiled firmware (`firmware.elf`) will be inside the `build/` directory.

### Flash to board
```bash
openocd -f interface/stlink.cfg -f target/stm32f4x.cfg   -c "program build/firmware.elf verify reset exit"
```

---

## 3. Repo Structure
```
Core/                   → Cube-generated user code (main.c, system_init, etc.)
Drivers/                → STM32 HAL drivers
examples/               → Example/test source files
startup_stm32f411xe.s   → Cortex-M startup assembly
STM32F411XX_FLASH.ld    → Linker script
Micromouse.ioc          → CubeMX configuration file
.vscode/                → VS Code build/debug tasks
CMakePresets.json       → Build presets for CMake
README.md               → Project notes
```

---

## Notes
- Repo is **review-protected**: no one can merge changes without approval.  
- Treat this repo as a **template/reference format**, not as a project where everyone commits directly.  
- If changes are needed, request review (Yshi or Robert can check).  
- Most members will make their own STM32Cube projects based on this format.  

---
