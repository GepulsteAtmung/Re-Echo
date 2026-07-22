<p align="right">
  <b>English</b> | 
  <a href="./ReEcho_README_ZH-TW.md">繁體中文</a> | 
  <a href="./ReEcho_README_JA.md">日本語</a>
</p>

---

Due to the lack of traction and interest, this project has been officially archived, and the associated release resources/downloads have been removed. Depending on future circumstances and feedback, I may consider refining the app and releasing it on the **App Store**. Thank you to everyone who previously checked out or supported this project.

# Re:Echo

> A Galgame and visual novel library and runtime for iOS, iPadOS, and macOS, built with modern SwiftUI.

Re:Echo is a personal hobby project developed in my spare time. It is not a commercial product, nor a promise of rapid, long-term maintenance for every engine and game format. The project began with ONS/ONScripter-style games as its core focus and now also experiments with RPG Maker, KrKr2, and PC Windows Galgame support on selected platforms.

The goal is not only to open a game. Re:Echo is intended to make importing, detection, organization, search, and launching feel like a native Apple-platform workflow. Users should not have to extract every archive, inspect several nested folders, and manually locate a startup file each time.

> Re:Echo does not provide games, copyrighted game assets, or commercial engine files. Only import content that you legally own and are authorized to use.

## Platform Overview

| Platform | Requirement | Primary use | Current engine entries |
| --- | --- | --- | --- |
| iOS | iOS 26.0 or later | A touch-first portable game library | ONS, RPG Maker MV/MZ |
| iPadOS | iPadOS 26.0 or later | Multi-column library and large-screen touch play | ONS, RPG Maker MV/MZ |
| macOS | macOS 26.0 or later on Apple silicon | Desktop library management, separate game windows, and additional engines | ONS, KrKr2, RPG Maker MV/MZ, PC Windows Galgame |

## iPhone: A Library Reworked for Touch

The iPhone version uses bottom tabs to separate Recent Games, ONS, RPG Maker, and experimental features. The entire collection is searchable, and frequently used titles are available from the recent-play history.

<p align="center">
  <img src="https://github.com/user-attachments/assets/f1da7830-fa37-4582-916f-7c3faff45477" alt="Recent Games and search in Re:Echo for iPhone" width="340" />
  <br />
  <sub style="color: gray;">Recent Games and search in Re:Echo for iPhone</sub>
</p>

Mobile highlights:

- Select ZIP packages or game folders through the Files app.
- Normalize common nested archive layouts automatically.
- Add detected content to the appropriate game library.
- Search the library and keep a recently played history.
- Adapt to portrait, landscape, and different iPhone sizes.
- Optionally enable the HUD and stretch-to-full-screen display.

## iPad: A Multi-Column Interface for the Larger Screen

The iPad version uses a sidebar, game list, and detail area. Switching engines, searching the collection, selecting a title, and launching it can all be done from one screen instead of fitting a traditional desktop emulator window onto a touch device.

<p align="center">
  <img src="https://github.com/user-attachments/assets/c494fc38-d3c8-4be0-8975-4f5eba495eec" alt="The multi-column Re:Echo library on iPadOS" width="1000" />
  <br />
  <sub style="color: gray;">The multi-column Re:Echo library on iPadOS</sub>
</p>

### Game HUD and Full Screen

A lightweight HUD can be opened during gameplay on iPhone and iPad. It currently keeps only Restart and Quit. Save, load, skip, and other game actions remain under the control of the engine and the game's own interface, reducing the risk of an extra control layer interfering with script behavior.

Stretch-to-full-screen can help older resolutions use more of a modern display. Both the HUD and stretch behavior can be disabled in Settings. Because original resolutions, aspect ratios, and scripts vary widely, stretched presentation will not be ideal for every title.

<p align="center">
  <img src="https://github.com/user-attachments/assets/f8437143-2824-435d-904d-554a8542e521" alt="The Re:Echo game HUD on iPadOS" width="1000" />
  <br />
  <sub style="color: gray;">The Re:Echo game HUD on iPadOS</sub>
