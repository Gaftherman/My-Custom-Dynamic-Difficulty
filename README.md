# My-Custom-Dynamic-Difficulty
> Based on Cubemath's Dynamic Difficulty X.
---
## Installation Guide

Download this repository and extract it's contents inside ``Steam\steamapps\common\Sven Co-op\svencoop\``

That should look like this:

```
└── 📁svencoop
    └── 📁scripts
        └── 📁plugins
            ├── 📁Gaftherman
            │   └── 📄DynamicDifficulty.as
            └── 📁store
                ├── 📄DDX-Banned.txt
                ├── 📄DDX-Maplist.txt
                └── 📄DDX-Matrix.txt        
```
## What is new/changed in this script?

- 🛠The skills now are reading from store/DDX-Matrix.txt
    > Reason: An easier way to edit enemy skills.

- 🛠The DDX-Maplist.txt now works in reverse. With this I mean that the maps that you put here will be where the DD doesn't work (it will take the default skill of SC)
    > Reason: It's preferable to make a BlackList instead of a WhiteList in my opinion.

- 💡I added a timer to see how much time has passed on the map.
    - To modificate this, put in the console ".admin_timer_mode 0-2"
    - ⚠️ Just admins can modificate this.

    Mode 0: Deactivate the timer.
    
     ![](https://i.imgur.com/A5BBHcc.png)
        
    Mode 1: In this mode the time is going to show like ( Timer: Hours : Minutes : Seconds )
    
     ![](https://i.imgur.com/brOfebH.png)
     
    Mode 2: In this mode the timer will be progressive.
    
     ![](https://i.imgur.com/8V9uPRc.png)
     ![](https://i.imgur.com/QetOUFh.png)
