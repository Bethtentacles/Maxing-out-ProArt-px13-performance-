# ASUS ProArt PX13 Performance Optimization

This repo contains all the resources needed to maximize the performance of an ASUS ProArt PX13.

> ⚠️ **Disclaimer:** I do not take credit for any of the programs provided in this repo. For the sake of simplicity, everything you need is included here.

---

## 📁 Contents

### Ghelper
Contains [G-Helper](https://github.com/seerge/g-helper) - an open-source alternative to Armoury Crate for ASUS laptops.

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
| `nvflash.exe` | NVFlash utility (32-bit) |
| `nvflash64.exe` | NVFlash utility (64-bit) |

---

## 🚀 Quick Start

### G-Helper Setup
1. Copy the `Ghelper` folder to your desired location
2. Run `GHelper.exe`
3. The included `config.json` will automatically apply optimized settings

### vBIOS Flash (Advanced Users Only)

> ⚠️ **Warning:** Flashing a modified vBIOS can void your warranty and potentially brick your GPU. Proceed at your own risk. Always create a backup first!

1. Open Command Prompt as Administrator
2. Navigate to the `NVflash` folder
3. Create a backup of your current vBIOS:
   ```
   nvflash64 --save backup.rom
   ```
4. Flash the new vBIOS:
   ```
   nvflash64 --protectoff
   nvflash64 -6 4060120w.rom
   ```
5. Restart your computer

---

## ⚙️ Performance Profiles

The G-Helper config includes three pre-configured profiles:

| Profile | Total TDP | CPU Limit | Use Case |
|---------|-----------|-----------|----------|
| Silent | 5W | 5W | Battery saving, quiet operation |
| Balanced | 75W | 48W | Everyday use |
| Turbo | 50W | 80W | Maximum performance |

---

## 📝 Notes

- Make sure to disable Armoury Crate before using G-Helper
- The vBIOS files are specifically for the ASUS ProArt PX13 - do not use on other devices
- Always keep a backup of your original vBIOS

---

## 🔗 Credits & Resources

- [G-Helper](https://github.com/seerge/g-helper) by seerge
- [NVFlash](https://www.techpowerup.com/download/nvidia-nvflash/) by NVIDIA

---

## ⚖️ License

This repository is provided for educational purposes only. Use at your own risk.
