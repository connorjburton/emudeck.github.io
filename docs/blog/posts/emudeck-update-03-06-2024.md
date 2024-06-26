---
draft: false 
date: 2024-03-06T13:00:00
categories:
  - EmuDeck
---

[TOC]

## GUI

* Fresh coat of paint
    * The application has been redesigned with a fancy new GUI

## Emulators

* BigPEmu (New emulator!)
    * Added BigPEmu to EmuDeck
    * [#775](https://github.com/dragoonDorise/EmuDeck/pull/775)
* Cemu
    * Fixed controls and audio not properly applying
        * [#1008](https://github.com/dragoonDorise/EmuDeck/pull/1008)
    * Switched to Cemu Native as the default
* Dolphin
    * Enabled VI Skip by default
        * [#737](https://github.com/dragoonDorise/EmuDeck/pull/737)
    * Switched all profiles to SDL
        * This fixes the long-standing issue of controllers not working after waking up the Steam Deck from sleep 
        * [#928](https://github.com/dragoonDorise/EmuDeck/pull/928)
    * Added a new GameCube profile mapped to the Xbox Layout
* DuckStation
    * Fixed conflicting "Quick Menu" and "Toggle Software Rendering" hotkeys, see [DuckStation Hotkeys](../../emulators/steamos/duckstation.md#duckstation-hotkeys) for an updated list
* Flycast (New emulator!)
    * Added Flycast to EmuDeck
        * [#617](https://github.com/dragoonDorise/EmuDeck/pull/617)
    * Fixed GUI scaling bug in Game Mode
* MAME
    * Fixed settings not applying properly in the GUI
    * Added a `Cheats` folder to `Emulation/storage/mame`
    * Added OOTB support for light gun games using the Steam Deck trackpad
* melonDS
    * Fixed cheats not applying properly
* Model 2 Emulator (New emulator!)
    * Added the Model 2 Emulator to EmuDeck
        * [#959](https://github.com/dragoonDorise/EmuDeck/pull/959)
* PPSSPP
    * Added combo hotkeys, see [PPSSPP Hotkeys](../../emulators/steamos/ppsspp.md#ppsspp-hotkeys) for a full list
    * Added CHD support for PPSSPP in Steam ROM Manager
    * Added RetroAchievements support
        * [#865](https://github.com/dragoonDorise/EmuDeck/pull/865)
* RetroArch
    * Set RetroArch Input Driver to SDL by default
    * Replaced Yabause with Kronos as the default in Steam ROM Manager
        * [#792](https://github.com/dragoonDorise/EmuDeck/pull/792)
    * Added migration support for the new melonDSDS RetroArch core
        * Migration tool will automatically copy, **not delete**, saves and configurations from the old melonDS 
        core to the new new melonDSDS RetroArch core  
        * Use the "Nintendo DS - RetroArch melonDS DS" parser in Steam ROM Manager or select it in ES-DE's alternate emulators list to try it out! 
        * [#956](https://github.com/dragoonDorise/EmuDeck/pull/956)
    * Fixed Hardcore Mode for FBNeo RetroAchievements
    * Added buildbot downloader to automatically download shaders, PPSSPP files, assets, info, cheats, controller configuration, and overlay files
        * [#957](https://github.com/dragoonDorise/EmuDeck/commit/dc9803a729db0920fc06d5ef77e6097bee1a4f50)
    * Culled unused/outdated cores
        * [#597](https://github.com/dragoonDorise/EmuDeck/pull/597)
    * Added support for the RetroArch Citra core
* Rosalie's Mupen GUI
    * Added combo hotkeys, see [RMG Hotkeys](../../emulators/steamos/rmg.md#rmg-hotkeys) for a full list
    * Fixed save and save state folders not being created
        * [#1030](https://github.com/dragoonDorise/EmuDeck/commits/dev/)
* Ryujinx 
    * Pointed launcher to Ryujinx's `.sh` file instead
* RPCS3
    * Added support for migrating to the AppImage
* Supermodel (New emulator!)
    * Added Supermodel to EmuDeck
        * [#937](https://github.com/dragoonDorise/EmuDeck/pull/937)
* Vita3K
    * Set renderer to Vulkan by default
    * Removed default fields in config
        * [#880](https://github.com/dragoonDorise/EmuDeck/pull/895)
* Xenia
    * Added symlink to saves folder in `Emulation/saves`
    * Set renderer to D3D12 by default

## Tools

* EmulationStation-DE
    * Moved the AppImage to $HOME/Applications and renamed to ES-DE.AppImage
    * Set melonDS DS as the new default core for the Nintendo DS
* Pegasus (New frontend!)
    * Added Pegasus to EmuDeck  
* Steam ROM Manager
    * Added "Atomiswave (Flycast Standalone)" parser
    * Added "NAOMI (Flycast Standalone)" parser
    * Added "NAOMI 2 (Flycast Standalone)" parser
    * Added "Nintendo 3DS (RetroArch Citra)" parser
    * Added "Philips CD-i (MAME Standalone)" parser
    * Added "SNK Neo Geo CD - MAME (MAME Standalone)" parser
    * Added "SNK Neo Geo CD - MAME (RetroArch FBNeo)" parser
    * Added "Tiger Electronics Game.com - MAME (MAME Standalone)" parser
    * Added "VTech VSmile - MAME (MAME Standalone)" parser
    * Added "Mattel Electronics Intellivison (RA Core)" parser
    * Added "NEC PC-FX (RA Core)" parser
    * Added "Nintendo Virtual Boy (RA Core)" parser
    * Added "TIC 80" parser
        * [#791](https://github.com/dragoonDorise/EmuDeck/pull/791)
    * Added "Sameboy Game Boy Color (RA Core)" parser
        * [#794](https://github.com/dragoonDorise/EmuDeck/pull/794) 
    * Cleaned up parser category names
        * [#808](https://github.com/dragoonDorise/EmuDeck/pull/808)
    * Fixed Steam ROM Manager shortcut not launching on GNOME desktops

## EmuDeck Tools

* Uninstall Tool
    * Properly wipes your device of anything EmuDeck related
    * Included a prompt to uninstall Decky Loader
    * Included a prompt to back up BIOS and saves
* Compression Tool
    * Added CDI to whitelist
        * [#1021](https://github.com/dragoonDorise/EmuDeck/pull/1021)
    * Added CHD support for PPSSPP
        * Compression Tool will prompt users if they would like to compress their PPSSPP ROMs to CSO or CHD
    * Added XISO support for Xemu
    * Added 3DS Trimming support for Citra
        * [#530](https://github.com/dragoonDorise/EmuDeck/pull/530)
    * Added 7Zip support for a large amount of systems (primarily RetroArch)
    * Updated CHDMAN
    * Added support for compressing Dreamcast CUE/BIN ROMs to CHD
* Cloud Services   
    * Added Nebula
        * [#731](https://github.com/dragoonDorise/EmuDeck/pull/731)
    * Added Greenlight xCloud Client
        * [#702](https://github.com/dragoonDorise/EmuDeck/pull/702)
    * Added Steam Link and Spotify
        * [#707](https://github.com/dragoonDorise/EmuDeck/pull/707)
    * Added Shadow.Tech Cloud Streaming Client
        * [#739](https://github.com/dragoonDorise/EmuDeck/pull/739)
    * Added Pocket Casts
        * [#893](https://github.com/dragoonDorise/EmuDeck/pull/893)
    * Added Crave
        * [#891](https://github.com/dragoonDorise/EmuDeck/pull/891)
    * Removed Firefox as a default browser for Cloud Services
        * [#910](https://github.com/dragoonDorise/EmuDeck/pull/910)
    * Add Antstream Arcade Cloud
        * [#969](https://github.com/dragoonDorise/EmuDeck/pull/969)
    * Switched to a more universal browser command that is not reliant on flatpak only
        * [#941](https://github.com/dragoonDorise/EmuDeck/pull/941)
    * Switched to local running instance of Jellyfin for default URL. This allows instant access if Jellyfin server is installed and running on Steam Deck
        * [#909](https://github.com/dragoonDorise/EmuDeck/pull/909)
* Homebrew Games
    * Added Apotris
        * [#706](https://github.com/dragoonDorise/EmuDeck/pull/706)

## EmuDeck Configurations

* Added OOTB support for ChimeraOS
* Added OOTB support for a wide variety of Linux distributions
* Added preliminary support for setting emulator languages through the EmuDeck application
    * [#545](https://github.com/dragoonDorise/EmuDeck/pull/545)
* Removed 3DS and GameCube symlinks with proper logic to ensure ROMs are not lost
    * [#1005](https://github.com/dragoonDorise/EmuDeck/pull/1005)
* Steam Input
    * Added a `EmuDeck - Steam Deck Radial Menus XL` profile with all emulators mapped 
        * Pressure sensitivity dialed way down from the previous profile   
        * [#1018](https://github.com/dragoonDorise/EmuDeck/pull/1018)
    * Added `EmuDeck - Controller Hotkeys` and `EmuDeck - Frontend Controller Hotkeys` profiles for controllers. See the [Hotkeys](../../controls-and-hotkeys/steamos/hotkeys.md) page for a full list of the new hotkeys
    * Added a `EmuDeck - Steam Deck Light Gun Controls` profile
        * Intended to be used with Flycast (Standalone), MAME (Standalone), the Model 2 Emulator, and Supermodel
        * Right Trackpad set as mouse, sensitivity set to 200%. R2 set to "Left Click". L2 set to "Right Click". 
* Moved all `/bin/sh` and `/usr/bin/bash` to `/bin/bash` 
    * [#972](https://github.com/dragoonDorise/EmuDeck/pull/972)
* Updated emulatorInit/isLatestVersionGH
    * Allow user to skip update check for all or per emulator
    * [#942](https://github.com/dragoonDorise/EmuDeck/pull/942)
* Added support for launching Proton emulators with flags
    * Allows for lauching Xenia with custom flags (sort of like per game configs)
    * [#961](https://github.com/dragoonDorise/EmuDeck/pull/961)
* Allow user override Proton version for Proton launchers
    * [#870](https://github.com/dragoonDorise/EmuDeck/pull/870)
* Removed dependency on google in Yuzu launcher
    * [#774](https://github.com/dragoonDorise/EmuDeck/pull/774)
* Added preliminary support for ULWGL
* Added support for swapping between the Nintendo and the Xbox Layout