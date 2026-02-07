# G-Helper for ASUS ProArt PX13

[G-Helper](https://github.com/seerge/g-helper) - an open-source alternative to Armoury Crate for ASUS laptops.

---

## 📁 Contents

| File | Description |
|------|-------------|
| `GHelper.exe` | G-Helper application |
| `config.json` | Pre-configured settings optimized for the PX13 |

**Config Highlights:**
- Custom fan profiles for Silent, Balanced, and Turbo modes
- GPU overclocking settings (Core +320MHz, Memory +540MHz in Turbo)
- CPU undervolting profiles (-30mV to -40mV)
- TDP limits configured for each performance mode

---

## 🚀 Setup

1. Copy the `Ghelper` folder to your desired location (i.e programs folder)
2. Copy the `config.json` file in to this location "C:\Users\[USER NAME]\AppData\Roaming\GHelper" (user name is what your log in name is...)
3. Run `GHelper.exe`
4. The included `config.json` will automatically apply optimized settings

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

- Make sure to uninstall Armoury Crate and ProArt Creator Hub before using G-Helper

---

## 🔗 Credits

- [G-Helper](https://github.com/seerge/g-helper) by seerge