</p>

## Mac: Desktop Library Management and Separate Game Windows

The macOS version is designed for Apple silicon and desktop workflows. The sidebar separates Engine Types from user-created PC Galgame folders. Games are presented as individual cover icons, with search, import, and refresh controls in the main window.

<p align="center">
  <img src="https://github.com/user-attachments/assets/6f71e9a6-ae30-4216-af27-4c8b4cd16c00" alt="The Re:Echo home library on macOS" width="1100" />
  <br />
  <sub style="color: gray;">The Re:Echo home library on macOS</sub>
</p>

Mac features include:

- Dedicated ONS, KrKr2, RPG Maker, and PC Windows Galgame entries.
- Custom PC game folders, with Untitled provided as the default.
- Direct ZIP or folder import with package analysis.
- Automatic selection of a likely cover from images found in the game.
- Rename, edit cover, toggle Metal HUD, and permanently delete actions.
- Separate game windows that do not replace the main library view.
- Full-screen, restart, and quit controls for the active game from the menu bar.

<p align="center">
  <img src="https://github.com/user-attachments/assets/db2097c1-5ad1-463c-b8e9-30b4108ad11a" alt="The Re:Echo library beside a separate ONS game window" width="1100" />
  <br />
  <sub style="color: gray;">The Re:Echo library beside a separate ONS game window</sub>
</p>


## Direct ZIP Import

Game packages do not follow one consistent directory layout. Some ZIP files include an extra top-level folder, some mix documentation and system files into the archive, and others place the actual game entry several levels deep. Re:Echo attempts to reduce that repetitive file work:

1. Select a `.zip` file or an already extracted game folder.
2. Import its contents into the app's local game library.
3. Scan for common engine signatures and startup files.
4. Normalize common multi-level folder layouts.
5. Add the result to the appropriate engine category or PC game folder.
6. Launch it directly from the Re:Echo library in the future.

An archive may still fail detection or execution if required files are absent, encryption is unsupported, or the package is only an update patch rather than a complete game.

## How It Works (Briefly)

Re:Echo selects an appropriate runtime from characteristic files in the imported package, then integrates graphics, audio, and input with a native Apple-platform interface. iPhone and iPad focus on touch and display adaptation; Mac uses separate windows plus keyboard and mouse input. PC Windows Galgame titles are attempted through a compatibility translation environment bundled with the app, without requiring users to install CrossOver separately.


## Compatibility

### Compatibility Levels

| Level | Meaning |
| --- | --- |
| Primary support | A core use case; general compatibility issues receive priority |
| Limited/experimental | Some titles run, but plug-ins, media, or platform differences may cause problems |
| Unsupported | No corresponding runtime is currently available, or the technical requirements are unsuitable for the app |

### ONS/ONScripter

**Status: Primary support.** ONS is available on iOS, iPadOS, and macOS.

More likely to run:

- ONS packages using common entries such as `0.txt`, `00.txt`, or `nscript.dat`.
- Complete, uncorrupted games using common image and audio formats.
- ZIP packages whose main complication is an extra top-level folder, documentation, or ordinary archive clutter.

May not run correctly:

- Titles relying on private commands from a particular ONS fork, external plug-ins, or modified engine behavior.
- Scripts that must load Windows DLLs, external EXE files, or other native modules.
- Content using unusual encryption, proprietary packages, or unsupported media codecs.
- Patch-only or incomplete archives, missing scripts or assets, and packages with filename case mismatches.
- Titles tightly coupled to desktop-only fonts, system paths, locale encodings, or nonstandard input methods.

### RPG Maker

**Status: Limited/experimental.** The current target is RPG Maker **MV/MZ** content.

More likely to run:

- MV/MZ packages containing complete web-game files, data, JavaScript, and asset directories.
- Titles built mostly with standard engine APIs and commonly supported web media formats.

