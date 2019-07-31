---
title: Prison Architect
permalink: /docs/guides/prisonarchitect/
---

## Prison Architect setup
1. Press Window+R. Paste in `C:\Users\USERNAME\AppData\Local\Introversion\Prison Architect`, replacing USERNAME with your Windows username. Open preferences.txt
    * Alternatively, Paste `%appdata%` in Windows+R, go up a directory, then into `Local\Introversion\Prison Architect`
1. Set ScreenWindowed to `true`
1. Set ScreenW and ScreenH to the width/height you want. e.g. for a 1920x1080 monitor, use ScreenW 960 and ScreenH 1020 for vertical split screen or ScreenW 1920 and ScreenH 500 for horizontal split screen. Adapt this for your monitor size.
1. Open the game's directory by right-clicking Prison Architect in Steam -> Properties -> Local files -> Browse game files...
1. Rename `steam_api.dll` to `steam_api.dll.valve` and `steam_api64.dll` to `steam_api64.dll.valve`
1. Download the latest release of the Goldberg Emulator [here](https://gitlab.com/Mr_Goldberg/goldberg_emulator/releases), The Goldberg Emulator is required to run two instances of the game.
1. Extract it anywhere by right-clicking -> Extract all...
1. Copy steam_api.dll and steam_api64.dll from the Goldberg directory into the game directory.
1. Launch Prison Architect64.exe (or Prison Architect.exe if you are on 32-bit) as many times as you need.
1. On one instance, load or create a prison. Open the pause menu and click Go Online. Make sure the server is Publicly listed. You will probably want to set a password. The Username can be whatever you want.
1. On the other instance(s), go to Join Online Game -> Find the game in the list -> Enter the password and another username.

## Split screen setup
1. Install and run Universal Split Screen: see the [Quick Start guide](https://universalsplitscreen.github.io/docs/quickstart/).
1. In options, load the Prison Architect preset.
1. Go back to the Current window tab. Alt+tab into the first instance. Set the mouse and keyboard. Repeat for the other instances.
1. Click Start split screen. You should now be able to play. Press End to stop.

## Default options
For reference, here are the default options.
![Prison Architect Options](https://raw.githubusercontent.com/UniversalSplitScreen/UniversalSplitScreen.github.io/master/img/prisonarchitect_options.png)
