# Re-Echo
A simple and easy-to-use Galgame emulator built with modern SwiftUI
# Re:Echo

Re:Echo is a visual novel emulator project made in my spare time. Updates will be very slow. This is not a commercial product, and it is not a promise of fast, long-term maintenance for a full emulator suite. If you want to try it, please treat it primarily as an ONS emulator.

The project is built with modern SwiftUI and aims to provide a more native iPhone and iPad experience for galgame / visual novel playback. The library, import flow, player interface, and in-game HUD are designed around mobile devices instead of simply copying a desktop emulator window.

## Main Focus

- The current core use case is ONS / ONScripter-style games.
- Zip archives can be imported directly from the Files app.
- You do not need to manually extract the archive, browse folders, or find `0.txt`, `nscript.dat`, or other startup files yourself.
- The app tries to detect the playable game directory inside the archive and add it to the local library automatically.

## Direct Zip Import

Visual novel packages do not always use a consistent folder layout. Some archives contain an extra top-level folder, some include readme files or system files, and some may even contain nested archives. Re:Echo tries to hide part of that file-management work:

- Select a `.zip` file directly.
- Extract it into the local game library.
- Look for common ONS startup files automatically.
- Normalize common multi-level folder layouts.
- Launch the game from the library after import, without finding the same files again.
- App UI for iPhone and iPad:
<img width="1179" height="2404" alt="IMG_1702" src="https://github.com/user-attachments/assets/397f5736-30f2-42a7-9723-89940f81b5fc" />
<img width="2266" height="1434" alt="IMG_0459" src="https://github.com/user-attachments/assets/d81ba666-b765-401b-887d-1f4fb82a0255" />


This is one of the main problems the project tries to solve: less manual file handling on iOS, and more direct playing.

## Player And HUD

The player includes a mobile-oriented HUD for common controls and runtime state. The goal is not to recreate every complex desktop emulator menu, but to keep the touch experience lightweight and practical:
<img width="2266" height="1424" alt="IMG_0461" src="https://github.com/user-attachments/assets/6395e827-2d92-4554-807c-a0a2b103d875" />

- In-game floating control entry.
- Portrait and landscape support.
- Layout behavior adapted for different iPhone and iPad screen sizes.
- Stretch-to-fullscreen support, making older game visuals easier to fit on modern displays.
<img width="2425" height="1364" alt="IMG_1701" src="https://github.com/user-attachments/assets/b1214f21-d42c-4a2d-bc3a-fedb8c571360" />


Because visual novels vary widely in original resolution, asset ratio, and script behavior, fullscreen adaptation will not be perfect for every game. The goal is to provide a reasonable mobile viewing and control experience.

## Possible Future Directions

Future experiments may include:

- KRKR / Kirikiri support.
- Ren'Py support.
- Very limited execution of some exe-based games through a Mac-side packaging/conversion workflow.

These directions are difficult and time-consuming. Script compatibility, resource formats, plugins, fonts, audio, saves, platform APIs, and Windows runtime behavior can each become long-term work on their own. Please do not expect too much from these features, and do not treat this project as a complete KRKR, Ren'Py, or Windows galgame runner.

For now, please treat Re:Echo as an ONS emulator.

## Signing And Installation

This project is intended for personal use and testing. Free Apple ID signing expires quickly, so the app may need to be signed and installed again after the profile expires.

This project does not plan to support p12 signing or provide any signing service. 

## Project Status

This is a personal hobby project. Features will be refined slowly, and the project may stay in one stage for a long time. You are welcome to try it as an experimental iOS ONS emulator, but please do not expect it to become a universal all-engine, all-platform, all-format compatibility tool in the near future.
Compatibility: Requires iOS 26.0 or later.
