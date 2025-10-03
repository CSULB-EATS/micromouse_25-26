# 🐭 CSULB Micromouse – Setup  

Welcome to our **setup repository** for Micromouse development!  
This repo gives new members a starting point with **STM32CubeIDE** or **VS Code** for embedded projects.  

---

## Installing Prerequisites  

### Tools
- ![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)  
  Install from [git-scm.com](https://git-scm.com/downloads).  
  Check install:  
  ```bash
  git --version
  ```

- ![STM32CubeIDE](https://img.shields.io/badge/STM32CubeIDE-03234B?style=flat&logo=stmicroelectronics&logoColor=white)  
  Download from [ST’s website](https://www.st.com/en/development-tools/stm32cubeide.html).  
  This is the **main IDE** we use for STM32 boards.  

- ![Visual Studio Code](https://img.shields.io/badge/VS%20Code-007ACC?style=flat&logo=visualstudiocode&logoColor=white) *(optional but recommend)*  
  Extensions to install:  
  - C/C++ (Microsoft)  
  - Cortex-Debug  
  - GitLens (optional, for Git history)  

- ![ST-Link](https://img.shields.io/badge/ST--Link-03234B?style=flat&logo=stmicroelectronics&logoColor=white)  
  **Windows only**: install [ST-Link drivers](https://www.st.com/en/development-tools/st-link-v2.html) to flash/debug.  

---

## 📂 Cloning the Repo  

```bash
git clone https://github.com/csulb-eats/micromouse-setup.git
cd micromouse-setup
```

---

## Build & Flash

### 🔹 STM32CubeIDE  
1. Open **STM32CubeIDE**  
2. Import the project:  
   - `File > Open Projects from File System...`  
   - Select this folder  
3. Click ** Build**  
4. Connect your board and click **Debug** to flash  

### 🔹 VS Code  
- Open the folder in **VS Code**  
- VS Code is only an editor → you’ll need a toolchain & debugger installed.  
- Options:  
  - Use **STM32CubeIDE build** in the background (import Cube-generated Makefiles).  
  - Install **PlatformIO** (auto handles compiler + flashing).  
  - Advanced: set up **arm-none-eabi-gcc** + **OpenOCD** manually.  
  - Use the `.vscode/launch.json` (included) to debug with the Cortex-Debug extension.  

---

## Debugging  

- **STM32CubeIDE** → Use the green “bug” button  
- **VS Code** → Cortex-Debug extension  
- Make sure your **ST-Link** is connected and recognized  

---

## Developing  

- Languages: ![C](https://img.shields.io/badge/C-00599C?style=flat&logo=c&logoColor=white) ![Embedded C](https://img.shields.io/badge/Embedded%20C-orange?style=flat)  
- Recommended: enable **Format on Save** in your IDE for clean code.
- ## 🌱 Git Workflow  

To keep our main branch clean, **always work on your own sub-branch**.  

### Example: Create and push your sub-branch  
```bash
# Make sure you are on the latest main branch
git checkout main
git pull origin main

# Create your own sub-branch (replace 'bex-spi' with your name/feature)
git checkout -b bex-spi

# Work on your changes
git add .
git commit -m "Implement SPI driver"

# Push your sub-branch to the repo
git push origin bex-spi
```
---

## 📝 Notes  

- You can use either **STM32CubeIDE** or **VS Code** → both are valid.  
- Flashing steps vary per IDE/toolchain, but code stays the same.  
- This repo = **starter setup** → real applications will live in their own repos.  

