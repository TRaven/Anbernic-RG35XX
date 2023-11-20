---
title: TRaven's RG35XX Setup
---
## Firmware
My preferred firmware (for now) is <a href="https://www.patreon.com/posts/garlicos-for-76561333" target="_blank">GarlicOS</a>.
You can flash your SD card with the firmware with a tool such as [Balena Etcher](https://etcher.balena.io/)

## Accessing the files via USB on GarlicOS
We will use ADB to access the files on our RG35XX without having to remove the SD cards after it's set up. This guide will focus on accessing the files via Windows.

### Prepping the SD card.
1. Download the latest <a href="https://www.rg35xx.com/en/apps/mods-for-garlicos/" target="_blank">Toggle ADB mod</a>.
1. Pull the SD card where you store your ROMs (i.e. in a 2-card setup, use the 2nd SD card) and plug it into your computer.
1. On the SD card, navigate to Roms/APPS
1. Paste the contents of the Toggle ADB archive into this directory (i.e. Roms/APPS/Toggle ADB.sh and Roms/APPS/bin/printstr).
1. Eject the SD card and re-instert it into the RG35XX.

### Prepping Windows
To access our library and mess with the game artwork, we'll download and extract [GarlicPress](https://github.com/prosthetichead/GarlicPress). 

Accessing other files to upload roms, update themes, buttons, etc. for example will require a little extra work:
1. In Windows, install [ADB Explorer](https://apps.microsoft.com/store/detail/adb-explorer/9PPGN2WM50QB)
1. In *ADB Explorer* settings, search for *Override ADB Path* and point to the *ADB.exe* in the directory where you extracted the *GarlicPress*
   * Alternatively, if you're NOT going to download GarlicPress, you can: 
      1. Download the [ADB Platform Tools](https://developer.android.com/tools/releases/platform-tools)
      1. Extract the *ADB Platform Tools* to a known location like your User directory.
	  1. use the adb.exe in here in the *Override ADB Path* setting in *ADB Explorer*
### Access
1. Turn on GarlicOS and navitgate to Consoles > APPS
1. Run *Toggle ADB*.
1. Restart the RG35XX (Turn it off and on again)
1. Plug the USB cord into the RG35XX and the Computer.
1. To work with Roms and artwork, open *GarlicPress*
   * If GarlicPress sees your console, the logo on the top left of the app will turn green.
1. To work with other files:
   1. Open *ADB Explorer*
   1. Click on the detected device and click *Browse*
   1. Click on *Root*
   1. Find the files you want! For example, in a single card setup, your Roms will be in mnt/mmc/Roms. In a two card setup, you'll find your roms in mnt/SDCARD/Roms.
Don't Forget to Run *Toggle ADB* again to turn it off if you want to use wired controllers or you may have problems.

## Enhanced Features
### ROM Search
GarlicOS doesn't have a ROM search by default. You can enable this functionality by uploading the [romSearch app](https://www.rg35xx.com/en/apps/apps-for-garlicos/).

### ROM Collections
If you want to enable some rom categorization functionality (i.e. putting your ROMs in a "Beaten" category or separate them out by genres) then use the [Collections mod](https://www.rg35xx.com/en/apps/mods-for-garlicos/).

## External Controller Support
I have had luck with the "Microsoft Xbox 360 Wireless Controller for Windows" which come with a USB wireless adaptor. This adaptor will plug into a USB-C to USB-A adaptor which will plug into the USB-C port on the bottom of the RG35XX. Right now I don't have it working with the Garlic main menu, but the games work.

1. On the RG35XX, on the first SD card in the /misc directory (or partition if you're plugging the SD card directly to your computer) create a file named waitForUSB (no extension).
1. While you're in there, back up /mnt/mmc/CFW/retroarch/.retroarch/retroarch.cfg (don't be like me and destroy your config and have to reflash).
1. *IMPORTANT*: If you're using it, make sure ADB is disabled before trying to plug in your controller or it won't be detected.
1. You may need to reconfigure the controls in retroarch.
   1. Settings -> Input -> Maximum Users = 2 (number of controllers + 1)
   2. Do not touch Port 1 Controls in global settings, they are mapped to rg35xx buttons.
   3. Settings -> Input -> Port 2 Controls
      1. Device Index = [Whatever controller is detected]
      2. Configure the keys
      3. Save Controller Profile
      4. Back out to the main retroarch menu and go to Configuration File -> Save Current Configuration
1. If you want to use one of the controllers as Player 1, launch the game, change the control mappings of the last controller (2nd in this example) in Quick Menu, and save them for game/directory/core (hold Menu for at least 1 second, then press X to open Quick Menu):
   1.   Quick Menu -> Controls -> Port 2 Controls -> Mapped Port = 1
   1.   Quick Menu -> Controls -> Manage Remap Files -> Update/Save Remap File for Game/Core

## Customizing the UI
You can play around with some [Skins](https://www.rg35xx.com/en/customization/garlicos-themes/), [boot logos](https://www.rg35xx.com/en/customization/boot-logos/), [System Icons](https://www.rg35xx.com/en/customization/system-icons/), and [battery charging themes]([https://www.rg35xx.com/en/customization/share-your-battery-charging-theme/) to customize your look.

## What Games Should I Play?
A good reference for what games will work on the RG35XX is the <a href="https://archive.org/details/tiny-best-set-go" target="_blank">Tiny Best Set: GO!</a>. Use this as a reference for what to load up from your collection.
