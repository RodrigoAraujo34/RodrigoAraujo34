<div align="center">

[![Português](https://img.shields.io/badge/Idioma-Português-009C3B?style=for-the-badge)](README.md)
[![English](https://img.shields.io/badge/Language-English-1E90FF?style=for-the-badge)](README_EN.md)
[![Español](https://img.shields.io/badge/Idioma-Español-EAA221?style=for-the-badge)](README_ES.md)

# 🚛 Rodrigo Araújo — CesnnaBravo

### ETS2 and ATS mod development with AI assistance

![Version](https://img.shields.io/badge/BRAKE_FADE-v0.7-8A2BE2?style=for-the-badge)
![Status](https://img.shields.io/badge/STATUS-BETA-F5A623?style=for-the-badge)
![Platform](https://img.shields.io/badge/Windows-64_bit-0078D4?style=for-the-badge&logo=windows&logoColor=white)

[Downloads](https://drive.google.com/drive/folders/10GtsLWKFm5A8UQ5ram_yBqZJTe6cOlUx?usp=drive_link) · [Discord](https://discord.gg/yFgebpcX8) · [Instagram](https://instagram.com/rodrigoaraujoca2/) · [Support development](https://buymeacoffee.com/cesnnabravo)

</div>

## 👨‍💻 About me

I am Rodrigo Araújo Campos, also known as CesnnaBravo. I develop DLL plugins and mods for Euro Truck Simulator 2 and American Truck Simulator, using artificial intelligence as a development aid. My projects focus on realism, simulation, new mechanics, and immersion.

## 🔥 Brake Fade v0.7

Brake Fade simulates brake temperature and reduced braking efficiency. Cargo mass, speed, and chassis wear influence the simulation. Continuous braking can overheat the brakes and severely reduce their effectiveness.

### 🆕 What is new?

- **Two input modes in one DLL:** select Keyboard or Controller/wheel in the panel.
- **Keyboard:** hold **S** to brake; release it to let go. No controller or calibration required.
- **Controller/wheel:** retain analog pedal or trigger input and saved calibration.
- **Redesigned F10 panel:** sidebar navigation, organized settings, volume, simulation, and warnings.
- **Three languages:** Brazilian Portuguese, English, and Spanish, applied immediately to the panel, warnings, calibration instructions, diagnostics, and displayed history.
- **Custom shortcuts:** F7 and F10 are defaults; choose other function keys in the panel. F9 and S remain fixed.
- **Diagnostics and logs:** check session status, input mode, audio, and calibration, and copy event history for support.
- **Saved preferences:** input mode, language, volume, warning visibility, simulation, and shortcuts.

Dynamic audio, WAV layers, procedural sound, smooth transitions, thermal simulation, cooling, cargo influence, and chassis wear remain part of the mod.

![Brake Fade v0.7 panel with keyboard mode selected](assets/brake-fade-v07-teclado.png)

*Actual standalone panel preview, shown in Portuguese. Use the language selector to switch to English.*

## 📥 Official downloads

[**Open the official download folder**](https://drive.google.com/drive/folders/10GtsLWKFm5A8UQ5ram_yBqZJTe6cOlUx?usp=drive_link)

**Check that the v0.7 package is present before downloading.** Updating this README does not upload the binary package to Google Drive.

## 📦 Installation

1. Completely close ETS2/ATS.
2. In Steam, open the game's **Properties → Installed Files → Browse**.
3. Open `bin\win_x64\plugins`; create `plugins` if it does not exist.
4. Back up older Brake Fade DLLs outside that folder and remove them from `plugins`.
5. Copy the v0.7 DLL and the supplied `sounds` folder into `plugins`.
6. Start the game, load your profile/save, and enter your truck.
7. Press **F10**, or your saved shortcut, to open the panel.

```text
bin/win_x64/plugins/
├── ets2_brake_fade.dll
└── sounds/
    ├── audio carreta temperatura baixa.wav
    └── audio_carreta temperatura alta.wav
```

The DLL name may vary by package; the source build may use `ets2_brake_fade_wheel.dll`. **Install only one Brake Fade DLL.** The integrated version supports both modes even if its filename contains `wheel`. Keep the WAV filenames unchanged.

This is a DLL plugin, not an `.scs` file to enable in Mod Manager.

## 🎯 Assign the virtual brake axis — both modes

1. Close the mod panel and open **Options → Controls** in the game.
2. Click the **Brake axis** assignment field.
3. Without operating your pedal or trigger, press **F9** once.
4. Check that the Brake Fade axis is assigned. It may appear as **ETS2 Brake Fade / Brake Fade Pedal**.
5. Set brake axis mode to **Normal**.

The game must use the **virtual axis**, not the physical brake axis directly. This is how the plugin sends braking reduced by fade. F9 assigns the axis; it does not calibrate your equipment.

### ⌨️ Keyboard

1. In **Settings → Keys and controls**, select **Keyboard**.
2. Remove **S** from the game's original digital service brake binding in **Keys & Buttons**.
3. Keep the virtual brake axis assigned with F9.
4. Return to driving, close the panel, release S, then hold S to brake.

No controller or calibration is needed. The plugin still reads S after its original game binding is removed. Keeping that digital binding can apply braking in parallel and bypass the intended fade effect.

S requests full braking, limited by current brake efficiency. Release S before pressing it again after a pause, focus change, or mode switch. Keyboard braking is blocked outside the game, while the panel is open, and while driving is paused.

### 🛞 Steering wheel and pedals

1. Connect the equipment before starting the game and check that Windows recognizes it.
2. Select **Controller/wheel** in the panel.
3. Stop the truck, return to driving, and close the mod panel.
4. **Release the brake fully and press F7.**
5. **Press only the brake to 100%, hold it there, and press F7 again.**
6. **Fully release it and press F7 a third time.**
7. Check the calibration complete message.
8. Assign the virtual brake axis using F9, in Normal mode, and test at low speed.

Do not move other pedals or axes during calibration. Steering, accelerator, and clutch can retain their normal physical axis assignments. Use your customized calibration key if you changed F7.

### 🎮 Controller/gamepad

Select **Controller/wheel** and calibrate the intended analog brake trigger/axis using the same three stages: **released → F7; fully pressed → F7; released → F7**. Close the panel and perform calibration in driving mode.

Then assign the virtual axis with F9 in Normal mode. Remove digital brake bindings that could act in parallel. Do not move thumbsticks or other triggers during calibration. A control exposed only as a digital button may not be detected as a brake axis.

### 🔄 Switching modes and recalibrating

Stop the truck, release all brake inputs, and choose the mode in the panel. Your choice is saved; wheel calibration is retained. The same virtual axis serves both modes.

If calibration is already active, pressing the calibration shortcut starts recalibration. Follow the instructions to press fully, confirm, release, and confirm again. Users migrating from the old keyboard-only DLL should recheck the F9 assignment because the integrated device retains the wheel version's identifier.

## ⌨️ Shortcuts and languages

| Default | Action |
|:---:|:---|
| F10 | Open/close panel |
| F7 | Calibrate/recalibrate controller or wheel |
| F9 | Assign virtual axis; fixed |
| S | Keyboard brake; fixed |
| Esc | Close panel or cancel shortcut capture |

Customize F7/F10 using F1–F12 except F9; the two shortcuts must differ. **Restore default shortcuts** returns them to F7/F10.

Use **Language / Idioma** to select Português (Brasil), English (US), or Español. The choice takes effect immediately and is saved. Technical identifiers, filenames, and error codes remain unchanged. Existing disk log lines retain the language used when written.

## 🌡️ Temperature, load, and wear

| Temperature | Thermal efficiency |
|:---:|:---:|
| Up to 150 °C | 100% |
| 200 °C | 95% |
| 250 °C | 85% |
| 300 °C | 70% |
| 350 °C | 50% |
| 400 °C | 30% |
| 450 °C | 15% |
| 500 °C or above | 0% |

Efficiency changes progressively between these points. Chassis wear also limits final efficiency. Warnings start at 300, 350, 400, 450, and 500 °C; recovery is announced after a heat warning when temperature falls to 150 °C or below.

Cargo mass from telemetry affects heating; speed influences heating and cooling. Use the engine brake and retarder when available and plan your braking in the game.

## 🛠️ Troubleshooting

| Problem | Check |
|:---|:---|
| Panel does not open | Correct DLL folder, extracted files, game restarted, saved shortcut, Fn key if needed. |
| Waiting for profile/save | Load the save and enter driving mode. |
| S does not brake | Keyboard mode, virtual axis assigned, game focused, panel closed, release S before pressing again. |
| Calibration fails | Recognized analog axis, Controller/wheel mode, panel closed, only brake moved. |
| Brake remains applied | Recalibrate, use Normal axis mode, remove conflicting bindings. |
| Fade has no effect | Simulation enabled, virtual brake axis assigned, no physical/digital brake acting in parallel. |
| F9 does not assign | Click the Brake axis assignment field first; check Fn + F9 if needed. |
| Audio missing | Panel volume, simulation enabled, Windows output, `sounds` folder, exact WAV filenames; 16-bit PCM mono/stereo. |
| Overlay missing | Try Windowed or Borderless Windowed. Exclusive fullscreen is not guaranteed. |

Procedural sound may still play if WAV layers are missing. Hearing some audio does not confirm both WAVs loaded.

## 💬 Support

Use **Diagnostics** and **Logs** in the panel. Include the game/version, Brake Fade v0.7, input mode, equipment model, reproduction steps, and a screenshot or copied logs.

- `brake_fade_v07.log`: next to the DLL.
- `game.log.txt`: usually under `Documents\Euro Truck Simulator 2` or `Documents\American Truck Simulator`, or your custom `-homedir`.
- [Discord support and community](https://discord.gg/yFgebpcX8)

Preferences are saved in `brake_fade_v07.ini` beside the DLL. Wheel calibration is stored separately.

## 🎥 Video tutorials

[Tutorial 1](https://www.youtube.com/watch?v=pR7P1BxTyl8) · [Tutorial 2](https://www.youtube.com/watch?v=25W1FI4E_3o&t=205s)

Videos may show an earlier version. Use this README for v0.7 mode selection and customizable shortcuts.

## 📜 Version history

- **v0.7 — Current beta:** unified input modes, redesigned panel, three languages, customizable shortcuts, diagnostics, and saved preferences.
- **v0.6:** dynamic audio, smooth transitions, F7 as the default calibration key, F9 for axis assignment.
- **v0.5:** earlier brake audio, revised cooling, chassis wear and cargo influence.
- **v0.4:** temperature warnings, efficiency display, calibration confirmation, and saved settings.
- **v0.3:** expanded input device support.

This is a beta. Builds, automated checks, and panel previews were verified; in-game behavior across different equipment and configurations remains part of player testing.

## 💜 Support development

Brake Fade is free. Donations are optional and are not required to download or use the mod.

[Buy Me a Coffee](https://buymeacoffee.com/cesnnabravo)

PIX — random key, Rodrigo Araújo Campos:

```text
c2ad1129-8267-4e80-a0b6-2e0ddb93526c
```

You can also support the project by leaving a ⭐ on [GitHub](https://github.com/RodrigoAraujo34/RodrigoAraujo34).

**Realism • Simulation • Immersion — Rodrigo Araújo Campos / CesnnaBravo**
