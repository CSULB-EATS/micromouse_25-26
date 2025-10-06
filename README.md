# 🐭 CSULB Micromouse – Quick Setup (Reference Repo)

Welcome to the **Micromouse setup repository!**  
This repository is meant to serve as a **reference hub** for all CSULB Micromouse teams working with the **STM32Cube platform**.  
You’ll find example projects, configuration files, and build instructions to help you get started quickly.

---

## 📢 Important Notice

**Do not clone this repository directly to make edits.**  
Instead, **fork** it to your own GitHub account if you want to experiment or build on top of it.  

> The main organization repo is for **reference only** — no changes should be pushed here.

If you just want to browse or copy code snippets, cloning or downloading is fine.  
But for active development, **each team should maintain its own fork or private repo** based on this template.

---

## 🧭 What’s Inside

This repository includes reference materials and example setups for:
- **STM32CubeIDE** project templates  
- **Example code** and older team projects  
- **Peripheral setup samples** (ADC, PWM, UART, timers, sensors, and motors)  
- **Pin configuration examples** (`.ioc` files)  
- **Starter code for motion control and maze solving**

These examples are meant to help your team **understand structure and best practices** for STM32-based Micromouse development.

---

## 🧰 Tools Required

- ![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)  
  [Download Git](https://git-scm.com/downloads)
  ```bash
  git --version
  ```

- ![STM32CubeIDE](https://img.shields.io/badge/STM32CubeIDE-03234B?style=flat&logo=stmicroelectronics&logoColor=white)  
  [Download STM32CubeIDE](https://www.st.com/en/development-tools/stm32cubeide.html)  
  → Main tool for compiling, flashing, and debugging.

- ![ST-Link](https://img.shields.io/badge/ST--Link-03234B?style=flat&logo=stmicroelectronics&logoColor=white)  
  [Install ST-Link drivers](https://www.st.com/en/development-tools/st-link-v2.html) *(Windows users only)*

*(Optional)*  
- ![VS Code](https://img.shields.io/badge/VS%20Code-007ACC?style=flat&logo=visualstudiocode&logoColor=white)  
  Use for code editing only. STM32CubeIDE handles all builds and flashing.

---

## 🪜 How to Use This Repo (Per Team)

### 1. Fork the Repository
Click **“Fork”** at the top right of this page.  
This creates your own copy under your GitHub account — your team can edit and push freely there.

### 2. Clone *Your Fork* Locally
After forking, clone your personal copy:
```bash
git clone https://github.com/<your-username>/micromouse-setup.git
cd micromouse-setup
```

### 3. Import into STM32CubeIDE
1. Open STM32CubeIDE  
2. Go to `File > Open Projects from File System...`  
3. Select your local folder  
4. Build with the **hammer icon**  
5. Flash using the **green bug icon**

---

## 📂 Files You May Need

Depending on your team’s setup, you may find these files useful:
- `*.ioc` — STM32Cube configuration files  
- `/Core/Src/main.c` — Example main firmware  
- `/Drivers` — HAL and BSP driver examples  
- `/README_TEMPLATES/` — Example formatting for documentation  

> Each team can decide its own **project structure standards** based on comfort level and workflow.

---

## 🧩 Development Notes

- Languages: ![C](https://img.shields.io/badge/C-00599C?style=flat&logo=c&logoColor=white)  
- Format on Save for cleaner commits  
- Keep `main` clean — work only in your team repo or fork  
- Reference examples here, but write your own code for your actual mouse

---

## 📝 Summary

✅ Use this repo for **reference and templates**  
✅ Fork it for your team’s own workspace  
✅ Follow STM32CubeIDE setup instructions  
✅ Each team maintains its **own standards and structure**

---

© 2025 CSULB EATS Micromouse – Educational reference only.
