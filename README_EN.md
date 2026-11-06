<div align="center">

[Português](README.md) · [English](README_EN.md) · [Español](README_ES.md)

# Rodrigo Araújo — CesnnaBravo
### ETS BRAKE FADE 0.8.0

![Version](https://img.shields.io/badge/ETS_BRAKE_FADE-0.8.0-5965F2?style=for-the-badge)
![Platform](https://img.shields.io/badge/Windows-x64-0078D4?style=for-the-badge)

[Official website](https://cb-mods-road.wswmjkwr2r.chatgpt.site/) · [Downloads](https://cb-mods-road.wswmjkwr2r.chatgpt.site/#mods) · [Discord](https://discord.gg/yFgebpcX8)

</div>

> **NOTICE — WE ARE MOVING TO THE OFFICIAL WEBSITE**
>
> The [CB Mods website](https://cb-mods-road.wswmjkwr2r.chatgpt.site/) is now the project's main hub for current downloads, tutorials, registration, your library and purchases of the smoke add-on. This GitHub remains a project introduction and community reference. Download the current release from the website; older files may no longer represent the current distribution.

## About

I am Rodrigo Araújo Campos, also known as CesnnaBravo. I develop mods with AI assistance, aiming to add simulation and immersion to your journeys.

**ETS BRAKE FADE** simulates brake heating, cooling and loss of efficiency, with separate truck and trailer data. Temperatures, masses and power values are **model estimates** using a generic thermal profile, rather than real measurements or manufacturer data.

## What's new in 0.8.0

- Separate temperatures and brake fade for each vehicle, with recovery as the brakes cool.
- Estimated gross combination mass, cargo, speed and grade used in thermal calculations.
- Original game controls for keyboard, controller and wheel: **no plugin calibration or F9 required**.
- Light/dark panel themes, Portuguese/English/Spanish, audio and alerts.
- Adjustable heating and cooling rates from **25% to 200%**. Higher percentages mean faster changes.
- **Brake Smoke** add-on: smoke on the truck and attached trailers, stationary/moving profiles, adjustable density and an on/off switch.
- Browser-based account linking and server verification of smoke access.
- Notifications for newer releases published on the website. Installation remains manual.

### Brake fade curve

| Estimated temperature | Service-brake gain on the affected vehicle |
|---|---|
| Up to 350 °C | 100% |
| 440 °C | 50% |
| 530 °C or above | 0% |

The reduction is progressive between 350 and 530 °C. The truck and trailers are handled independently. Braking capacity recovers as they cool; parking and auxiliary brakes are preserved. This is a mod setting, not a specification for real brakes.

## Free base and paid smoke

| Product | Access |
|---|---|
| **ETS Brake Fade — base** | Free; braking works without signing in. |
| **Brake Smoke — add-on** | **R$ 15 BRL**, one-time purchase on the website. Requires an account with access, online verification and an active SCS mod. |

A confirmed purchase unlocks the add-on in your account library. The panel links through a code authorized on the website; your password is not stored in the plugin. Accounts granted access manually by the administrator can also use the add-on.

Without online verification, smoke remains locked while the free braking system remains available. Density ranges from **0% to 500%**, with an on/off option in the panel. Emission is requested from **420 °C** per vehicle and stops once it cools to **380 °C or below**, with particles fading gradually.

## Current compatibility

**Windows x64 · ETS2 1.62.1.0 — executable recognized by the native integration.**

**American Truck Simulator support is in preparation.** Do not use or purchase 0.8.0 and its smoke add-on expecting ATS compatibility. Other game versions also require adaptation and validation. Support in older plugin versions does not guarantee support in this new system.

## Installation and updates

1. Close the game and keep a backup outside `plugins`.
2. Download the current base from the website. Copy its `plugins` contents to `Euro Truck Simulator 2\bin\win_x64\plugins`.
3. Keep **both DLLs**: `ets2_brake_fade.dll` and `cb_brake_smoke_probe.dll`, plus `cb_smoke_native.ini` and `sounds`. Despite its old name, the second DLL runs physics and particles and is required.
4. Remove duplicate old plugin DLLs and the diagnostic `cb_brake_physics_probe.dll`. Preserve `brake_fade_v07.ini` to keep your preferences.
5. Use original game controls. Remove the old virtual-axis assignment if present. Open the panel with **F10** or your saved shortcut.
6. For smoke, also copy the add-on's SCS file to `Documents\Euro Truck Simulator 2\mod`, enable it in Mod Manager and link your account through the panel. Use the Documents location configured in Windows.

**Full tutorials on the website (Portuguese):** [install the free base](https://cb-mods-road.wswmjkwr2r.chatgpt.site/install-base.html) · [install and activate smoke](https://cb-mods-road.wswmjkwr2r.chatgpt.site/install-smoke.html)

## Support and future work

On [Discord](https://discord.gg/yFgebpcX8), include game/mod versions, hardware, reproduction steps, `game.log.txt` and `brake_fade_v07.log`. Never share passwords or `account.dat`.

Priorities are stability, tests on more combinations and ATS adaptation. No release dates or universal compatibility are promised. Automated checks and player reports do not replace validation on each game version.

## Support development

The base is free. Donations are optional and separate from purchasing the smoke add-on.

[Buy Me a Coffee](https://buymeacoffee.com/cesnnabravo) · [Instagram](https://instagram.com/rodrigoaraujoca2/) · [Discord](https://discord.gg/yFgebpcX8)

PIX donation key — Rodrigo Araújo Campos: `c2ad1129-8267-4e80-a0b6-2e0ddb93526c`.

**Realism • Simulation • Immersion — CesnnaBravo**