May not run correctly:

- Plug-ins that depend on NW.js, Node.js, Electron, desktop filesystem APIs, or external programs.
- Packages requiring platform-specific native modules, Windows DLLs, or data produced only by an installer.
- Custom encryption, unusual video/audio codecs, or packages missing keys and required assets.
- Large plug-in stacks that substantially replace rendering, input, save, or networking behavior.

Currently unsupported:

- Native Windows releases from RPG Maker 2000/2003, XP, VX, and VX Ace.
- Packages that require the official editor, an installed RTP, or a Windows-only player to start.

### KrKr2/Kirikiri2 (macOS Only)

**Status: Limited/experimental.** There is currently no KrKr2 entry on iOS or iPadOS.

More likely to run:

- Kirikiri2-style titles with a standard startup script and complete data archives.
- Content relying mainly on built-in scripting, images, audio, and basic video playback.

May not run correctly:

- Titles depending on Windows DLLs, COM, ActiveX, external EXE files, or vendor-specific native plug-ins.
- Special XP3 encryption, license verification, proprietary unpacking, or DRM-protected content.
- Games requiring Windows-only video filters, legacy codecs, or a specific installed font environment.
- Kirikiri Z and heavily modified derivative engines; a KrKr2 entry does not imply support for every Kirikiri-family runtime.

### PC Windows Galgame (macOS Only)

**Status: Highly experimental.** This is not a complete Windows virtual machine and should not be treated as a commercially supported, universal Windows runtime.

More likely to run:

- Portable, traditional 2D games that can start directly from an extracted directory and have few dependencies.
- Titles that do not require drivers, account services, third-party launchers, or a complex installation process.
- Content based on common Windows APIs, DirectDraw/older graphics paths, and ordinary audio formats.

Usually unsupported or unlikely to work:

- Games with DRM, anti-cheat, online activation, kernel drivers, or mandatory third-party launchers.
- Titles requiring Windows system services, device drivers, proprietary codecs, or globally installed fonts.
- Installer-dependent games that require extensive registry state or several external runtimes and provide no portable game directory.
- Games requiring DirectX 12, modern high-end 3D, VR, specialized input hardware, or vendor GPU extensions.
- Unsupported 16-bit executables, driver-level protection, hardware keys, or other low-level Windows components.
- Packages where a launcher and the real game executable are separate but required components are missing.

## Cross-Platform Differences

- iOS and iPadOS do not execute Windows EXE files and do not include the Mac PC Galgame compatibility environment.
- KrKr2 is currently available only on macOS.
- RPG Maker support targets web-based MV/MZ games, not every generation of RPG Maker.
- Fonts, media playback, touch, keyboard input, and full-screen behavior may differ between devices.
- Saves are normally managed by the game and its runtime. Back up important saves before updating, deleting, or reimporting a title.

## Signing and Installation

The iOS/iPadOS project is intended mainly for personal use and testing. Apps signed with a free Apple ID expire quickly and may need to be signed and installed again. This project does not plan to provide P12 signing or any signing service.

The macOS edition currently targets Apple silicon and macOS 26.0 or later. System security settings, app signing, quarantine attributes, and the source of third-party game files can affect first launch.

## Project Status

Re:Echo is a personal hobby project. Updates may be slow, and some features may remain experimental for a long time. Work will generally prioritize fixes that improve an entire class of games rather than promises to adapt every title individually.

Please treat Re:Echo as an ONS-focused project that is gradually experimenting with other engines and platform capabilities, not as a universal all-engine, all-platform, all-format emulator expected in the near future.

## Links

- Developer: [GepulsteAtmung on GitHub](https://github.com/GepulsteAtmung)
- Discord: [Join the community](https://discord.gg/MeJkYV6ghj)

---

*Game footage in this document is shown only to demonstrate Re:Echo functionality. All games, characters, artwork, trademarks, and related materials remain the property of their respective rights holders.*
