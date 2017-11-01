---
layout: single
title: "Real Time Strategy"
excerpt: "Gather resources, build all your base, and destroy your enemies?"
header:
  image:  /assets/images/rts_/header.png
  teaser: /assets/images/rts_/title_screen.png
gallery:
  - url:       /assets/images/rts_/archery.png
    image_path: assets/images/rts_/archery.png
  - url:       /assets/images/rts_/barracks.png
    image_path: assets/images/rts_/barracks.png
  - url:       /assets/images/rts_/deposit_house.png
    image_path: assets/images/rts_/deposit_house.png
  - url:       /assets/images/rts_/archer_tower.png
    image_path: assets/images/rts_/archer_tower.png
  - url:       /assets/images/rts_/frost_tower.png
    image_path: assets/images/rts_/frost_tower.png
  - url:       /assets/images/rts_/fire_tower_lv1.png
    image_path: assets/images/rts_/fire_tower_lv1.png
  - url:       /assets/images/rts_/fire_tower_lv2.png
    image_path: assets/images/rts_/fire_tower_lv2.png
  - url:       /assets/images/rts_/fire_tower_lv3.png
    image_path: assets/images/rts_/fire_tower_lv3.png
  - url:       /assets/images/rts_/seige_tower_lv1.png
    image_path: assets/images/rts_/seige_tower_lv1.png
  - url:       /assets/images/rts_/seige_tower_lv2.png
    image_path: assets/images/rts_/seige_tower_lv2.png
  - url:       /assets/images/rts_/seige_tower_lv3.png
    image_path: assets/images/rts_/seige_tower_lv3.png
    
---

What happens when you try to create one of the most complicated types of games with no programming experience?  
You get something like this:

![There is supposed to be a picture here.](../../assets/images/rts_/screenshot_002.png "Super alpha screen shot")

It might look the same as the newer version but that is because the art assets remained the same.  
The older version uses naive pathfinding which only checks in infront of the unit to maneuver around obstacles.
Furthermore, there are no observers for selected units and no action buttons (even though they are drawn) to give units commands.
The combat system is very simple and only uses distances between two base classes to determine where to move and what to attack. 
The selection system is also very trivial and toggles a boolean value to indicate if a unit was selected.
Workers are dumb and will only automatically gather from resources which are nearest to them. 
They don't care that you want them to stand there and not do anything, they are workers! That's all they know how to do!
What can I say, I didn't know any awesome algorithms or data structures that would have helped me make a more robust project.


### Updated! Oh boy!
After I was done with 2 years of college and learning the basics of C++/ Java languages, I decided to revisit this forgotten project.
Most of the old "code" I wrote was gutted and replaced with the programming knowledge that I had learned from college. 
A robust unit selection system was put into place, using data structures to keep track of which units were selected and display them on the GUI.
The naive pathfinding was replaced with A* pathfinding, however, I didn't make the units into solid objects for simplicity.
Workers had a brain installed and now are much smarter at their tasks, locating similar resources near them if the current is depleted. 
An "action-queueing" system was set into place and each unit can have a series of actions assigned to them, which they will perform one at a time.


![alt text](../../assets/images/rts_/screenshot_003.png "Worker about to build a main camp")


Workers were also upgraded with the ability to construct buildings, no more random letter key assignments for placing buildings!
Unfortunately, you now have to collect the required amount of resources. 

Resource locations where given a worker capacity which functions like a mutex (GameMaker language [GML] doesn't have mutexes or threads available to the game developer.)
You can see the worker capacity near the resources, they are the blue numbers. The top number is the maximum capacity, the bottom is the current capacity.
The tricky part was getting it to work when a worker died while gathering from the resource.

I did run into some limits with GameMaker Studio and GML, one of them being the number of inheritance layers you can use.
GML only allows for a base class and a derived class, and it has no concept of interfaces. So if you want to have a hierarchy of 3 classes, you can't.
An example of this would be, a unit class as the base, a building class derived from the base, and a main camp class derived from building class.
This way, you can split the functionality vertically along the inheritance hierarchy starting from the most general functions to more specific functions.

  
### Art Assets:  
Here are some of the models I made that are not accessable in the game. I built these using Google Sketchup. The buildings in the game are not 3D models, they are 2D sprites of 3D models.
{% include gallery %}



### Windows version:
  * [Super Alpha](https://www.dropbox.com/s/o4ug5ba7b6nfcsp/RTS_alpha.exe?dl=1)
  * [Latest Alpha](https://www.dropbox.com/s/o4ug5ba7b6nfcsp/RTS_alpha.exe?dl=1)

### Controls:
  * Left click - select units
  * Right click - order selected units to move
  * Delete - destroys the selected unit
  * Older version extra controls:
    - A key - spawn Archer tower at cursor location
    - B key - spawn Fireball tower at cursor location
    - C key - spawn Frost tower at cursor location
    - D key - spawn Cannon tower at cursor location
    - E key - spawn wood resource at cursor location
    - F key - spawn gold resource at cursor location
    - G key - spawn stone resource at cursor location
    - H key - spawn food resource at cursor location
    - I key - spawn deposit camp at cursor location
    - J key - spawn main camp at cursor location
    - 1 key - spawn a frost wizard at cursor location
    - 2 key - spawn an archer at cursor location
    - 3 key - spawn a knight at cursor location
    - 4 key - spawn a warlock at cursor location
    - 5 key - spawn holy knight at cursor location
    - 6 key - spawn a worker at cursor location
    - 7 key - spawn crossbowman at cursor location
    - 8 key - spawn flame wizard at cursor location
    - 9 key - spawn lightning wizard at cursor location
    - 0 key - spawn spearman at cursor location