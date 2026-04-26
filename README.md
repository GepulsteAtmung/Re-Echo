<img width="1477" height="829" alt="image" src="https://github.com/user-attachments/assets/afa1fd8c-ec57-4b1a-bb1e-75e9853bc1bf" /><img width="1486" height="829" alt="image" src="https://github.com/user-attachments/assets/c941c941-58c5-4b99-96b3-66685cbaa30c" /># Re-Echo
ios galgame emu
# Re:Echo
**A Next-Generation Galgame Runtime Framework for iOS / iPadOS.**

Re:Echo is not just another desktop emulator ported to mobile. It is a native, extensible engine architecture designed from the ground up to integrate the Galgame experience seamlessly into the iOS ecosystem.

---

## 🌟 Key Features

### 📦 Seamless Import & Intelligent Detection
* **Zip Native Support:** Directly import `.zip` files. Re:Echo automatically identifies engine types and locates boot files.
* **Integrated Workflow:** Import, categorize, launch, full-screen, and save management—all within one clean, unified system.
* <img width="1478" height="827" alt="PixPin_2026-04-26_16-52-56" src="https://github.com/user-attachments/assets/1e43821e-d006-48a7-8ed0-a523c301f3db" />


### ⚙️ Under the Hood
* **Multi-Category Library:** Automated probing and sorting of your game collection.
* **True VM Visual Session:** For ONS, we don't just "display text." Re:Echo runs a full VM pipeline (Script, Graphics, Fonts, Audio, Saves).
* **Modern iPad Support.
<img width="1477" height="827" alt="PixPin_2026-04-26_16-57-39" src="https://github.com/user-attachments/assets/71f6e2c7-656c-407e-8eb2-c5ae30648db8" />


### 🖐️ Natural Interaction
Experience Galgames with gestures as natural as iPadOS itself:
* **Single Tap:** Advance text, maintain immersion.
* **Double Tap:** Summon HUD (Save, Load, Skip, Restart, Quit).
* **Auto-Hide HUD:** Controls disappear after 3 seconds of inactivity.

---

## 🛠 Engine Architecture
Re:Echo decouples the UI from engine specifics. Each runtime handles its own `Probe`, `Prepare`, and `Launch` logic.

**Workflow:**
`Import` ⮕ `Probe` ⮕ `Runtime` ⮕ `Session` ⮕ `Player`

---

## 📊 Roadmap

* **[NOW] ONS:** True VM visual playback, full audio/font support.
* **[NEXT] RPG & Ren'Py:** RPG2000/2003/XP detection and module implementation.
* **[LATER] krkr & macOS Companion:** Full krkr support and PC package conversion tools.

---

## 📱 Supported Devices
* **Hardware:** iPhone & iPad.
* **System:** Optimized for **iOS / iPadOS 26.0+**.
* <img width="1133" height="744" alt="截圖 2026-04-26 17 01 12" src="https://github.com/user-attachments/assets/8909110a-3e47-414d-94dd-d8e010c9ac89" />
