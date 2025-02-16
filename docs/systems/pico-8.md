# Pico-8

## Overview

| Path(s) | Supported Extensions |
| --- | --- |
| `storage/roms/pico-8` | ++".png"++ ++".p8"++ |

## Emulator(s)

| Name | Documentation |
| --- | --- |
| Pico-8 &nbsp; `default` | [https://www.lexaloffle.com/pico-8.php](https://www.lexaloffle.com/pico-8.php) |
| Fake-08 | [https://github.com/jtothebell/fake-08](https://github.com/jtothebell/fake-08) |

## Instructions

### Option 1: Running Pico-8 through the native engine

Pico-8 games are best played with the default emulator as it supports all native features without any limitations.  You need to purchase it from [Lexaloffle](https://www.lexaloffle.com/pico-8.php) and we do recommend that you buy a copy if you can. Its an awesome piece of software and it also comes with the tools to make your own games. Enabling SSH and SAMBA can be done from the settings menu.

#### Setup

Once you have purchased a license; the files you need will depend on the device you are using. These instructions will walk through how to set things up to work on all of our supported devices.

The creation of the directories and copy of the files must be done as the root user. Creating the directories and copying the files directly to the microSD card **will not work** as the folder and files will not have the correct permissions.

- Go to [Lexaloffle's download page](https://www.lexaloffle.com/games.php?page=updates)
- From that page download the `Linux 64-bit` zip file and the `Raspberry Pi` zip file
- From the Linux 64-bit zip file...
    - Create a directory in `roms/pico-8` called `x86_64`
    - Upload the `pico8_dyn` and `pico8.dat` from the Linux 64-bit zip to this directory (you do not need any other files)
- From the Raspberry Pi zip file...
    - Create a directory in `roms/pico-8` called `aarch64`
    - Upload the `pico8_64` and `pico8.dat` from the Raspberry Pi zip to this directory (you do not need any other files)

``` bash title="Folder Structure"
/storage/roms/pico-8/
    ├─ x86_64/
    │   ├─ pico8_dyn
    │   ├─ pico8.dat
    ├─ aarch64/
    │   ├─ pico8_64
    │   ├─ pico8.dat
    └─ Splore.png
```

Launch Pico-8 from the device. This will ensure you have successfully loaded the files and the permissions are set. On launch Pico-8 will create the carts directory. You can then copy .png or .p8 files into this directory.

#### Playing a game

Once the above is set up is you have 2 options for playing games through Pico-8's native engine:

1. Using Splore
    - Splore is awesome as it allows you to browse and play the entire library of user created games with an internet connection.  
    - To use this method simply launch Splore.png from the gamelist.
    - Note that you will need an internet connection to browse the pico-8 BBS (If you don't have an internet connection you can still use it to launch games you have downloaded previously)
2. Through .png or .p8 files added directly `roms/pico-8`
    - Browse the list of games (aka. "Carts") on [Lexaloffle's website](https://www.lexaloffle.com/bbs/?cat=7&carts_tab=1#mode=carts&sub=2)
    - Download the .png file for any game you are interested in playing and upload it to `roms/pico-8`
    - Refresh EmulationStation by pressing ++"START"++ to open the Main Menu then select `Game Settings > Update Gamelists`.
    - You should now be able to launch the game by selecting it from the gamelist.

### Option 2: Running through RetroArch Fake-08

!!! warning "Fake-08 does not support all the native features of Pico-8 so its not guaranteed that every game will work with it."

- Set the default emulator for Pico-8 to Fake-08
- Browse the list of games (aka. "Carts") on [Lexaloffle's website](https://www.lexaloffle.com/bbs/?cat=7&carts_tab=1#mode=carts&sub=2)
- Download the .png file for any game you are interested in playing and upload it to `roms/pico-8`
- Refresh EmulationStation by pressing ++"START"++ to open the Main Menu then select `Game Settings > Update Gamelists`.
- You should now be able to launch the game by selecting it from the gamelist.