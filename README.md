<!-- DRAFT for the public release repository github.com/Daniiel18/SimFleet. Not published. -->

<p align="center">
  <img src="media/cover.png" alt="SimFleet" width="720">
</p>

# SimFleet

**A Windows companion for Microsoft Flight Simulator 2020 and 2024: manage your Community folder, log every flight automatically, and keep a maintenance log whose failures show up in the aircraft.**

[![Latest release](https://img.shields.io/github/v/release/Daniiel18/SimFleet?label=download&color=2563eb)](https://github.com/Daniiel18/SimFleet/releases/latest)
[![Windows](https://img.shields.io/badge/Windows-10%20%7C%2011%20x64-0078D6)](#requirements)
[![MSFS](https://img.shields.io/badge/MSFS-2020%20%7C%202024-1e88e5)](#requirements)

SimFleet is free to use and closed source. This repository only holds the releases, the release notes and this page.

---

## Download

Get **`SimFleet_<version>_x64-setup.exe`** from the [latest release](https://github.com/Daniiel18/SimFleet/releases/latest). Each release also lists the installer's SHA-256 checksum.

## Features

**Community folder**
- Enable or disable add-ons in place (nothing is moved), save sets of add-ons and switch between them.
- Installs local archives (ZIP, 7z, RAR) by drag and drop into the right simulator's Community folder.
- Add-on updates, documentation, scenery conflicts, MSFS 2024 `Content.xml` manager and cache optimizer.

**Flying**
- **FlightBook:** every flight logged automatically through SimConnect: route, track, phases, landing rate and score.
- **Best Landings:** records the touchdown and keeps the clip with its thumbnail; plays inside the app.
- **Tech Log:** wear of each part by flight hours, cycles and how the aircraft was flown. On the **Fenix A319/A320/A321** and the **PMDG 737 and 777**, failed parts appear as real failures in the aircraft and go away when repaired.
- **Hangar and economy:** fleet analytics, maintenance costs and an airline balance built from your flights.

**Integrations**
- SimBrief (flight plans and dispatch), GSX Pro, TechLog, Discord status, optional Google Drive sync to your own Drive.
- AMD Adrenalin fix for MSFS: keeps the recording microphone, the MSFS detection and your saved graphics settings.

## Screenshots

| Dashboard | FlightBook | Hangar |
|---|---|---|
| ![Dashboard](media/dashboard.png) | ![FlightBook](media/flightbook.png) | ![Hangar](media/hangar.png) |

## Requirements

- Windows 10 or 11, 64-bit, with the Microsoft Edge WebView2 Runtime (included in current Windows).
- Microsoft Flight Simulator 2020 or 2024 (Steam or Microsoft Store).
- Optional: GSX Pro, a SimBrief account, a Google account for sync, AMD Adrenalin for its fix.

## Install

1. Download the installer from the [latest release](https://github.com/Daniiel18/SimFleet/releases/latest).
2. Run it. The installer is not code-signed, so Windows SmartScreen may warn the first time: choose **More info → Run anyway**.
3. Open SimFleet and pick your simulator on the first start.

Your data stays on your PC: in a `data` folder next to SimFleet, or in `%LOCALAPPDATA%\SimFleet\data` if that folder is not writable.

## Updating

SimFleet checks this repository's latest release when it starts and every 15 minutes, and offers to install it. It installs an update only when the installer matches the SHA-256 checksum GitHub publishes for it. Only the release information is requested; nothing about you is sent. Automatic checks can be turned off in Settings › General (Look for app updates).

## Settings worth knowing

- **Failures in the aircraft** (Settings › Flight & sim › Maintenance): on by default. PMDG failures need PMDG's licence accepted once inside SimFleet.
- **AMD Adrenalin** (Settings › Flight & sim): Windows asks once for permission, because AMD only lets its service be closed with administrator rights.
- **Desktop notices** (Settings › General): small notices over the sim when a download finishes or something fails while SimFleet is in the background; they can be turned off.

## Troubleshooting

- **No flight is being logged:** start MSFS first, then check the connection badge at the top of SimFleet.
- **PMDG failures do not appear:** the right CDU must have power; SimFleet waits while you are typing in it.
- **Anything else:** open Settings › Folders & backup › Folders › Logs and attach the latest `simfleet.<date>.log` to your issue.

## Known limitations

- Failures in the aircraft are only for the Fenix and the PMDG 737 and 777; other aircraft keep the Tech Log without failures, because they have no public interface for it.
- If TechLog is installed, it manages the failures and SimFleet stays out.
- Windows only.

## Support

Open an [issue](https://github.com/Daniiel18/SimFleet/issues) with your Windows version, your simulator (2020 or 2024, Steam or Store), the SimFleet version and the steps to reproduce.

## Licence

Free to use, closed source, all rights reserved. See [LICENSE](LICENSE.txt). SimFleet is not affiliated with Microsoft, Asobo, Fenix, PMDG, FSDreamTeam, SimBrief or AMD; all trademarks belong to their owners.
