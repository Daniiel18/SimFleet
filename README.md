# SimFleet

**A Windows companion for Microsoft Flight Simulator 2020 and 2024: manage your Community folder, log every flight automatically, and keep a maintenance log whose failures show up in the aircraft.**

[![Latest release](https://img.shields.io/github/v/release/Daniiel18/SimFleet?label=download&color=2563eb)](https://github.com/Daniiel18/SimFleet/releases/latest)
[![Windows](https://img.shields.io/badge/Windows-10%20%7C%2011%20x64-0078D6)](#requirements)
[![MSFS](https://img.shields.io/badge/MSFS-2020%20%7C%202024-1e88e5)](#requirements)

SimFleet is closed source and runs with a licence linked to your Google account. This repository only holds the releases, the release notes and this page.

**Current version: 10.1.0** · [release notes](https://github.com/Daniiel18/SimFleet/releases/latest)

---

## What's new in 10.1.0

- **Your GPU tuning stays.** "Save my settings" also saves AMD Adrenalin's Performance › Tuning (voltage, clocks, power limit, VRAM, fan curve, Zero RPM). If Adrenalin loses it after a crash or a driver update, SimFleet puts it back on its own, live, without closing Adrenalin.
- **Recommended tuning for any AMD card.** On a card that is still on factory values, SimFleet offers once a cautious tuning: 50 mV less voltage, the power limit at its maximum and a fan curve that cools earlier. Nothing is applied without your OK.
- **Safe with crashes and drivers.** A tuning that keeps getting lost is softened or removed, with a notice. Nothing is touched while the AMD driver is being installed, and every value is checked against the new driver's limits.

Earlier versions: see [all releases](https://github.com/Daniiel18/SimFleet/releases).

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
- AMD Adrenalin for MSFS: keeps the recording microphone, the MSFS detection, your saved graphics settings and your GPU tuning (voltage, power, fan curve), and offers a recommended tuning for AMD cards on factory values.

## Requirements

- Windows 10 or 11, 64-bit, with the Microsoft Edge WebView2 Runtime (included in current Windows).
- Microsoft Flight Simulator 2020 or 2024 (Steam or Microsoft Store).
- A Google account and an active SimFleet licence (see [Licence and sign-in](#licence-and-sign-in)).
- Optional: GSX Pro, a SimBrief account, Google Drive for sync, an AMD card with Adrenalin for its tools.

## Install

1. Download the installer from the [latest release](https://github.com/Daniiel18/SimFleet/releases/latest).
2. Run it. The installer is not code-signed, so Windows SmartScreen may warn the first time: choose **More info → Run anyway**.
3. Open SimFleet, sign in with your Google account, and pick your simulator on the first start.

### Licence and sign-in

- A new account waits until its licence is activated; SimFleet shows "licence pending" until then.
- Each licence works on **one PC**. It keeps working up to **7 days without internet** and asks you to sign in with Google again every **30 days**.
- Signing out frees the PC, so the licence can be used on another one.
- What the licence server keeps is described in [SECURITY.md](SECURITY.md#data--privacy).

Your data stays on your PC: in a `data` folder next to SimFleet, or in `%LOCALAPPDATA%\SimFleet\data` if that folder is not writable.

## Updating

SimFleet checks this repository's latest release when it starts and every 15 minutes, and offers to install it. It installs an update only when the installer matches the SHA-256 checksum GitHub publishes for it. Only the release information is requested; nothing about you is sent. Automatic checks can be turned off in Settings › General (Look for app updates).

## Settings worth knowing

- **Failures in the aircraft** (Settings › Flight & sim › Maintenance): on by default. PMDG failures need PMDG's licence accepted once inside SimFleet.
- **AMD Adrenalin** (Settings › Flight & sim): Windows asks once for permission, because AMD only lets its service be closed with administrator rights. "Save my settings" keeps both your MSFS graphics settings and your GPU tuning; a change you make in Adrenalin on purpose is never undone, save it again to keep it.
- **Desktop notices** (Settings › General): small notices over the sim when a download finishes or something fails while SimFleet is in the background; they can be turned off.

## Troubleshooting

- **No flight is being logged:** start MSFS first, then check the connection badge at the top of SimFleet.
- **PMDG failures do not appear:** the right CDU must have power; SimFleet waits while you are typing in it.
- **Anything else:** open Settings › Folders & backup › Folders › Logs and attach the latest `simfleet.<date>.log` to your issue.

## Known limitations

- Failures in the aircraft are only for the Fenix and the PMDG 737 and 777; other aircraft keep the Tech Log without failures, because they have no public interface for it.
- If TechLog is installed, it manages the failures and SimFleet stays out.
- GPU tuning is for AMD cards only. On the RX 6000 series the voltage can't be set through AMD's API, so only the power limit and the fans are tuned.
- Windows only.

## Support

Open an [issue](https://github.com/Daniiel18/SimFleet/issues) with your Windows version, your simulator (2020 or 2024, Steam or Store), the SimFleet version and the steps to reproduce.

## Licence

Closed source, all rights reserved; using SimFleet needs an active licence. See [LICENSE](LICENSE.txt). SimFleet is not affiliated with Microsoft, Asobo, Fenix, PMDG, FSDreamTeam, SimBrief or AMD; all trademarks belong to their owners.
