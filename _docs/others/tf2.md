---
title: Team Fortress 2
permalink: /docs/guides/tf2/
---

#### TF2 supports keyboards, mice and controllers so you can use any combination.

## Universal Split Screen setup
1. Install and run Universal Split Screen: see the [quick start guide](https://universalsplitscreen.github.io/docs/quickstart/).
1. In options, load the Source Engine preset.
1. Go back to the Current window tab.

## TF2 setup
1. Open the TF2 directory by right-clicking TF2 in Steam -> Properties -> Local files -> Browse game files...

1. Right-click hl2.exe and click Create shortcut. Rename the shortcut if you want.

1. Right-click the new shortcut and select properties.

1. At the end of Target, add `-game tf -windowed -w 1920 -h 500 -insecure +m_rawinput 1 +sv_lan 1`
    * This is for a 1920x1080 monitor. You can adjust the width/height for your monitor.
    * The `-insecure` will prevent you from joining any Valve Anti Cheat (VAC) secured servers.

1. Launch the shortcut as many times as you need.
     * Source Engine games will usually not let you launch more than one instance. In Universal Split Screen, alt-tab into TF2 so the window is selected, then click 'Unlock Source engine for a new instance'

1. Go to Options (click the cog at the bottom of the screen) -> Keyboard -> Advanced. Check enable developer console. Set gamepad to enabled in Settings -> Mouse if you are using a controller.

1. At the main menu, use the ` (tilde) key to open the console. This key is usually above the tab key.

1. To start a game, click Find a Game -> Create Server -> Change settings and click Start.

1. Once the game has started, open the console again at the pause menu. Type `status` and click Submit. Find the IP address that starts with 192.168, e.g. `192.168.1.117`.

1. On another instance, open the console and run `connect 192.168.XXX.YYY`. Replace the IP address with the IP address from the last step.

1. You should now be connected to the same game.

## Tips before you start
* If you have inconsistent mouse movement, especially when moving multiple mice, make sure the polling rates on your mice are set as low as possible. You can usually set this in your mouse configuration program (look on the manufacturer's website).

* Disable steam overlay by right-clicking TF2 in Steam -> Properties and un-check 'Enable the Steam Overlay while in-game'

* If you want to start and stop split screen, you should restart all instances of the game or it will start to slow down significantly.

## Split screen setup
1. Open Universal Split Screen

1. In options, load the Source Engine preset (if you have not already done so).

1. Go back to the Current window tab. Alt+tab into the first instance. Set the mouse and keyboard or controller. Repeat for the other instances.

1. Click Start split screen. You should now be able to play. Press End to stop.

## Default options
For reference, here are the default options.
![Source options](https://raw.githubusercontent.com/UniversalSplitScreen/UniversalSplitScreen.github.io/master/img/source_options.png)
