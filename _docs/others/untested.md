---
title: Untested Games Setup
permalink: /docs/untested/
---

#### Use this guide if there isn't a guide on your game. It covers how to setup the game and how to setup the options.

## Launching multiple instances
### For most Steam games
Right-click it on Steam -> Properties -> Local files -> Browse game files... to open the game directory. 

You will need to find an executable(exe) file for the game. 
If this isn't in the immediate directory, try looking in folders named `bin`/`win32`/`win64` or similar.

Try launching the exe multiple times. 
If it doesn't let you open multiple instances, you will probably need to manipulate steam_api.dll

### Manipulating steam_api.dll
Search for steam_api.dll and/or steam_api64.dll in the game directory. 

When you find it, try renaming it to steam_api.dll.disabled (or anything) and launch the executables again. 

If this doesn't work, e.g. it gives a "Couldn't load steam_api.dll" error, you will need a replacement for steam_api.dll. 
See the guide on the [Goldberg Emulator](https://universalsplitscreen.github.io/docs/goldberg/).

### Closing a Mutex
Some games will open a mutex that indicates to any other process that the game is already running, to prevent multiple instances.
You can close these mutexes with Process Explorer. Download it [here](https://docs.microsoft.com/en-us/sysinternals/downloads/process-explorer).
1. Run Process Explorer as administrator by right-clicking -> Run as administrator.
1. Scroll down to the game process in the list. Press Ctrl+H to open the list of handles. 
1. Scroll down to the Mutex types.
1. Try and find a mutex with a name related to the game, e.g. hl2_singleton_mutex. Right-click -> Close Handle. 
    * It may sometimes not by a Mutex type, e.g. it could be an Event type.
1. Try launching the game again from the executable. 
1. Repeat until you are able to launch a second instance.

Once you have identified the handle name, you can use the `Handle unlocker` button in Universal Split Screen. Enter the handle name in the text box and click the button to close it for the targeted game.
      
## Connecting the instances.
Most games will have a LAN (Local Area Network) option that will allow you to connect to a server running on the same machine. 
Start a server as you normally would, then search for servers on LAN.

If the game has a direct connect option, enter `127.0.0.1` or `localhost` as the server IP address. For the port, leave it as default or use whatever the server is hosting on.

If the game only accepts connections via Steam invites, see the guide on the [Goldberg Emulator](https://universalsplitscreen.github.io/docs/goldberg/). It will allow you to trick the invite system.
  
## Setting up Universal Split Screen
Before starting, see the [Important Notes](https://universalsplitscreen.github.io/docs/importantnotes/) section.

See the [Quick Start guide](https://universalsplitscreen.github.io/docs/quickstart/) for installation instructions and how to configure input devices.

You will need to work out which options are required by the game. All the options are labelled if you hover over them.

The first thing you should try to get working is keyboard input. 
It will work for most games if the game is tricked into thinking it is the foreground window, which is the first step.

The options you should all enable at first are `Send normal mouse`, `Send normal keyboard`, `Send fake window activate`, `Send fake window focus`, `Hook GetForegroundWindow`, `Hook GetCursorPos`, `Hook SetCursorPos` and `Hook GetAsyncKeyState`

Start split screen and see what results you get. If the game responds to any input, you have tricked it into thinking it's in the foreground.

If keyboard input isn't working at this point, try enabling `Send raw keyboard`, `Hook GetKeyState for WASD keys` and `Hook GetAsyncKeyState`.

When testing mouse input, there are a few components that need to work: Camera in first person games, clicking in first person, moving the mouse in menus, clicking in menus and whether the game distinguishes mouse devices. Make sure to test each one after changing options.

If you find that the game is confused where the mouse pointer is (ie it keeps moving towards the real Windows mouse cursor), try enabling `Filter mouse input messages from Windows`. Disable this if it doesn't work, as it can cause issues.

If you want to use controllers, make sure to enable `Hook XInput for gamepads`

If the game uses raw input and isn't responding to any mouse input, try enabling `Send raw mouse input`. 
Make sure anything related to raw input is turned on in the game's options.
This isn't recommended unless necessary, since it has the worst performance. 

If the game is responding to multiple mice, try enabling `Filter raw input messages from Windows`.

If mouse input isn't working at this stage, it's likely that the game uses a legacy mouse input method. 
Make sure to ***disable*** anything to do with raw input, in the options and the game itself, and enable `Send normal mouse input`, `Hook GetCursorPos`, `Hook SetCursorPos` and `Use legacy input`. `Update absolute position flag in mouse move messages` is also highly recommended for legacy input, especially if you notice sudden jerks in movement.

To make sure the fake mouse cursor is hidden/shown when needed, check `Hook mouse visibility`. This is useful in a first person game where the cursor should stay hidden unless in a UI menu.

Once you have input working correctly, try disabling the options one by one until you have the minimal setup.

Save your options as a preset by clicking New, typing a name **and clicking Save**.

Please report your results (positive or negative) in the [GitHub issue tracker](https://github.com/UniversalSplitScreen/UniversalSplitScreen/issues) or e-mail me (ilyaki@pm.me). Please send the options you used and the steps you followed.
