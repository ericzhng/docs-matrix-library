---
title: Virtual super resolution
permalink: /docs/guides/borderlands2/
---

You may find that some games will not let you resize them smaller than some size, or that UI elements break.
You can solve this by setting up a virtual super resolution.

## On AMD GPUs
1. Right-click the AMD icon in the taskbar -> Open Radeon Settings -> Display -> check Virtual Super Resolution and GPU scaling. Then set the resolution to something like 2560x1440 or 3840x2160 in Windows display settings.

## On NVIDIA GPUs
1. Right click desktop -> NVIDIA Control Panel
1. Open Display -> Change Resolution -> click Customize -> click Create custom resolution.
1. To set resolution to X by Y, set Horizontal Pixels to X and Vertical lines to Y (I would recommend either 2560 by 1440 or 3840 by 2160)
1. Click Test -> Yes to changes -> Ok
1. In the list of resolutions, select your new custom resolution, click Apply -> Yes to changes
1. Done. If you want to quickly switch between resolutions now, you can go to Windows settings -> Display -> Resolution

## On Intel GPUs
1. Right-click desktop -> Graphics Properties -> Display
2. Open Custom Resolutions -> Add
3. Set Width to new width in pixels and Height to new height in pixels. (I would recommend either 2560 by 1440 or 3840 by 2160). Set Refresh Rate to 60
4. Open General Settings and select your new custom resolution in the Resolution menu
5. If you get an error 'This resolution exceeds the maximum bandwidth capacity', try updating your display drivers. If this does not fix it, try plugging in your laptop/computer into a secondary monitor, then use the AMD/NVIDIA instructions depending on which discrete GPU you have.
