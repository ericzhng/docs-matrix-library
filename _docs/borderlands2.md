---
title: Borderlands 2
permalink: /docs/borderlands2/
---

Borderlands 2 (BL2) supports keyboards, mice and controllers, so you can use any combination you like.

Borderlands: The Pre-Sequel will also work exactly the same with this guide.

Please note that the mouse cursor will be invisible when you open your inventory until you left click or right click.

## Video tutorial
<div class="embed-container">
  <iframe 
          width="560" 
          height="315" 
          src="https://www.youtube.com/embed/XSUR1NCQows" 
          frameborder="0" 
          allow="accelerometer; 
                 autoplay; 
                 encrypted-media; 
                 gyroscope; 
                 picture-in-picture" 
          allowfullscreen="allowfullscreen">
  </iframe>
</div>

## Tips before you start
* If you have inconsistent mouse movement, especially when moving multiple mice, make sure the polling rates on your mice are set as low as possible. You can usually set this in your mouse configuration program (look on the manufacturer's website).
* If the mouse cursor is flickering, set VSync on in the Video options.
* Disable Steam overlay by right-clicking Borderlands 2 in Steam -> Properties and un-check 'Enable the Steam Overlay while in-game'. Steam overlay can cause some issues with split screen.
* If you want to copy or move characters between save folders, go to `Documents\My games\Borderlands 2\WillowGame\SaveData\`
* If you are using an off-brand controller that doesn't work with BL2 normally, see the guide on x360ce. x360ce will need to be placed in the `Binaries\Win32` directory.

## Borderlands 2 setup
1. Open the Borderlands2 directory by right-clicking Borderlands 2 in Steam, -> Properties -> Local files -> Browse game files...

1. Open Binaries/Win32

1. Right-click Borderlands2.exe and click Create shortcut. Rename the shortcut if you want.

1. Right-click the new shortcut and select properties.

1. At the end of Target, add `-NoLauncher -AlwaysFocus -WindowPosX=0 -WindowPosY=0 -ResX=1920 -ResY=500`
    * This is for a 1920x1080 monitor. You can adjust the X/Y for your monitor.
    
1. Create another shortcut. This time add `-NoLauncher -AlwaysFocus -SaveDataId=2 -WindowPosX=0 -WindowPosY=0 -ResX=1920 -ResY=500` instead. Note that SaveDataId has changed.

1. Repeat for as many players as you need. Make sure to change SaveDataId. Now launch all the shortcuts.

1. Set LAN in Network Options for each game. Click Find Games to connect to one player.

## Split screen setup
1. Install and run Universal Split Screen: see the [quick start guide](https://universalsplitscreen.github.io/docs/quickstart/).
1. In options, load the Borderlands 2 preset.
1. Go back to the Current window tab. Alt+tab into the first instance. Set the mouse and keyboard or controller. Repeat for the other instances.
1. Click Start split screen. You should now be able to play. Press End to stop.

## Default options
For reference, here are the default options.
![Borderlands 2 options](https://raw.githubusercontent.com/UniversalSplitScreen/UniversalSplitScreen.github.io/master/img/bl2_options.png)
