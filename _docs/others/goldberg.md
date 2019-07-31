---
title: Goldberg Emulator
permalink: /docs/goldberg/
---

(This guide is based on Goldberg Emulator v0.2.4)

The original Readme for the Goldberg emulator can be found [here](https://gitlab.com/Mr_Goldberg/goldberg_emulator/blob/master/Readme_release.txt)

You can find a list of games compatible with the Goldberg Emulator [here](https://www.reddit.com/r/GoldbergEmu/comments/bg7f3e/please_sticky_list_of_confirmed_workingnonworking/)

Some games use Steam to prevent you from launching multiple instances, and some games use Steam for matchmaking, preventing you playing with one copy. 

The Goldberg emulator replaces the Steam API dll, tricking games into letting you launch multiple instances and join the same server.
 
## Installation
1. Download the latest release of Goldberg [here](https://gitlab.com/Mr_Goldberg/goldberg_emulator/releases)
1. Extract it anywhere by right-clicking -> Extract all...
1. Open the game's directory by right-clicking it in Steam -> Properties -> Local files -> Browse game files...
1. Find where `steam_api.dll` and/or `steam_api64.dll` is located. It will usually be in a folder called `bin` or something similar.
1. Rename the dlls to something different, e.g. `steam_api.dll.valve`
1. Copy the dlls corredponding steam_api.dll and/or steam_api64.dll from the Goldberg directory to the game's directory.
1. In the same folder, if `steam_appid.txt` doesn't already exist, create it and fill it with the app id of the game. You can find the app id of any steam game with [SteamDB](https://steamdb.info/apps/)
1. Drag the original steam_api.dll (steam_api.dll.valve) onto generate_interfaces_file.exe in the tools folder (inside the Golberg folder). This will generate a steam_interfaces.txt file next to the steam_api.dll files.

## Setup
1. Launch the game from its executable (exe).
1. Before you launch a second instance, you will need to change your (fake) username and steam id.
1. Press Windows+R to open a command window, type in `%appdata%` and click OK. Navigate to Goldberg SteamEmu Saves\settings
1. Open `account_name.txt` and set it to a unique name. Open `user_steam_id.txt` and change it *slightly*, e.g. by increasing by 1.
1. Now you can launch the game again from the executable. Repeat these steps as many times as you need
    * Alternatively, you might be have to use lobby_connect. See the Lobby Connect section.
  
## Connecting the instances together
* If the game has a LAN option, try using it. If the game only has steam multiplayer invites for connecting, you will need to use the Lobby Connect method.

### Lobby Connect
1. On your first instance, start hosting a game. Make sure it is *not* invite-only (so friends can join without an invite).
1. (After changing account_name.txt and user_steam_id.txt) Run `lobby_connect\lobby_connect.exe` in the Goldberg directory.
1. The program will search for available games. When it has found one, enter the corresponding number and press Enter. You will have to point to the game's executable file. The game should launch and automatically connect to the server.
1. If you need any more instances, change the account name and user id, then repeat the Lobby Connect instructions.

## Uninstallation
1. Delete the steam_api.dll and/or steam_api64.dll in the game's directory. Rename the original (e.g. steam_api.dll.valve) back to the original name (ie steam_api.dll)
