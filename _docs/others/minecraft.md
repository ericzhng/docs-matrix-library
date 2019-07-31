---
title: Minecraft
permalink: /docs/guides/minecraft/
---

Minecraft does not support controllers, so you will need multiple keyboards and mice.

Please note that if you are using a high polling rate mouse, input will be very stuttery for about a minute after split screen starts. 

If you are using Minecraft 1.12 or earlier, use the Minecraft 1.14.3 preset and enable "Send fake window focus messages"

## Video tutorial
(If you are following the video, make sure to disable Raw input in Options -> Controls -> Mouse settings in Minecraft 1.14.4 or higher)
<div class="embed-container">
  <iframe 
          width="560" 
          height="315" 
          src="https://www.youtube.com/embed/nOvlsMehzjk" 
          frameborder="0" 
          allow="accelerometer; 
                 autoplay; 
                 encrypted-media; 
                 gyroscope; 
                 picture-in-picture" 
          allowfullscreen="allowfullscreen">
  </iframe>
</div>

## Minecraft setup
To launch two separate Minecraft instances, we will need a launcher called MultiMC
1. Download and extract [MultiMC](https://multimc.org/#Download)

1. Run MultiMC and log in with your Mojang account.

1. Create two(or more) instances by clicking Add Instance. Make sure they have a different names.

1. (Optional) [Install OptiFine with MultiMC](https://github.com/MultiMC/MultiMC5/wiki/MultiMC-and-OptiFine) for better performance.

1. * (If you have multiple Minecraft accounts) Select the first instance and click Launch. Change account in the top-right corner, then repeat for the second instance.
   * (If you have one Minecraft account) Select the first instance and click Launch Offline. Set your username to anything. Repeat for the second instance

1. Make sure the games are running in windowed mode. Resize them however you like.

1. Start a singleplayer world and open to LAN in the pause menu. The other player can join from the multiplayer menu. Alternatively, you can connect to any server (with multiple Minecraft accounts) or an 'Offline' server (if you have one Minecraft account).

1. (Minecraft 1.14.4 or higher) Make sure to disable Raw input in Options -> Controls -> Mouse settings.


## Split screen setup
1. See how to install Universal Split Screen in the [Quick Start guide](https://universalsplitscreen.github.io/docs/quickstart/).

1. In options, select the preset and click Load.
    * For Minecraft 1.14.3 and higher, you should use the `Minecraft 1.14.3` preset. For versions 1.13 to 1.14.2, use `Minecraft Alternative`. If split screen doesn't work, try the other preset (after restarting the instances).

1. Go back to the Current window tab.

1. Alt+tab into the first game. Set the mouse and keyboard. Repeat for the second game.

1. Click Start split screen. You should now be able to play. Press End to stop.


## Tips
 * If you have inconsistent mouse movement, especially when moving multiple mice, make sure the polling rates on your mice are set as low as possible. You can usually set this in your mouse configuration program (look on the manufacturer's website).
 
 * If the mouse cursor is flickering, try setting VSync on by dragging the FPS limit slider to the left.
 
 * Joining a Minecraft server with 'anti-cheat' will not get you banned if you use Hooks(in the options), since servers cannot run code on your machine.
 
 * You can click Toggle window borders to remove the window title, giving you more space.
 
 * If you want to use an existing save, copy it from `C:\Users\YOUR_WINDOWS_USERNAME\AppData\Roaming\.minecraft\saves` to `MultiMC\instances\INSTANCE_NAME\.minecraft\saves`, replacing YOUR_WINDOWS_USERNAME and INSTANCE_NAME as necessary.


## Default options
For reference, here are the default options.
![Minecraft Options](https://raw.githubusercontent.com/UniversalSplitScreen/UniversalSplitScreen.github.io/master/img/minecraft_options.png)
