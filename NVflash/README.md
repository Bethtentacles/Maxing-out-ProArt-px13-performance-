# NVFlash for ASUS ProArt PX13

NVIDIA vBIOS files and flashing utilities for increasing GPU TDP.

---

## 📁 Contents

| File | Description |
|------|-------------|
| `4060120w.rom` | RTX 4060 vBIOS with 120W TDP |
| `4070120w.rom` | RTX 4070 vBIOS with 120W TDP |
| `backup4060.rom` | Backup of original 4060 vBIOS |
| `nvflash.exe`   | NVFlash utility (32-bit) |
| `nvflash64.exe` | NVFlash utility (64-bit) | (this is the one you're using)

---

## 🚀 vBIOS Flash (Advanced Users Only)

> ⚠️ **Warning:** Flashing a modified vBIOS can void your warranty and potentially brick your GPU. Although the risk is low and you can easily reflash the back up bio if something happens. Proceed at your own risk. Always create a backup first!

1. Open Command Prompt as Administrator
2. Navigate to the `NVflash` folder:
   ```
   cd "C:\path\to\NVflash"
   ```
   For example, if you downloaded the repo to your Downloads folder:
   ```
   cd "C:\Users\YourUsername\Documents\PX13\NVflash"
   ```
3. Flash the new vBIOS:
   ```
   nvflash64 --protectoff
   ```
        (for RTX4060)
   ```
   nvflash64 -6 4060120w.rom
   ```
        (for RTX4070)
   ```
   nvflash64 -6 4070120w.rom
   ```
4. Restart your computer

---

## 📝 Notes

- The vBIOS files are specifically for the ASUS ProArt PX13 - do not use on other devices
- Always keep a backup of your original vBIOS

---

## 🔗 Credits

- [NVFlash](https://www.techpowerup.com/download/nvidia-nvflash/) by NVIDIA
