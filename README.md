# My-Custom-Dynamic-Difficulty
> Based on Cubemath's Dynamic Difficulty0~10.
---
## Installation Guide

Download this repository and extract it's contents inside `Steam\steamapps\common\Sven Co-op\svencoop\`

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
    - ⚠️Just admins can modificate this. 
    - To modificate this, put in the console `.admin_timer_mode 0-2`.
    ```
    Mode 0: Deactivate the timer.
    ```
    ![](https://i.imgur.com/A5BBHcc.png)
    ```
    Mode 1: In this mode the time is going to show like ( Timer: Hours : Minutes : Seconds )
    ```
    ![](https://i.imgur.com/brOfebH.png)
    ```
    Mode 2: In this mode the timer will be progressive.
    ```
    ![](https://i.imgur.com/8V9uPRc.png)
    ![](https://i.imgur.com/QetOUFh.png)
    
 - 💡I added a way to change the velocity of the enemies depending of the difficult. It's like a multiplier. 
    - ⚠️Putting a multiplier too high may not work.
 
    ```angelscript
    /***********************/
    /* Monster speed array */
    /***********************/
    private array<double> MonsterSpeedMultiplier =
    {
        1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.3, 1.6
    };
    ```
  - 💡I added a way to barnacle eat more fast depending of the difficult. 
     - ⚠️Putting a value too high may not work.
     ```angelscript
     /****************************/
     /* Barnacle speed eat array */
     /****************************/
     private array<double> BarnacleEatSpeed =
     {
        8.0, 8.0, 8.0, 8.0, 8.0, 12.0, 16.0, 24.0
     };
     ```
    
  - 💡I added a way to vote for the player to change the difficulty on-the-fly.
    - ⚠️There is a delay of 15 seconds between vote. To avoid spam.
    - ⚠️If the player vote more than 8 times, He will not be able to vote for 80 seconds.
    - ⚠️You can add the SteamID of the people that you don't want to vote in the DDX-Banned.txt.
    
    `In the console:`
    ```
    .diff [number] - All players
    ```
    ```
    .admin_diff [number] - Only admins. This will change the difficulty without vote
    ```
    `In the chat:`
    ```
    /vote diff [number] - All players
    ```
    ```
    /votediff [number] - All player
    ```
    
  - 💡I added a way clamp the difficulty.
    - ⚠️You need to be admin to change this.
    - ⚠️They will not be able to vote under the minimum difficulty.
    - ⚠️They will not be able to vote above the maximun difficulty.
    - ⚠️This will be permanent. And restart will not change this.
    
    `To clamp the difficulty:`
    ```
    .admin_clamp_diff [min number] [max number]
    ```
    `To disable the clamped difficulty`
    ```
    .admin_clamp_diff -1 -1
    ```
