---
title: Half-life
permalink: /docs/guides/halflife/
---

#### Half Life supports keyboards, mice and controllers so you can use any combination.

## Universal Split Screen setup
1. Install and run Universal Split Screen: see the [quick start guide](https://universalsplitscreen.github.io/docs/quickstart/).
1. In options, load the GoldSrc Engine preset.
1. Go back to the Current window tab.

## Half Life setup
1. Open the Half Life directory by right-clicking Half Life in Steam -> Properties -> Local files -> Browse game files...

1. Launch the shortcut as many times as you need.
     * GoldSrc Engine games will usually not let you launch more than one instance. In Universal Split Screen, alt-tab into Half Life so the window is selected, then click 'Unlock Source engine for a new instance'

1. Go to Options -> Mouse. Set Raw mouse input to yes. Set Joystick to enabled if you are using a controller. (If you are using a controller, make sure to also enable `Hook XInput` in Universal Split Screen).

1. On the first instance, use the server browser to find a server (***Find a server without Valve Anti Cheat, just in case***). Right-click -> View server info. Copy the IP Address.

1. In all instances, at the main menu, use the ` (tilde) key to open the console. This key is usually above the tab key.

1. Type `connect IP` and click Submit, replacing IP with the IP you copied, e.g. `connect 123.456.789.123`

1. You should now be connected to the same game.

## Tips before you start
* If you have inconsistent mouse movement, especially when moving multiple mice, make sure the polling rates on your mice are set as low as possible. You can usually set this in your mouse configuration program (look on the manufacturer's website).

* Disable steam overlay by right-clicking Half Life in Steam -> Properties and un-check 'Enable the Steam Overlay while in-game'

* If you want to start and stop split screen, you should restart all instances of the game or it will start to slow down significantly.

## Split screen setup
1. Install and run Universal Split Screen: see the [quick start guide](https://universalsplitscreen.github.io/docs/quickstart/)

1. In options, load the GoldSrc Engine preset (if you have not already done so).

1. Go back to the Current window tab. Alt+tab into the first instance. Set the mouse and keyboard or controller. Repeat for the other instances.

1. Click Start split screen. You should now be able to play. Press End to stop.

## Default options
For reference, here are the default options.
![Goldsrc options](https://raw.githubusercontent.com/UniversalSplitScreen/UniversalSplitScreen.github.io/master/img/goldsrc_options.png)
