# ASUS ProArt PX13 Performance Optimization

This repo contains all the resources needed to maximize the performance of an ASUS ProArt PX13.

> ⚠️ **Disclaimer:** I do not take credit for any of the programs provided in this repo. For the sake of simplicity, everything you need is included here.

---

## 📁 Contents

### Ghelper
Contains [G-Helper](https://github.com/seerge/g-helper) - an open-source alternative to Armoury Crate or ProArt Creator Hub for ASUS laptops.

If you run in to sability issues, its most likelt due to these settings, Decrease the overclock settings if games crash and if system crashes decrease the undervolt for the cpu (-40 to -30)

| File | Description |
|------|-------------|
| `GHelper.exe` | G-Helper application |
| `config.json` | Pre-configured settings optimized for the PX13 |

**Config Highlights:**
- Custom fan profiles for Silent, Balanced, and Turbo modes
- GPU overclocking settings (Core +320MHz, Memory +540MHz in Turbo)
- CPU undervolting profiles (-30mV to -40mV)
- TDP limits configured for each performance mode

### NVflash
Contains NVIDIA vBIOS files and flashing utilities for increasing GPU TDP.

| File | Description |
|------|-------------|
| `4060120w.rom` | RTX 4060 vBIOS with 120W TDP |
| `4070120w.rom` | RTX 4070 vBIOS with 120W TDP |
| `backup4060.rom` | Backup of original 4060 vBIOS |
| `nvflash.exe`   | NVFlash utility (32-bit) |
| `nvflash64.exe` | NVFlash utility (64-bit) | (this is the one you're using)

---

## 🚀 Quick Start

### G-Helper Setup
1. Copy the `Ghelper` folder to your desired location (i.e programs folder)
2. Copy the `config.json` file in to this location "C:\Users\[USER NAME]\AppData\Roaming\GHelper" (user name is what your log in name is...)
3. Run `GHelper.exe`
4. The included `config.json` will automatically apply optimized settings

### vBIOS Flash (Advanced Users Only)

> ⚠️ **Warning:** Flashing a modified vBIOS can void your warranty and potentially brick your GPU. Although the risk is low and you can easily reflash the back up bio if something happens, proceed at your own risk!

1. Open Command Prompt as Administrator
2. Navigate to the `NVflash` folder:
   ```
   cd "C:\path\to\NVflash"
   ```
   For example, if you downloaded the repo to your Downloads folder:
   ```
   cd "C:\Users\YourUsername\Downloads"
   ```
3. Flash the new vBIOS:
   ```
   nvflash64 --protectoff
   ```
   **For RTX4060:**
   ```
   nvflash64 -6 4060120w.rom
   ```
   **For RTX4070:**
   ```
   nvflash64 -6 4070120w.rom
   ```
4. Restart your computer

---

## ⚙️ Performance Profiles

The G-Helper config includes three pre-configured profiles:

| Profile | Total TDP | CPU Limit | Use Case |
|---------|-----------|-----------|----------|
| Silent | 5W | 5W | Battery saving, quiet operation |
| Balanced | 75W | 50W | Everyday use |
| Turbo | 140W | 75W | Maximum performance |

---

## 📝 Notes

- Make sure to uninstal Armoury Crate and ProArt Creator Hub before using G-Helper
- The vBIOS files are specifically for the ASUS ProArt PX13 - do not use on other devices
- Always keep a backup of your original vBIOS

---

## 🔗 Credits & Resources

- [G-Helper](https://github.com/seerge/g-helper) by seerge
- [NVFlash](https://www.techpowerup.com/download/nvidia-nvflash/) by NVIDIA

---

## ⚖️ License

This repository is provided for educational purposes only. Use at your own risk.
