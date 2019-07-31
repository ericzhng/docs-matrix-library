---
title: Don't Starve Together
permalink: /docs/guides/dst/
---

## Video tutorial
<div class="embed-container">
  <iframe 
          width="560" 
          height="315" 
          src="https://www.youtube.com/embed/arGi0uOwh_M" 
          frameborder="0" 
          allow="accelerometer; 
                 autoplay; 
                 encrypted-media; 
                 gyroscope; 
                 picture-in-picture" 
          allowfullscreen="allowfullscreen">
  </iframe>
</div>

## Don't Starve Together (DST) setup
1. Open the DST directory by right-clicking DST in Steam -> Properties -> Local files -> Browse game files...
1. Open the `bin` directory.
1. Create a text file called `steam_appid.txt`. Inside it, write `322330`. Save and exit.
1. Rename `steam_api.dll` to `steam_api.dll.valve`.
1. Download the latest release of the Goldberg Emulator [here](https://gitlab.com/Mr_Goldberg/goldberg_emulator/releases). Goldberg emu is required to run two instances of the game and to connect them together.
1. Extract it anywhere by right-clicking -> Extract all...
1. Copy the steam_api.dll from the Goldberg directory to the bin directory.

## Launching the instances
1. Run `dontstarve_steam.exe` once. After clicking Play! you will need to quickly click Play Offline. If you miss, click Cancel and try again.
    * If you can't get it fast enough, try disconnecting from the internet. Alternatively, use the steam_api.dll from the `experimental` folder in Goldberg. This version will prevent the game from connecting to the internet.
1. Before you launch a second instance, you will need to change your (fake) username and steam id.
1. Press Windows+R to open a command window, type in `%appdata%` and click OK. Navigate to Goldberg SteamEmu Saves\settings
1. Open `account_name.txt` and set it to a unique name. Open `user_steam_id.txt` and change it *slightly*, e.g. by increasing by 1.
1. Now you can launch the game again from the executable. Repeat these steps as many times as you need.
1. If you are using a controller, go to Settings -> and make sure Input Device is set to a controller (you will probably want to use the first controller on all instances)

## Connecting the instances
1. On one instance, go to Host Game and Make sure it is on Local Only
1. On the other instances, go to Browse Games -> Select the world.

## Split screen setup
1. Install and run Universal Split Screen: see the [quick start guide](https://universalsplitscreen.github.io/docs/quickstart/).
1. In options, load the Dont Starve Together preset.
1. Go back to the Current window tab. Alt+tab into the first instance. Set the mouse and keyboard or controller. Repeat for the other instances.
1. Click Start split screen. You should now be able to play. Press End to stop.

## Default options
For reference, here are the default options.
![Don't Starve Together options](https://raw.githubusercontent.com/UniversalSplitScreen/UniversalSplitScreen.github.io/master/img/dst_options.png)

