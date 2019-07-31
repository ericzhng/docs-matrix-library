---
title: Important notes
permalink: /docs/importantnotes/
---

* Selecting any of the Hooks in the options page will mean Universal Split Screen will run code in the process of the game. This may be detected as cheating by a game's anti-cheat or malware by your antivirus. _**Be careful not to use hooks on any games with an anti-cheat system!**_

* After ending split screen with Hooks enabled, it is always best to restart all the game instances. Source games (most Valve games) will start to slow down significantly otherwise.

* You can click Enable window resizing on a window to allow it to be resized (hover your mouse over the window edges). This can cause stretching in some games, however.

* If you have inconsistent mouse movement, especially when moving multiple mice, make sure the polling rates on your mice are set as low as possible. You can usually set this in your mouse configuration program (look on the manufacturer's website). This is especially important if you have 'Send raw mouse input' selected.

* On Windows 10, you can set each game to output to a different sound device. Right click the audio icon in the taskbar -> Open Sound settings -> App volume device preferences. Set the Output device for each game.

* If a window somehow is focused during split screen, you can press Windows+B then to unfocus it. If this doesn't work, make sure you have at least one hook selected, e.g. `Hook GetForegroundWindow`. This will automatically unfocus the window.

* If the program somehow crashes and input is locked, unlock input by pressing `Ctrl+Alt+Delete`

* If you want to use a controller that doesn't work out of the box with a game, you will need to use [x360ce](https://universalsplitscreen.github.io/docs/x360ce/).

* You can use the same keyboard as the input device for multiple games. You will need to change the controls for each instance, e.g. one uses WASD and one uses the number pad.

* If you get a warning like 'xinput1_4.dll not found' on Windows 7, copy `C:\Windows\System32\xinput1_3.dll` to the game directory and rename it to `xinput1_4.dll`. This will be fixed in a future version.
