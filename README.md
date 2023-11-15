---
title: TRaven's RG35XX Setup
---
## Firmware
My preferred firmware (for now) is <a href="https://www.patreon.com/posts/garlicos-for-76561333" target="_blank">GarlicOS</a>.

## Accessing the files via USB on GarlicOS
We will use ADB to access the files on our RG35XX without having to remove the SD cards after it's set up. This guide will focus on accessing the files via Windows.
### Prepping the SD card.
1. Download the latest <a href="https://www.rg35xx.com/en/apps/mods-for-garlicos/" target="_blank">Toggle ADB mod</a>.
1. Pull the SD card where you store your ROMs (i.e. in a 2-card setup, use the 2nd SD card) and plug it into your computer.
1. On the SD card, navigate to Roms/APPS
1. Paste the contents of the Toggle ADB archive into this directory (i.e. Roms/APPS/Toggle ADB.sh and Roms/APPS/bin/printstr).
1. Eject the SD card and re-instert it into the RG35XX.
### Prepping Windows
Now we'll need a way to access these files once we plug the RG35XX to the USB port on our computer. 
1. In Windows, install <a href="https://apps.microsoft.com/store/detail/adb-explorer/9PPGN2WM50QB" target="_blank">ADB Explorer</a>
1. Download the <a href="https://developer.android.com/tools/releases/platform-tools" target="_blank">ADB Platform Tools</a>.
1. Extract the *ADB Platform Tools* to a known location like your User directory.
1. In *ADB Explorer* settings, search for *Override ADB Path* and point to the *ADB.exe* in the directory where you extracted the *ADB Platform Tools*
### Access
1. Turn on GarlicOS and navitgate to Consoles > APPS
1. Run *Toggle ADB*.
1. Restart the RG35XX (Turn it off and on again)
1. Plug the USB cord into the RG35XX and the Computer.
1. Open *ADB Explorer*
1. Click on the detected device and click *Browse*
1. Click on *Root*
1. Find the files you want! For example, in a single card setup, your Roms will be in mnt/mmc/Roms. In a two card setup, you'll find your roms in mnt/SDCARD/Roms.

Don't Forget to Run *Toggle ADB* again to turn it off if you want to use wired controllers or you may have problems.

## What Games Should I Play?
A good reference for what games will work on the RG35XX is the <a href="https://archive.org/details/tiny-best-set-go" target="_blank">Tiny Best Set: GO!</a>. Use this as a reference for what to load up from your collection.
