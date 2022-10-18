---
title: "Useful AutoHotKey Scripts for Destiny 2"
description: "A list of scripts I use frequently for Destiny 2 PVE"
date: 2022-10-18T07:00:00-06:00
tags: ["destiny"]
draft: false
---

## Divinity Spam

**Explanation:** spams left click on a 80ms delay for group DPS scenarios. Helps the Divinity user conserve ammo while still providing the constant crit bubble & weaken

**Instructions**:

1. Launch the script
2. Press **6** to start
3. Press **7** to reset
4. Press **8** to terminate script

**Script:**

```
#SingleInstance, Force

6::
loop,
{
    Click,
    Sleep, 80
}
Return

7::Reload

8::
ExitApp
```

## Hiveway Titan AFK

**Explanation:** spams grenade and class ability to kill a group of enemies to give you passive XP while AFK

**Instructions**:

1. Launch the script
2. Press **6** to start
3. Press **7** to reset
4. Press **8** to terminate script

**Script:**

```
#SingleInstance, Force

6::
loop,
{
    Send, k
    Sleep, 100
    Send, {s Down}
    Sleep, 100
    Send, {s Up}
    Sleep, 100
    Send, v
    Sleep, 100
    Continue
}
Return

7::Reload

8::
ExitApp
```

## Last Wish Raid Wish Wall Menu

**Explanation:** [shurochi.com](https://shurochi.com/)

**Instructions:**

1. Make sure your in-game sens is 8, Screen Bounds max, FOV max, Aim Smoothing turned off, and Windowed Fullscreen
2. Stand on the middle of the plate
3. Aim at the very middle of the wall grid
4. Press **F3** and type a number corresponding to whatever wish you want to input
5. Press **F4** to close macro at any time (or at the end if you don’t want to input it again)

**Script:**
[wish_wall_menu.ahk](https://gist.githubusercontent.com/mackiser/eef24400c71152dacce1633f19f1ee54/raw/04d07982b5e29630f703445364d67f37fdc4f3e2/wish_wall_menu.ahk)
