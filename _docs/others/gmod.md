---
title: Garry's Mod
permalink: /docs/guides/gmod/
---

## Video tutorial
<div class="embed-container">
  <iframe 
          width="560" 
          height="315" 
          src="https://www.youtube.com/embed/t3DZtNIdjDM" 
          frameborder="0" 
          allow="accelerometer; 
                 autoplay; 
                 encrypted-media; 
                 gyroscope; 
                 picture-in-picture" 
          allowfullscreen="allowfullscreen">
  </iframe>
</div>

## Universal Split Screen setup
1. Install and run Universal Split Screen: see the [quick start guide](https://universalsplitscreen.github.io/docs/quickstart/).
1. In options, load the Source Engine preset.
1. Go back to the Current window tab.

## Garry's Mod setup
1. Open the GarrysMod directory by right-clicking Garry's mod in Steam -> Properties -> Local files -> Browse game files...

1. Right-click hl2.exe and click Create shortcut. Rename the shortcut if you want.

1. Right-click the new shortcut and select properties.

1. At the end of Target, add `-windowed -w 1920 -h 500 -insecure +m_rawinput 1`
    * This is for a 1920x1080 monitor. You can adjust the width/height for your monitor.
    * The `-insecure` will prevent you from joining any Valve Anti Cheat (VAC) secured servers. You can remove it if you want, but it is risky.

1. Launch the shortcut as many times as you need.
     * Source Engine games will usually not let you launch more than one instance. In Universal Split Screen, alt-tab into Garry's Mod so the window is selected,  then click 'Unlock Source engine for a new instance'

1. Click Start new game. Change Single Player to however many players you need. Make sure Local Server is checked. You can set the map/gamemode as you like. Click Start Game.

1. On the other instances, go to Find Multiplayer Game -> Local Network and join the server.

## Tips before you start
* If you have inconsistent mouse movement, especially when moving multiple mice, make sure the polling rates on your mice are set as low as possible. You can usually set this in your mouse configuration program (look on the manufacturer's website).

* Disable steam overlay by right-clicking Garry's Mod in Steam -> Properties and un-check 'Enable the Steam Overlay while in-game'

* If you want to start and stop split screen, you should restart all instances of the game or it will start to slow down significantly.

## Split screen setup
1. Open Universal Split Screen

1. In options, load the Source Engine preset (if you have not already done so).

1. Go back to the Current window tab. Alt+tab into the first instance. Set the mouse and keyboard or controller. Repeat for the other instances.

1. Click Start split screen. You should now be able to play. Press End to stop.

## Default options
For reference, here are the default options.
![Source options](https://raw.githubusercontent.com/UniversalSplitScreen/UniversalSplitScreen.github.io/master/img/source_options.png)
