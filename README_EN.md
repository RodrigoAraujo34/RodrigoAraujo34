<div align="center">

[![Português](https://img.shields.io/badge/Idioma-Português-009C3B?style=for-the-badge)](README.md)
[![English](https://img.shields.io/badge/Language-English-1E90FF?style=for-the-badge)](README_EN.md)

# 🚛 Rodrigo Araújo — CesnnaBravo

### 🤖 ETS2 & ATS Mod Developer — AI-Assisted Development

![ETS2](https://img.shields.io/badge/Euro%20Truck%20Simulator%202-Modding-orange?style=for-the-badge)
![ATS](https://img.shields.io/badge/American%20Truck%20Simulator-Compatible-1E90FF?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Windows-0078D4?style=for-the-badge&logo=windows&logoColor=white)

<br>

[![Download](https://img.shields.io/badge/Download-Brake_Fade_v0.6-4285F4?style=for-the-badge&logo=googledrive&logoColor=white)](https://drive.google.com/drive/folders/10GtsLWKFm5A8UQ5ram_yBqZJTe6cOlUx?usp=drive_link)
[![Buy Me a Coffee](https://img.shields.io/badge/☕_Support-Buy_Me_a_Coffee-FFDD00?style=for-the-badge&logo=buymeacoffee&logoColor=000000)](https://buymeacoffee.com/cesnnabravo)
[![Instagram](https://img.shields.io/badge/Instagram-@rodrigoaraujoca2-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com/rodrigoaraujoca2/)

![Visitors](https://komarev.com/ghpvc/?username=RodrigoAraujo34&label=PROJECT%20VISITORS&color=blueviolet&style=for-the-badge)

</div>

---

## 🌎 Choose your language

This is the complete **English version**. To read the project page in Portuguese:

[![READ IN ENGLISH](https://img.shields.io/badge/🇺🇸_READ-IN_ENGLISH-1E90FF?style=for-the-badge)](README_EN.md)
[![LER EM PORTUGUÊS](https://img.shields.io/badge/🇧🇷_LER-EM_PORTUGUÊS-009C3B?style=for-the-badge)](README.md)

---

## 👨‍💻 About Me

Hi! I'm **Rodrigo Araújo**, also known as **CesnnaBravo**.

I develop mods for **Euro Truck Simulator 2 (ETS2)** and **American Truck Simulator (ATS)**, using **Artificial Intelligence as a supporting tool during development**.

My goal is to create modifications that add new mechanics and increase the level of **realism, difficulty, and immersion** in truck simulators. I mainly work on systems and **DLL plugins** that introduce mechanics not originally available in the games.

### 🎯 Main focus

- 🚛 Realism and simulation
- ⚙️ New gameplay mechanics
- 🔥 Wear and temperature systems
- 🎮 Greater immersion
- 🛠️ DLL plugins for ETS2 and ATS
- 🧪 Experimental systems
- 🤖 AI-assisted development

---

# 🔥 Main Project

## 🚛 Brake Fade — Brake Overheating System

<div align="center">

![Version](https://img.shields.io/badge/VERSION-0.6-0078D4?style=for-the-badge)
![Status](https://img.shields.io/badge/STATUS-BETA-F5A623?style=for-the-badge)
![Games](https://img.shields.io/badge/GAMES-ETS2_%7C_ATS-F36F21?style=for-the-badge)

</div>

Brake Fade adds dynamic brake temperature and braking-efficiency simulation to **Euro Truck Simulator 2** and **American Truck Simulator**.

Long braking, steep descents, high speed, heavy cargo, and chassis wear can significantly increase brake temperature. As the brakes get hotter, braking performance progressively decreases. In extreme situations, the player may experience a severe or complete loss of service-brake efficiency.

---

# 🆕 What's New in v0.6

> 🔊 **MAJOR AUDIO UPDATE — BRAKE FADE v0.6 (BETA)**
>
> **IMPORTANT CONTROL CHANGE: F8 → F7.** On controller and steering-wheel versions, use **F7** for brake calibration. **F9** remains the virtual brake-axis assignment key.

### 🔊 New Dynamic Brake Audio Engine

- Real brake recordings combined with code-generated friction effects.
- Smooth volume fades and crossfades instead of abrupt audio cuts.
- Brake sounds respond to temperature, braking input, and vehicle movement.
- Gradual transitions between warm-brake and overheated-brake sounds.
- The existing `sounds` folder and original WAV filenames remain in use.

### 🚛 Realistic Brake Simulation

- Progressive brake heating and cooling, influenced by braking and vehicle speed.
- Heavy loads increase heat buildup; chassis wear affects braking performance.
- Braking efficiency decreases as temperature rises and can reach **0% at 500°C or above**.
- On-screen warnings for overheating, efficiency loss, recovery, and calibration.

### 🎮 Controls and Compatibility

- **F7:** three-step brake calibration (**replaces F8**, controller/wheel only).
- **F9:** assign the Brake Fade virtual brake axis (controller/wheel).
- **S:** standard brake key for the separate keyboard edition.
- Separate keyboard and controller/wheel builds for **ETS2 and ATS**.
- Beta release: ongoing testing and bug fixes based on player reports.

---

# ⚙️ Main Features

✅ Dynamic brake-temperature simulation  
✅ Progressive heating during braking  
✅ Speed-based brake cooling  
✅ Dynamic XAudio2 audio with real recordings, procedural effects, and smooth crossfades  
✅ Gradual loss of braking efficiency  
✅ Total service-brake loss at extreme temperatures  
✅ Cargo and truck weight influence heating  
✅ Chassis wear affects brake efficiency and heat generation  
✅ In-game temperature and efficiency notifications  
✅ Saved configuration and calibration  
✅ Keyboard, controller, steering wheel, and pedal compatibility  

---

# 🌡️ Temperature System

| Temperature | Brake condition |
|:---:|:---|
| 🟢 `0°C – 150°C` | Normal operation |
| 🟡 `150°C – 250°C` | Moderate heating |
| 🟠 `250°C – 350°C` | High temperature |
| 🔴 `350°C – 499°C` | Critical condition |
| ☠️ `500°C+` | Service-brake efficiency can reach 0% |

> ⚠️ **Be careful on descents.** Use the engine brake, reduce speed before going downhill, and avoid holding the service brake continuously.

---

# ⚖️ Weight and Brake Heating

The system considers the total weight of the truck and cargo. Heavier loads require more braking force and produce more heat, making heavy-haul journeys much more challenging.

| Total weight | Heating level |
|:---:|:---:|
| 🚚 10 tons | Normal |
| 🚚 20 tons | Increased |
| 🚛 30 tons | Elevated |
| 🚛 40 tons | High |
| 🚛 50 tons | Very high |
| 🚛 60+ tons | Extreme 🔥 |

---

# 🎮 Compatibility

| Device / Game | v0.6 status |
|:---|:---:|
| ⌨️ Keyboard | ✅ Supported |
| 🎮 Controller | ✅ Supported |
| 🛞 Steering wheel | ✅ Supported |
| 🦶 Pedals | ✅ Supported |
| 🚛 Euro Truck Simulator 2 | ✅ Supported |
| 🇺🇸 American Truck Simulator | ✅ Supported |

---

# 📥 Official Download

<div align="center">

## Brake Fade `v0.6`

[![DOWNLOAD MOD](https://img.shields.io/badge/📥_DOWNLOAD_BRAKE_FADE_v0.5-GOOGLE_DRIVE-4285F4?style=for-the-badge&logo=googledrive&logoColor=white)](https://drive.google.com/drive/folders/10GtsLWKFm5A8UQ5ram_yBqZJTe6cOlUx?usp=drive_link)

The official folder is used for current releases, future updates, and project files. **Please verify that the v0.6 package for your device is present before downloading.**

</div>

---

# 🛠️ Installation and Setup

### 1. Install the correct edition

1. Download the **v0.6** package for your input device: **keyboard** or **controller / steering wheel**.
2. Close ETS2/ATS before copying files.
3. Open the game's `bin/win_x64/plugins` directory. Create `plugins` if it does not exist.
4. Copy the DLL included with your edition into `plugins`, together with its complete `sounds` folder.
5. **Remove older Brake Fade DLLs from the same plugins directory** to avoid two versions loading at once. Do not delete unrelated plugins.
6. Keep the WAV filenames unchanged. The folder should look like this:

```text
bin/
└── win_x64/
    └── plugins/
        ├── <Brake Fade DLL supplied with your download>
        └── sounds/
            ├── audio carreta temperatura baixa.wav
            └── audio_carreta temperatura alta.wav
```

### 2. Controller / steering wheel calibration — **F7 (not F8)**

1. Start ETS2/ATS and connect your controller or wheel.
2. **Release** the physical brake trigger/pedal completely, then press **F7**.
3. **Fully press and hold** the brake trigger/pedal, then press **F7** again.
4. **Release** the brake completely, then press **F7** once more to finish.
5. Open **Options → Controls**. Choose the Brake Fade virtual input device if it is listed by the game.
6. Select **Brake Axis** and press **F9** to assign the virtual axis.
7. Set **Brake Axis Mode** to **Normal**.
8. Remove any direct assignment of the physical brake pedal/trigger to the game's original Brake Axis, since it can bypass the mod's efficiency reduction.

> ⚠️ **Updated shortcut:** **F8 is no longer the calibration key. Use F7.** F9 has not changed. The keyboard edition does not need F7 calibration.

### 3. Keyboard edition

Use **S** for braking, as in the previous keyboard version. Install the keyboard DLL rather than the controller/wheel DLL. Follow any input-binding instructions included with that edition; do not install both editions together.

---

# 🧰 Troubleshooting / Known Issues

| Problem | What to check / How to fix |
|:---|:---|
| **The mod does not load** | Confirm you are using the **64-bit game**, the correct game's `bin/win_x64/plugins` directory, and the correct DLL edition. Restart the game and inspect `game.log.txt` for plugin-loading errors. |
| **No brake sounds** | Make sure the `sounds` folder is beside the DLL and both WAV files have their original names. Check Windows audio output and the game's volume. |
| **Brake audio sounds too loud or unusual** | Check whether duplicate Brake Fade DLLs are installed. Report the brake temperature, vehicle speed, and whether the pedal was pressed. |
| **F7 does not calibrate** | Use the controller/wheel edition, keep the game focused, and perform all three steps: released → fully pressed → released. Make sure no other software intercepts F7. |
| **F9 does not bind the axis** | Click the in-game **Brake Axis** assignment field first, then press F9. Check that the Brake Fade virtual device is available and **Brake Axis Mode** is **Normal**. |
| **Truck brakes by itself / inverted brake axis** | Check for duplicate brake bindings, repeat F7 calibration, and verify **Brake Axis Mode: Normal**. Remove direct physical-axis assignments that bypass the virtual axis. |
| **Braking strength does not change** | Check whether the original physical brake is still assigned directly in the game. Use the mod's virtual axis on the controller/wheel edition. |
| **Mod stops working after an update** | Verify that the downloaded DLL matches your current game version. Remove older Brake Fade DLLs and restart ETS2/ATS. |
| **Game crashes or freezes** | Temporarily remove the Brake Fade DLL to compare behavior, then provide the game log and your game/mod versions. Do not assume the plugin is the cause without testing. |

### 🐛 Report a Bug

Please include: **ETS2 or ATS**, game version, **Brake Fade v0.6 edition** (keyboard/controller/wheel), Windows version, steps to reproduce, what you expected, what happened, and relevant excerpts from `game.log.txt` (usually in your ETS2/ATS user-data folder). If you use a custom `-homedir`, check that location instead. Remove private information before sharing logs.

> **Beta notice:** Not every configuration has been tested. These are troubleshooting recommendations, not a claim that every issue listed is a confirmed bug.

---

# 🎥 Video Tutorials

<div align="center">

[![Tutorial 1](https://img.shields.io/badge/▶_WATCH_TUTORIAL_1-YOUTUBE-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/watch?v=pR7P1BxTyl8)

[![Tutorial 2](https://img.shields.io/badge/▶_WATCH_TUTORIAL_2-YOUTUBE-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/watch?v=BuuNf36USyU)

</div>

---

# ☕ Support Development

<div align="center">

Brake Fade is available **free of charge to the community**.

If you enjoy the project, you can voluntarily support the development of new releases, improvements, bug fixes, and future mods.

[![Buy Me a Coffee](https://img.shields.io/badge/☕_SUPPORT_MY_WORK-BUY_ME_A_COFFEE-FFDD00?style=for-the-badge&logo=buymeacoffee&logoColor=000000)](https://buymeacoffee.com/cesnnabravo)

### Every contribution helps. Thank you! 🚛❤️

</div>

> ⚠️ **Support is completely optional.** A contribution is not required to download or use the mod and does not represent the purchase of the project. Brake Fade will remain freely available.

---

# 📦 Available Versions

| Version | Release status |
|:---:|:---|
| `v0.6` | 🟡 Current beta / Available |
| `v0.5` | ⚪ Previous version |
| `v0.4` | ⚪ Previous version |
| `v0.3` | ⚪ Previous version |

---

# 📜 Changelog

## 🚀 v0.6 — Current Beta

- New XAudio2 dynamic brake audio with real recordings and procedural effects
- Smooth sound transitions and fades
- Calibration shortcut changed from **F8 to F7** (controller/wheel)
- **F9** virtual-axis binding retained
- Separate keyboard and controller/wheel editions
- Continued brake heating, cooling, cargo weight, chassis wear, and efficiency warnings
- Beta testing and stability review

## 📦 v0.5

- Brake sound effects
- New cooling system
- Chassis damage affects braking performance
- Temperature and efficiency warnings
- Cargo-weight influence
- Saved settings and calibration
- Stability improvements and bug fixes
- Keyboard, controller, steering wheel, and pedal support
- ETS2 and ATS compatibility

## 📦 v0.4

- Brake-temperature warnings
- Current braking-efficiency display
- Calibration confirmation
- Saved settings and calibration
- Bug fixes and stability improvements

## 📦 v0.3

- Keyboard support
- Controller support
- Steering wheel and pedal support

---

# 🛠️ Technologies and Tools

<div align="center">

![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![CMake](https://img.shields.io/badge/CMake-064F8C?style=for-the-badge&logo=cmake&logoColor=white)
![Visual Studio](https://img.shields.io/badge/Visual%20Studio-5C2D91?style=for-the-badge&logo=visualstudio&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)

</div>

- C++ and CMake
- Visual Studio and Visual Studio Code
- SCS Telemetry SDK
- DLL plugins
- Artificial Intelligence as a development-support tool

---

# 📊 Project Status

| Project | Version | Status |
|:---|:---:|:---:|
| 🔥 Brake Fade for ETS2 / ATS | `v0.6` | 🟡 Available / Beta |
| 🚛 New truck-simulator mods | Coming soon | 🟡 Planning |

Future versions may include additional bug fixes, simulation improvements, controller and wheel enhancements, new realism mechanics, optimization, and easier configuration.

---

# ⚠️ Notice

The projects shown in this repository are developed by **Rodrigo Araújo**, using **Artificial Intelligence as a supporting tool**. Some releases may still be under development or in beta testing. Always check the version, requirements, and installation instructions before use.

---

# 📱 Links

<div align="center">

[![Instagram](https://img.shields.io/badge/Instagram-@rodrigoaraujca2-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com/rodrigoaraujca2)
[![GitHub](https://img.shields.io/badge/GitHub-RodrigoAraujo34-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/RodrigoAraujo34)
[![YouTube](https://img.shields.io/badge/YouTube-Tutorials-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/watch?v=pR7P1BxTyl8)
[![Support](https://img.shields.io/badge/Support-Buy_Me_a_Coffee-FFDD00?style=for-the-badge&logo=buymeacoffee&logoColor=000000)](https://buymeacoffee.com/cesnnabravo)

### ⭐ If you enjoy my mods, please star the repository.

### Thank you for supporting my work! 🚛❤️

</div>
