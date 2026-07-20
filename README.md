# Dyanamic-Senfix-by-lilsmok3_V2
# SA-MP Dynamic Sensitivity & Micro-Tuning

A custom C++ ASI plugin for Grand Theft Auto: San Andreas Multiplayer (SA-MP) that introduces granular, real-time sensitivity tuning. 

This plugin separates standard camera free-look from weapon aiming, allowing players to stack specific weapon multipliers over a global master sensitivity. 

## ⚙️ Technical Features
* **Bypassed SDK Hooks:** Utilizes the `drawHudEvent` for stable execution and memory writes, bypassing unreliable animation state flags in SA-MP.
* **Direct Memory Manipulation:** Adjusts sensitivity directly via memory addresses `0xB6EC1C` (X-axis) and `0xB6EC18` (Y-axis) based on the active weapon slot.
* **Live Micro-Tuning:** In-game, non-intrusive UI for real-time 0.01 increment adjustments.
* **Instant Persistence:** Uses Windows API system calls (`WritePrivateProfileStringA`) to save configurations directly to the `.ini` file in real-time. No progress is lost on restart.

## 📥 Installation
1. Ensure you have an **ASI Loader** installed (like Silent's ASI Loader).
2. Download the latest `.zip`
3. Extract `Dynamic_sens_by_lilsmok3.asi` and `Dynamic_sens.ini` into your GTA San Andreas root folder or the `scripts/` folder.
4. **Highly Recommended:** Install [SilentPatch](https://gtaforums.com/topic/669045-silentpatch/) first. The vanilla game has a broken vertical (Y-axis) aspect ratio. SilentPatch fixes this baseline, allowing this mod to scale your X and Y axes perfectly uniformly.

## 🎮 How to Use (Live Editor)
Adjust your sensitivity perfectly without ever tabbing out of the game.

* **Tune Global Master:** Hold `2` + `UP/DOWN Arrows` or hold no weapon in hand  
  *(Scales your standard camera free-look sensitivity)*
* **Tune Specific Weapon:** Equip a weapon, then Hold `1` + `UP/DOWN Arrows` 
  *(Stacks a specific multiplier on top of your Global Master when holding Right-Click)*

All adjustments are made in `0.01` increments for precise muscle-memory tuning. 

## 📝 Configuration File (`Dynamic_sens.ini`)
If you prefer to type your values manually, open the `.ini` file.
```ini
[Multipliers]
Global=1.00
Pistols=1.00
Shotguns=1.00
SMGs=1.00
AssaultRifles=1.00
Snipers=1.00
Minigun=1.00
