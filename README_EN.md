<div align="center">

[Português](README.md) · [English](README_EN.md) · [Español](README_ES.md)

# Rodrigo Araújo — CesnnaBravo
### Mods for Euro Truck Simulator 2 and American Truck Simulator

![Version](https://img.shields.io/badge/ETS_BRAKE_FADE-0.7.3.1-5965F2?style=for-the-badge)
![Platform](https://img.shields.io/badge/Windows-x64-0078D4?style=for-the-badge)
![Status](https://img.shields.io/badge/STATUS-BETA-F5A623?style=for-the-badge)

[Official download](https://drive.google.com/drive/folders/10GtsLWKFm5A8UQ5ram_yBqZJTe6cOlUx?usp=drive_link) · [Discord](https://discord.gg/yFgebpcX8) · [Instagram](https://instagram.com/rodrigoaraujoca2/) · [Support development](https://buymeacoffee.com/cesnnabravo)

</div>

## About the project

I am Rodrigo Araújo Campos, also known as CesnnaBravo. I develop mods and DLL plugins for ETS2 and ATS, using AI as a development aid. My focus is simulation, challenge and immersion.

**ETS BRAKE FADE** simulates brake temperature and the loss of braking efficiency caused by overheating. Repeated or prolonged braking builds heat; cooling gradually restores thermal efficiency. Cargo mass, speed, chassis wear and estimated incline influence the model.

The displayed temperature is **calculated by the mod**, not a real measurement of individual discs or drums. This version has no overload system or separate brake wear/maintenance system.

## What is new in 0.7.3.1?

- **Light or dark panel**, with a saved theme preference and Portuguese, English and Spanish interfaces.
- **Thermal settings:** noise onset temperature, heating rate and cooling rate.
- **Brake monitor:** simulated temperature, efficiency, cargo and estimated incline.
- **Keyboard, controller and steering wheel in one DLL**, selectable in the panel.
- **ETS2 and ATS:** game identification and calibration stored in the correct game folder.
- **In-game device/axis label:** `ETS BRAKE FADE 0.7.3.1`. The internal identifier is unchanged to preserve existing bindings.
- **Update checker**, supporting three-part and four-part versions. Notifications require a newer release on the server; installation remains manual.

### Included fixes

| Area | Fix |
|---|---|
| Windows loading | C++ runtime bundled into the DLL, removing the external Visual C++ dependencies involved in the reported `0000007E` loading failure. |
| Thermal panel | Panel-rendered sliders replace blank tracks; dragging, keyboard adjustment and reopening are supported. |
| In-game brake meter | Pedal/S preview works in control options while driving is paused, without advancing the thermal simulation. |
| Calibration | Completion, travel, direction and stored values are validated; invalid files are not treated as calibrated. |
| Pedals | Slider 1/2 axis persistence and an attempt to recover after input loss. |
| Saving | Temporary-file write before replacing calibration; diagnostics report save failure. |
| ATS | Separate calibration from ETS2; game window selected by the process hosting the plugin. |
| Input/startup | Axis resynchronization, F9 restricted to the game window and diagnostics for essential SDK event registration failure. |
| Simulation | Invalid telemetry is handled to prevent persistent temperature or brake-output corruption. |

**Brake smoke is not included in this update.** The experiment is postponed and disabled in the normal distribution.

## Download

Use the [official download folder](https://drive.google.com/drive/folders/10GtsLWKFm5A8UQ5ram_yBqZJTe6cOlUx?usp=drive_link) and check that the ZIP is **0.7.3.1**. Older packages may remain in the folder. The website is being prepared; the folder above remains the download reference.

## Installation — Windows 64-bit

1. Close the game and keep a backup of the previous DLL outside `plugins`.
2. Extract the package. Copy **`ets2_brake_fade.dll`** and **`sounds`** to the appropriate installation folder:

```text
Euro Truck Simulator 2\bin\win_x64\plugins
American Truck Simulator\bin\win_x64\plugins
```

3. Create `plugins` if needed. Keep **only one Brake Fade DLL** in each installation.
4. Preserve `brake_fade_v07.ini` to retain preferences. If you tested smoke, remove `cb_brake_smoke_probe.dll` and replace the experimental host with the normal DLL.
5. Start the game, load a profile/save and enter driving mode. Open the panel with **F10** or your saved shortcut.

The filename `ets2_brake_fade.dll` is the same for both games; it is not ETS2-only. Install the plugin beside the game executable as described above, not as an `.scs` file in Mod Manager.

## Keyboard, controller and wheel

| Default key | Function |
|---|---|
| F10 | Open/close the panel. Customizable. |
| F7 | Advance controller/wheel calibration. Customizable. |
| F9 | Send a pulse to bind the virtual brake axis. Fixed. |
| S | Brake in Keyboard mode. Fixed. |
| Esc | Close the panel or cancel shortcut capture. |

### Keyboard

Select **Keyboard** in the panel. Hold **S** to brake; release it to stop braking. No controller or calibration is required.

Assign the **virtual axis** to the game's brake: select the **Brake axis** binding field and press F9. Remove the game's original digital S brake binding so it does not apply braking in parallel and bypass fade.

During driving, the plugin ignores S outside the game window or while its panel is open. After returning from pause or switching modes, release S before pressing it again.

### Controller, wheel and pedals

Select **Controller/wheel** and check your saved calibration shortcut. While in driving mode, with the panel closed:

1. Fully release the brake; press and release the calibration shortcut.
2. Press **only the brake** to 100%, hold it and press the shortcut again.
3. Fully release the brake and press the shortcut a third time.
4. Check completion and saving in **Diagnostics**.
5. Select **Brake axis** in the game's options and use F9 to bind the virtual axis.

Check polarity: the meter should be at rest with the pedal released and increase when pressed. **Keep Normal/Inverted if it already works correctly in your profile.** Never bind Brake Fade to steering.

Old files without calibration-completion confirmation require recalibration once. Valid files from the stability revision can be reused. Compatibility depends on the driver exposing a readable analog axis; not every device is guaranteed.

### File locations

| File | Location |
|---|---|
| Preferences and shortcuts | `brake_fade_v07.ini`, beside the DLL. |
| Plugin log | `brake_fade_v07.log`, beside the DLL. |
| ETS2 calibration | `Documents\Euro Truck Simulator 2\BrakeFade\wheel_config.ini` |
| ATS calibration | `Documents\American Truck Simulator\BrakeFade\wheel_config.ini` |

Paths follow your Windows Documents location. ETS2 and ATS have separate calibrations. If an older ATS build saved calibration in the ETS2 folder, recalibrate in ATS; there is no need to delete the ETS2 file.

## Customize braking

In **Thermal settings**:

| Setting | Range | Default |
|---|---|---|
| Noise onset temperature | 50–500 °C | 100 °C |
| Cooling rate | 25–200% | 100% |
| Heating rate | 25–200% | 100% |

**Higher rate = faster; lower rate = slower.** These percentages are rates, not durations in seconds. Noise requires braking and movement and increases gradually above the threshold.

100% preserves the slower cooling adjustment. In a model test without braking, cooling from 500 °C to 150 °C took about **6 min 30 sec stationary** and **3 min 43 sec at 80 km/h**. These are active simulation-time references, not real-truck measurements; braking and different settings change the result.

The **Theme: light / Theme: dark** button is near the bottom of the sidebar. Volume, language, warnings and simulation are also configurable. Preferences save automatically.

## Troubleshooting and support

- **No panel or notifications:** check `game.log.txt`. `unable to load: 0000007E` occurs before plugin startup. Use the updated package; it bundles the C++ runtime and removes the previous build's external Visual C++ dependencies. If it persists, send a fresh log.
- **No braking:** check input mode, calibration and the virtual brake-axis binding. Test the meter in the game's options.
- **Abrupt A/D steering:** check the game's controller type and bindings. The mod's virtual axis must control only the brake.
- **Calibration is not saved:** check Diagnostics and send the log. A calibration may work for the current session but require repeating after restart if saving failed.
- **No audio:** check volume, enabled simulation, Windows output and `sounds`. WAV layers use 16-bit PCM, mono or stereo. Procedural audio can work even without the WAVs.
- **No overlay:** try Windowed or Borderless Windowed. Exclusive fullscreen may prevent display.

On [Discord](https://discord.gg/yFgebpcX8), include the mod/game versions, equipment, input mode and reproduction steps. Send `game.log.txt` and `brake_fade_v07.log` from the affected attempt. The game log is usually in its ETS2/ATS Documents folder, or your custom `-homedir`.

The x64 build and **eight automated tests** passed, covering DLL loading, ATS/ETS2 identification, dependencies, calibration, languages, input, thermal physics and the panel. Users have confirmed the fixes for reported cases; this does not guarantee bug-free operation on every setup.

## Video tutorials

[Tutorial 1](https://www.youtube.com/watch?v=pR7P1BxTyl8) · [Tutorial 2](https://www.youtube.com/watch?v=25W1FI4E_3o&t=205s)

Videos may show earlier versions. Follow this README for 0.7.3.1 shortcuts, installation and calibration.

## Version history

| Version | Main changes |
|---|---|
| **0.7.3.1** | Light/dark themes, thermal settings, monitor, panel/calibration/input fixes, revised ATS support and loading without external Visual C++ dependencies. |
| 0.7 | Unified input modes, redesigned panel, three languages, shortcuts and diagnostics. |
| 0.6 | Dynamic audio and smooth transitions. |
| 0.5 | Revised cooling and cargo/chassis-wear influence. |
| 0.4 | Temperature warnings, calibration and saved settings. |
| 0.3 | Expanded input-device support. |

## Future improvements — under consideration

- Continue fixing issues using community reports and logs.
- Broaden wheel, pedal and controller testing in ETS2 and ATS.
- Refine diagnostics, interface and thermal behavior using player feedback.
- Resume brake-smoke research after stability work. The current prototype is diagnostic and **does not render visual particles**.

These are not available features or promises of dates or compatibility. Stability is the current priority.

Older builds that only recognize three-part versions cannot automatically detect `0.7.3.1`; this migration is manual. This version's checker understands three or four components and never installs DLLs automatically.

## Support development

The mod is free. Donations are optional and are not needed to download or use it.

[Buy Me a Coffee](https://buymeacoffee.com/cesnnabravo)

PIX — random key, Rodrigo Araújo Campos:

```text
c2ad1129-8267-4e80-a0b6-2e0ddb93526c
```

[Instagram](https://instagram.com/rodrigoaraujoca2/) · [Discord](https://discord.gg/yFgebpcX8) · [GitHub](https://github.com/RodrigoAraujo34/RodrigoAraujo34)

**Realism • Simulation • Immersion — CesnnaBravo**
