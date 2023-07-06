# Cemu is a Wii U Emulator.

Website: https://cemu.info/

Github: https://github.com/cemu-project/Cemu

Compatibility List: https://compat.cemu.info/

**This page is for the native build of Cemu. EmuDeck includes the native build of Cemu as an optional install. Both versions will remain installed. One quick way to tell the difference is to compare the two GUIs. For the Proton version of Cemu, visit https://github.com/dragoonDorise/EmuDeck/wiki/Cemu-Proton.**

Native Cemu: <img src="https://user-images.githubusercontent.com/108900299/226765451-f9e712cd-f6c5-4257-8821-8957f28b3745.png" height="300">

Proton Cemu: <img src="https://user-images.githubusercontent.com/108900299/226765705-e8aa00ff-d647-4965-9e8a-253dfb36f289.png" height="300">

***

# Cemu Native Table of Contents

1. [Getting started with Cemu](#getting-started-with-cemu)
    - [Setting up Cemu Questionnaire](#setting-up-cemu-questionnaire)
    - [Configuration](#cemu-native-configuration)
    - [The Dangers of Proton](#the-dangers-of-proton)
    - [How to Update Cemu](#how-to-update-cemu)
    - [How to Launch Cemu in Desktop Mode](#how-to-launch-cemu-in-desktop-mode)
    - [File Formats](#cemu-native-file-formats)
    - [How to Convert to WUA](#how-to-convert-to-wua)
    - [How to Manage DLC and Updates](#how-to-manage-dlc-and-updates)
    - [Hotkeys](#cemu-native-hotkeys)

2. [Common Issues](#common-issues)
    - [Game Compatibility](#game-compatibility)
    - [Cemu Version Issues](#cemu-version-issues)

3. [Cemu Tips and Tricks](#cemu-tips-and-tricks)
    - [How to Configure Gyro](#how-to-configure-gyro)
    - [How to Configure Gyro With External Controllers](#how-to-configure-gyro-with-external-controllers)
    - [How to Optimize Performance (Power Tools)](#how-to-optimize-performance-power-tools)
    - [How to Configure Multiplayer](#how-to-configure-multiplayer)
    - [How to Use the Wii U Pro Controller Configuration](#how-to-use-the-wii-u-pro-controller-configuration)
    - [How to Configure Cemu Native to Work With EmulationStation-DE](#how-to-configure-cemu-native-to-work-with-emulationstation-de)
    - [How to Optimize Breath of the Wild](#how-to-optimize-breath-of-the-wild)

***

# Getting started with Cemu
[Back to the Top](#cemu-native-table-of-contents)

**IMPORTANT:** Cemu is shifting away from encrypted ROMs (WUX, WUD). It is strongly recommended you use decrypted ROMs (Loadiine, WUA). Decrypted ROMs do not need any additional configuration and should launch without any issue.

Cemu is a fairly straight-forward emulator to set up, _if_ you use decrypted ROMs. Place your ROMs in `Emulation/roms/wiiu/roms`. **Do not** install your games. No additional setup is required. 

Read the [Configuration](#cemu-proton-configuration) section to learn more about Cemu and its folder locations. 

For updates and DLC, read [How to Manage DLC and Updates](#how-to-manage-dlc-and-updates).  

To launch your ROMs in game mode, use Steam ROM Manager and use one of the following parsers to play your Wii U ROMs:

* `EmulationStation-DE`
* `Nintendo WiiU - Cemu (.rpx) - Native` or `Nintendo WiiU - Cemu (.wud, .wux, .wua) - Native`
    * Read the [File Formats](#file-formats) section to learn more about these various file formats
    * `.rpx` and `.wua` are decrypted ROM formats
* `Emulators`

_If_ you intend on using encrypted ROMs, proceed to the [Setting up Cemu Questionnaire](#setting-up-cemu-questionnaire). 

***

## Setting up Cemu Questionnaire
[Back to the Top](#cemu-native-table-of-contents)

**IMPORTANT:** Cemu is shifting away from encrypted ROMs (WUX, WUD). It is strongly recommended you use decrypted ROMs (Loadiine, WUA). Decrypted ROMs do not need any additional configuration and should launch without any issue. If you use decrypted ROMs, you do not need the following questionnaire. 

**Setting up Cemu Questionnaire**

1. Is your ROM encrypted? If yes, do you have a `keys.txt` in the right place with the correct keys for your games in the `keys.txt` file?
    1. What are keys?: Keys are required to decrypt Wii U ROMs. Your `keys.txt` needs to contain keys (one key per game) that must be dumped from a Wii U console. Any other method of obtaining keys is piracy and cannot be discussed here or on the EmuDeck discord.
    2. Which Cemu ROM Formats are encrypted?: [File Formats](#file-formats)
    3. `keys.txt` Location: `/home/deck/.local/share/Cemu/`
    4. If your ROM is NUS Format (a folder with .h3 and .app files), you will need to decrypt your ROM into the Loadiine format (folder format with three subfolders - code, content, meta). Decryption methods cannot be discussed here or on the EmuDeck discord.
2. Is your ROM decrypted?
    1. Which Cemu ROM Formats are decrypted?: [File Formats](#cemu-native-file-formats)
    2. If your ROM is decrypted, place the ROM in `Emulation/roms/wiiu/roms`. Your game should launch without needing any keys. 
3. If you are getting an `Unable to launch game` error, did you place the `keys.txt` in the right place?
    1. `keys.txt` Location: `/home/deck/.local/share/Cemu/`
4. If you placed the `keys.txt` in the right place, and your ROM is still not working, does your `keys.txt` have the correct key for the ROM?
    1. Even if you placed a key for your game in `keys.txt`, you may still have the incorrect key. 
5. Did you transfer your ROM from another computer and did you compare file sizes to ensure it transferred successfully? 
6. Did you turn on Proton in Steam? If yes, turn it off. If you are unsure, check.
    1. How do I check?: [The Dangers of Proton](#the-dangers-of-proton)


***

## Cemu Native Configuration
[Back to the Top](#cemu-native-table-of-contents)

**IMPORTANT:** Cemu is shifting away from encrypted ROMs (WUX, WUD). It is strongly recommended you use decrypted ROMs (Loadiine, WUA). Decrypted ROMs do not need any additional configuration and should launch without any issue.

* Type of Emulator: AppImage
* Executable Location:  `/home/deck/Applications/Cemu.AppImage`
* Configuration: `/home/deck/.config/Cemu/`
* Emulator Folders Location: 
    * `/home/deck/.config/Cemu/` 
        * Contains the following folders and files: 
            * `controllerProfiles`
            * `gameProfiles`
            * `settings.xml`
    * `/home/deck/.local/share/Cemu/`
        * Contains the following folders and files: 
            * `graphicPacks`
            * `memorySearcher`
            * `log.txt`
            * `title_list_cache.xml`
    * `/home/deck/.cache/Cemu`
        * Contains the following folders and files: 
            * `shaderCache`
* Persistent Storage: `Emulation/roms/wiiu/mlc01/`
* ROM Location: `Emulation/roms/wiiu/roms` 
    * Note the second `roms` folder in the path. 
    * Do not put DLC / update files in the ROM path. Refer to [How to Manage DLC and Updates](#how-to-manage-dlc-and-updates)
    * Place your game ROMs here, **do not** install your game ROMs
* `keys.txt` Location: `/home/deck/.local/share/Cemu/`
    * The `keys.txt` is only necessary if the Wii U ROM is encrypted.
    * `keys.txt` needs to contain keys (one key per game) that must be dumped from a Wii U console. Any other method of obtaining keys is piracy and cannot be discussed here or on the EmuDeck discord.
* Saves Location:
    * Symlink:  `Emulation/saves/Cemu/saves/`
    * Target: `Emulation/roms/wiiu/mlc01/usr/save`

### Works With
* Steam ROM Manager
* EmulationStation-DE

***

## The Dangers of Proton
[Back to the Top](#cemu-native-table-of-contents)

**IMPORTANT:**

There is outdated info on the internet that indicates you need to set Proton on Cemu or on games added for this console by Steam ROM Manager in Steam. Turning on Proton is not necessary. **DO NOT set Proton Compatibity on Cemu or Cemu games added to Steam.** Do NOT set `STEAM_COMPAT_MOUNTS` in parameters.

**Turning on Proton is not necessary because this is the native linux version of Cemu.**

Do not open the `Compatibility` screen in `Game Mode`. Do not touch any of the settings on the `Compatibility` screen in `Game Mode`. 

<img width="500" alt="proton" src="https://user-images.githubusercontent.com/108900299/194777064-526930f4-c36c-44be-b26a-ec192375ef7b.png">

***

## How to Update Cemu
[Back to the Top](#cemu-native-table-of-contents)

**How to Update Cemu**

* Through the `Update your Emulators & Tools` section on the `Manage Emulators` page in the `EmuDeck` application
* Manual file replacement of `Cemu.AppImage` 
    * Refer to https://github.com/dragoonDorise/EmuDeck/wiki/File-Management#how-to-swap-out-appimages-and-binaries for instructions 

***

## How to Launch Cemu in Desktop Mode
[Back to the Top](#cemu-native-table-of-contents)

**How to Launch Cemu in Desktop Mode**

* Launch `Cemu AppImage` from the `Applications Launcher` (Steam Deck icon in the bottom left of the taskbar)
* Launch the script from `Emulation/tools/launchers`, `cemu.sh`
* Launch the emulator from `Steam` after adding it via the `Emulators` parser in `Steam ROM Manager` 

***

## Cemu Native File Formats
[Back to the Top](#cemu-native-table-of-contents)

* Loadiine (rpx)
    * Three folders (code, content, meta) 
    * Folders should be inside a folder with the name of the game. This game folder is placed in `Emulation/roms/wiiu/roms` (note the second `roms`)
    * **Visual Reference:** <img src="https://user-images.githubusercontent.com/108900299/194643616-cdf86618-1869-4ba5-b95e-f14066e77ac1.png" width="300">
    * Decrypted, does not require `keys.txt` 
* WUA 
    * Decrypted, does not require `keys.txt`
* WUX
    * Encrypted, requires `keys.txt` in `/home/deck/.local/share/Cemu/`
* WUD 
    * Encrypted, requires `keys.txt` in `/home/deck/.local/share/Cemu/`
* NUS
    * A folder with `.h3` and `.app` files
    * Encrypted, can be decrypted into a `Loadiine (rpx)` folder. Decryption methods cannot be discussed here or on the EmuDeck discord.

**IMPORTANT:**

* Some of these formats may require keys. We cannot help you get these. Place your `keys.txt` in: `/home/deck/.local/share/Cemu/`
    * `keys.txt` needs to contain keys (one key per game) that must be dumped from a Wii U console. Any other method is piracy and cannot be discussed here or on the EmuDeck discord.
* Once you put ROMs in place, you must refresh the list of games by right clicking in the Cemu UI and clicking `Refresh Games List`.
    * Your game will not show up in Cemu until you refresh. 
* Refer to #installing-dlc-and-updates, for DLC and Updates. 

***

## How to Convert to WUA
[Back to the Top](#cemu-native-table-of-contents)

The WUA format is a compressed version of the Loadiine format. It contains your base game, DLC, and updates all in one single file. The WUA format is a lot less fuss than the other formats, requires no keys, and is the most friendly format for EmulationStation-DE.

Here's how to convert to WUA:

**Note:** 
* Encrypted ROMs (WUX, WUD, NUS) cannot be converted to WUA

**Tutorial**

1. Open Cemu
2. Click `Tools`, `Title Manager`
    1. <img src="https://user-images.githubusercontent.com/108900299/226769311-0c9961f3-57d8-48fe-a7d9-babafcfc761f.png" height="300">
3. Either search for your ROM or find it in the list
4. Select the ROM with the word `base` in the `Type` column
    1. <img src="https://user-images.githubusercontent.com/108900299/226769442-cad00efe-9a9b-4d28-a461-e55cb7e2e4a8.png" height="300">
5. Verify the pop-up prompt has your base game, your update, and your DLC files
    1. You can either place these update and DLC files in `Emulation/roms/wiiu/roms` temporarily or install them: #installing-dlc-and-updates
6. Wait, it may take a while
7. Right click in Cemu, and click `Refresh Game List` to refresh your file path in Cemu to the newly created WUA file

***

## How to Manage DLC and Updates
[Back to the Top](#cemu-native-table-of-contents)

### Preface

DLC and Updates must be installed using the title manager. DLC and Updates are saved to mlc01, in the `Emulation/roms/wiiu` folder.

**IMPORTANT:** Do not keep your DLC and update files in `Emulation/roms/wiiu/roms`. After installing these, you may either delete or move the files to a backup location. Keeping DLC and update files in this directory will create duplicates in Steam ROM Manager.  

***

## How to Install DLC and Updates
[Back to the Top](#cemu-native-table-of-contents)

### Preface

DLC and Updates must be installed using the title manager. DLC and UPdates are saved to mlc01, in the `Emulation/roms/wiiu` folder.

**IMPORTANT:** Do not keep your DLC and update files in `Emulation/roms/wiiu/roms`. After installing them, you may either delete them or move them to a backup location. Keeping DLC and update files in this directory will create duplicates in Steam ROM Manager.  

***

### How to Install DLC and Updates

1. Launch Cemu on Desktop Mode
2. Click `File` in the top left, click `Install game title, update, or DLC...`
   * Visual Reference: <img src="https://user-images.githubusercontent.com/108900299/226768498-90501d46-1656-4ade-b52d-615c80f73fef.png" height="300">
3. Navigate to to your Update or DLC files
   * If your files are on your SD Card, click `Other Locations`, `Computer`, `run`, `media`, and navigate to your SD Card
   * Example SD Card Path: `/run/media/mmcblk0p1`
4. Select the Update or DLC and click `Open`
   1. Visual Reference: <img src="https://user-images.githubusercontent.com/108900299/226768959-2078b493-e542-4d16-a42f-b5f8372d809d.png" height="300">
5. Wait a moment, and your DLC or update will be successfully installed. Repeat for each DLC or update


***

## Cemu Native Hotkeys
[Back to the Top](#cemu-native-table-of-contents)

Cemu comes with a Steam Input profile for Hotkeys. Activate the Steam Input profile by clicking the `Game Controller` icon in `Game Mode`, change the template to `Emudeck - Cemu`. The hotkeys below can only be used if you have the Steam Input profile active.

|  Hotkey                 | Cemu           |
|-------------------------|----------------|
|  Toggle Screens         | `L4` or `R4`    |
|  Swap Screens           | `L5` or `R5`    |
|  Exit                   | `Select` + `Start` |
|  Blow Mic               | `R3`    |

**Note:** 

* The `Blow Mic` hotkey only works if you are using the gamepad. 

For a tutorial on how to select Steam Input Profiles, refer to: https://github.com/dragoonDorise/EmuDeck/wiki/hotkeys#how-to-select-a-steam-input-profile.

**Steam Deck Button Layout:** https://github.com/dragoonDorise/EmuDeck/wiki/Hotkeys#steam-deck-button-layout

***

# Common Issues
[Back to the Top](#cemu-native-table-of-contents)

***

## Game Compatibility
[Back to the Top](#cemu-native-table-of-contents)

This section collects which games currently do not work on the native version of Cemu. These games likely work on the proton version of Cemu.

* Tekken Tag Tournament 2 
  * Date added to this page: May 6th, 2023 

***

## Cemu Version Issues
[Back to the Top](#cemu-native-table-of-contents)

This section collects a version history of Cemu and seeks to detail compatibility and general issues with the emulator.

* Cemu Version 2.0.36
  * No Known Issues
  * Date added to this page: May 6th, 2023 

***

# Cemu Tips and Tricks
[Back to the Top](#cemu-native-table-of-contents)

***

## How to Configure Gyro
[Back to the Top](#cemu-native-table-of-contents)

Gyro for Cemu requires SteamDeckGyroDSU. SteamDeckGyroDSU can be installed via EmuDeck, or it can be installed manually.

Visit https://github.com/dragoonDorise/EmuDeck/wiki/EmuDeck-Application-101#steamdeckgyrodsu to learn how to install and utilize SteamDeckGyroDSU. 


***

## How to Configure Gyro With External Controllers
[Back to the Top](#cemu-native-table-of-contents)

Some external controllers, including the Sony DualSense and the Nintendo Switch Pro Controller feature gyro controls. Cemu allows you to use this gyro with a little bit of set up.



**Here's How**

### Desktop Mode

1. In Desktop Mode, exit out of Steam
    * Your controls will switch to `Lizard Mode`. Use `L2` to right click, `R2` to left click, and the `Right Trackpad` to move the mouse
2. Click the bluetooth icon in the bottom right of your taskbar and connect your controller
    * <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/24945d4c-df06-4fbe-9668-7becea0c5edb" height="300">
3. Click the Steam icon in the bottom left of the taskbar and open `Cemu AppImage` 
    * <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/e395d988-cf13-4b2c-af2c-e27059b44ac2" height="300">
4. At the top of the Cemu GUI, click `Options`, click `Input settings`
5. Under the `Controller 1` tab, press the `-` button to the right of the `Controller` drop-down twice
    * <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/d2b7eb25-e5a2-4140-9c8e-069e5c465ab5" height="300">
6. The drop-down box will be empty and your controls will no longer be mapped, this is expected behavior
    * <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/c38668d2-a128-415a-b4fa-756e4e254c53" height="300">
7. Under the `Controller 1` tab, press the `+` button to the right of the `Controller` drop-down
    * <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/3f0e4a6b-5355-420f-9def-5423cc1c0116" height="300">
8. Select `SDLController` for the `API` drop-down and select your controller under the `Controller` drop-down
    * <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/10c359ca-0737-4c47-bbd9-c095777cfd42" height="300">
9. Click the `Add` button and Cemu will auto-map your controls
10. Click the `Settings` button under the drop-down with your controller name
11. Check the box to the left of `Use motion`
    * <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/388f1867-dd5d-4eb1-bd9f-d0fbf39896d8" height="300">
12. Click the `OK` button 
13. Give the profile a unique name under the `Profile` drop-down box at the top and click `Save`
    * <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/5c64751c-041f-40a5-86a5-bc8c6615eb58" height="300">
14. Your controller is now configured with gyro, proceed to the `Game Mode` section to start using your controller in `Game Mode`

### Game Mode

1. In Game Mode, connect your controller
2. Select your Wii U game 
3. On the `Play` screen, select the `Controller` icon to the right of the screen 
    * <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/468d63e3-534c-4270-ac61-06e167d6df48" height="300">
4. Select your controller tab at the top
    * <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/b51a1405-9cdf-4ba3-bebf-db817f057f63" height="300">
5. Click the `Gear` icon to the right, and click `Disable Steam Input`
    * <img src="https://github.com/dragoonDorise/EmuDeck/assets/108900299/33cbcb8e-a444-4a75-8e4a-ba9451e6e07a" height="300">
6. Your controller's gyro will now work for this selected game, repeat as needed for your other games

### Post-Configuration

This section went over creating a new Player 1 profile for your external controller.

To switch between your new controller profile and the Steam Deck controller profile, open Cemu and open the input settings, select your preferred option in the `Profile` drop-down menu and click `Load`.

To switch back to the Steam Deck controls, select the `Deck-Gamepad-Gyro` profile:

<img src="https://github-production-user-asset-6210df.s3.amazonaws.com/108900299/242173410-54e3d6fb-a38b-499e-ba1a-f65e809ef439.png" height="300">

***

## How to Optimize Performance (Power Tools)
[Back to the Top](#cemu-native-table-of-contents)

Visit https://github.com/dragoonDorise/EmuDeck/wiki/EmuDeck-Application-101#power-tools to learn how to optimize performance using Power Tools. 

***

## How to Configure Multiplayer
[Back to the Top](#cemu-native-table-of-contents)

1. Open Cemu
2. It's recommended you enable multiplayer on a per-game basis. Turning on additional controllers can disable single player controls in a handful of games
3. Right click a game, click `Edit Game Profile`
4. Click `Controller`
5. To the right of each Controller (`Controller 2` through `Controller 4`), select the respective `Deck #` profile (Deck 2 for player 2 and so on)

<img src="https://user-images.githubusercontent.com/108900299/226769760-abc659a8-4ddb-420b-9c33-b98043f27756.png" height="300">

***

## How to Use the Wii U Pro Controller Configuration
[Back to the Top](#cemu-native-table-of-contents)

In some some games, the initial screen will prompt for a controller configuration: `Wii U Gamepad` or `Wii U Pro Controller`. Some games will automatically switch to the `Wii U Pro Controller` configuration if you choose it. 

For example: <img src="https://user-images.githubusercontent.com/108900299/214977370-2e0fece0-4166-45ea-b373-5599b4d2b7ca.png" height="400">

If you prefer to use the `Wii U Pro Controller` layout, you need to change the controller profile in Cemu. Make sure to change controller profiles on a per-game basis so it is persistent on EmuDeck updates.

**Tutorial**

1. Right click the game, click `Edit game profile`
2. Click the `Controller` tab
3. Change the profile to `Deck-P1`
    * <img src="https://user-images.githubusercontent.com/108900299/226769652-9696e8f7-a91e-46e7-a553-156037b7e39e.png" height="300">
4. When you launch a game, one of the following two things will happen: 
    * Some games will prompt you to choose a controller layout, select the `Wii U Pro Controller`
    * Some games will automatically switch to the `Wii U Pro Controller` configuration

*** 

## How to Configure Cemu Native to Work With EmulationStation-DE
[Back to the Top](#cemu-native-table-of-contents)

In order to use Cemu Native through EmulationStation-DE, you will have to enable it in the settings menu.

**Here's How**

1. Open EmulationStation-DE
2. Press `Start`
3. Press `Other Settings`
4. Press `Alternative Emulators`
5. On `Wiiu`, select `Cemu [Native]`

***

## How to Optimize Breath of the Wild
[Back to the Top](-proton#cemu-table-of-contents)

**IMPORTANT:** You need Version 208 of Breath of the Wild to use FPS++. Read [How to Manage DLC and Updates](#how-to-manage-dlc-and-updates) to learn how to install game updates for Cemu. 

### How to Configure Cemu

1. In Desktop Mode, open `Cemu AppImage`
2. Right click `Breath of the Wild`, click `Edit graphic packs`
    * <img src="https://user-images.githubusercontent.com/108900299/236599933-8b568386-64ca-4bf3-8573-96c2374c46ce.png" height="300">  
3. Click `Download latest community graphic packs`
4. Click the `⌄` to the left of `Mods` 
5. Check the box to the left of `FPS++`
6. Change the mode to `Advanced Settings`
7. Change the `Framerate Limit` to `40FPS`
    * <img src="https://user-images.githubusercontent.com/108900299/236599985-df1ac9fe-1c0f-48a0-8fcd-adb15688f71c.png" height="300">
8. Close out of Cemu

### How to Configure Game Mode

1. In Game Mode, open Breath of the Wild
2. Click the `...` (the QAM) button
3. Click the battery icon
4. Click `Advanced View`
5. Enable `Use per-game profile`
6. Set the refresh rate to 40
    * <img src="https://user-images.githubusercontent.com/108900299/236642316-5bafc264-6c82-479c-988a-b419515ee92b.png" height="300">
7. Read https://github.com/dragoonDorise/EmuDeck/wiki/EmuDeck-Application-101#power-tools to learn how to use the battery menu and `Power Tools` to further increase performance for Breath of the Wild

After doing the steps in the above two sections, Breath of the Wild will run at a stable 40 FPS with temporary occasional hiccups in new areas while it compiles shaders.


*** 