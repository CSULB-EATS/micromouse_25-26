# 🐭 CSULB Micromouse – Quick Setup  

Welcome to our **Micromouse setup repository!**  
This repo is designed to help new members quickly build and flash STM32 projects with **STM32CubeIDE**.  

---

## Prerequisites  

### Tools  

- ![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)  
  [Download Git](https://git-scm.com/downloads)  
  ```bash
  git --version
  ```

- ![STM32CubeIDE](https://img.shields.io/badge/STM32CubeIDE-03234B?style=flat&logo=stmicroelectronics&logoColor=white)  
  [Download STM32CubeIDE](https://www.st.com/en/development-tools/stm32cubeide.html)  
  → This is the **main tool** for compiling, flashing, and debugging.  

- ![ST-Link](https://img.shields.io/badge/ST--Link-03234B?style=flat&logo=stmicroelectronics&logoColor=white)  
  [Install ST-Link drivers](https://www.st.com/en/development-tools/st-link-v2.html) *(Windows users only)*  

*(Optional)*  
- ![VS Code](https://img.shields.io/badge/VS%20Code-007ACC?style=flat&logo=visualstudiocode&logoColor=white)  
  Can be used for code editing only. No flashing required from here.

---

## 📂 Cloning the Repo  

```bash
git clone https://github.com/csulb-eats/micromouse-setup.git
cd micromouse-setup
```

---

## ⚙️ Build & Flash (Simple Method)  

### 🔹 STM32CubeIDE Steps  

1. **Open STM32CubeIDE**  
2. Go to `File > Open Projects from File System...`  
3. Select this repo folder and import the project  
4. Click the **hammer icon 🛠️ (Build)** to compile  
5. Connect your STM32 board via USB  
6. Click the **green bug (Debug)** to flash and run  

> That’s it! The IDE automatically handles toolchain, compiler, and flashing.  

---

## 🧩 Development Notes  

- Languages: ![C](https://img.shields.io/badge/C-00599C?style=flat&logo=c&logoColor=white)  
- Use **Format on Save** for cleaner code.  
- Keep your **main branch clean** — always make your own feature branch:  

```bash
git checkout -b yourname-feature
git add .
git commit -m "Added motor setup"
git push origin yourname-feature
```

---

## 📝 Summary  

✅ Easiest setup for beginners  
✅ Build + flash all in STM32CubeIDE  
✅ Works out of the box with ST-Link  


