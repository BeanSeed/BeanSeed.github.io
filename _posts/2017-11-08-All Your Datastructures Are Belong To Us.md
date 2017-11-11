---
layout: single
title: All Your Datastructure Are Belong To Us
author_profile: false
---

### The Dream
Ever since I discovered the RTS game genre I have always wanted to create one. I started this game in my early years of game development, way before I even understand anything about programming. I was determined and I didn’t want anything to stop me from creating my very own RTS. That is why, without any programming experience, I still attempted to create the game even after being told that it would be impossible for one person of my skill.
 
The first version had just some units moving around. Moving things around is easy on a computer. However, I did not have selection implemented so the units just moved freely on the screen.

Due to my lack of experience and knowledge of the fine arts of programming, I hit a brick wall with this game. I decided that I was going to learn more about programming languages before continuing to develop this RTS.
 
Come several years later and hundreds of hours practicing and learning software development skills, I was able to create a simple selection, pathfinding and combat. Then I stopped again because the skills I learned were still not enough. However, this did not disgruntle my ambition and I continued to absorb and understand more advanced software development techniques and patterns.
 
Finally, after about five years of starting this game I had the necessary skillset to fully develop this RTS game. Of course there were other problems now.

### Starting to Look Like an RTS
The image on the left with the red squares is the current version of the game. It has selection, resource gathering, building, unit construction, and awesome pathfinding. All of these features may seem simple however, they are quite complicated.
 
First off, selection. It is just clicking and dragging your mouse to create a square on the screen, right? Wrong. That is just the part of it that the player sees. On the computer side of things you have to find all of the units that fit into the box, store their references into a data structure and display them neatly on the control panel at the bottom of the screen. Furthermore, you have to put correct commands in the commands panel which is located to the bottom right of the screen. You don’t want to put commands in there like build and repair if you have various types of units selected. This would make the command panel cluttered and might confuse the game. On top of that, you have to make sure that your control panel displays the correct units. What if a unit dies? What if a unit goes inside of a building? All of these questions have to be answered and the control panel has to constantly update the display with the proper units.
 
For resource gathering I have come into some problems, mainly keeping track of which worker is at which resource node. There are many things that can go wrong in the game while your workers are laboring away. Their labor cycle goes like this: walk to a node, collect resources until they can’t carry anymore, walk back to a resource deposit building, deposit resources, walk to a node, repeat. If implemented incorrectly the worker may claim a resource node which prevents the other works from using it and completely forget about it. The player may distract the worker by making the worker walk to a different location, or by interrupting their gathering to make an early deposit. The worker may be killed by enemy units and not free the resource nodes to other workers. This problem also arises in general Computer Science as race condition and deadlocks. One way of solving the problem is to use semaphores which are a type of data structure used to prevent processes on a machine from hogging and locking up resources. I used the same approach here. Each node has a semaphore type system, it allows a certain amount of workers at the node and it frees up space as a worker leaves the node. Also, because the resource node takes care of keeping track of workers, the workers do not need to free the resource which means that if the worker gets interrupted or dies, the resource frees itself.
 
These concepts would not be possible to implement for me without the knowledge I gained from studying computer science.

