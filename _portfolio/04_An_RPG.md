---
style: single
title: "RPG Dungeon Crawler"
excerpt: "Plunder through dungeons destroying enemies with powerful abilities. No epic loot here, unfortunately."
header:
  image: /assets/images/rpg_/header.png
  teaser: /assets/images/rpg_/title_screen.png
gallery:
  - url: /assets/images/rpg_/title_screen.png
    image_path: assets/images/rpg_/title_screen.png
  - url: /assets/images/rpg_/screenshot_001.png
    image_path: assets/images/rpg_/screenshot_001.png
  - url: /assets/images/rpg_/screenshot_002.png
    image_path: assets/images/rpg_/screenshot_002.png
  - url: /assets/images/rpg_/screenshot_003.png
    image_path: assets/images/rpg_/screenshot_003.png
  - url: /assets/images/rpg_/screenshot_004.png
    image_path: assets/images/rpg_/screenshot_004.png
  - url: /assets/images/rpg_/screenshot_005.png
    image_path: assets/images/rpg_/screenshot_005.png
---


I tried my hand at making an isometric RPG dungeon crawler, for teaching purposes of course.

This project was created to teach beginner programming club members basic coding and game development.
We covered variables, functions, data structures, classes, inheritance, and software principles like DRY and Open-Closed.  
Things a second year computer science student should know.

{% include gallery %}

### Implemented features:
 * Account creation/login
 * Character creation
 * Character selection
 * Core game mechanics:
    - Character abilities
    - Level system with progression
    - Basic enemy AI (roam and attack)

When creating this game, I focused heavily on polymorphism as many of the game objects perform similar tasks.
For example, the ability icons are derived from a basic ability class. 
Using this method, it makes creating and changing your classes abilities extremely simple.
Furthermore, the enemy and player game objects are derived from the same character class. 
This makes implementing the combat and movement system smooth as both the enemies and player use the same combat and movement systems.


This project was never ment to be finished as it was used solely for teaching purposes.
However, you can play it to see all that in action.

### Windows version:
  * [v1.1.1200](https://www.dropbox.com/s/v9wuhxqln52utq1/iso_rpg.exe?dl=1)

### Controls:
  * Left click - select enemy as target, select menu buttons
  * Right click - move to location
  * 1, 2, 3, 4 - use abilities
