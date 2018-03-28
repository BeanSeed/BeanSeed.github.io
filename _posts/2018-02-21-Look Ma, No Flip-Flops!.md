---
layout: single
title: Look Ma, No Flip-Flops!
author_profile: false
---

### This Gem of a Game
I have discovered, probably one of my all time favorite games. 
The game is called [Oxygen Not Included][oxygen_link].

It is a futuristic space-age mine and craft and survive type of game.
The game is developed and published by [Klei][klei_link] who also made [Don't Starve][dontstarve_link].


This game is just amazing. After seeing someone play it on a video, I didn't give a second thought about whether
to buy it or not. I just did.

No regrets.


As I played the game, and got further and further into the research tree, my duplicants discovered the automation system.
The automation system allows your duplicants to automate their base using logical gates and inputs, this helps your base with efficiency and resource management.
With my Computer Science background, I wanted to see how complicated of automation systems a player can design. 

So I set out making this:
![Oh my glob there should be an image here, where did it go!?](../../assets/images/blogs/lol_its_a_counter_.png)

In the image from left to right:
* The first purple outlined component is a two digit 7-segment display made to display the numbers 0 - 15 in decimal (4 bit binary).
* The second component is the display logic which takes the 4 bit signals and tells the 7 segment display which parts to light up or dim.
* The component in the red rectangle is a 4-bit Ripple Carry Full Adder with connections to the next component and increases the value by 1 each clock cycle. 
* The component in the green rectangle is the 4-bit register which is made from D-Flip-Flops (Tricked! There are flip-flops!) which is driven by the clock. 
* The clock is the cyan colored rectangle and it is an SR-Latch that also has a buffer gate. 
It isn't a double NOT gate, however it's called a buffer gate in the game. The buffer gate is used to slow down the clock so that the game doesn't crash from trying to compute all the logical 
outputs from the gates at a high frequency thus causing the CPU to be overwhelmed and stall. 

This thing works great and I was going to use it as a counter for something I wanted to add in the game, however, 
it would slow my computer to a halt if I added in all the other parts of the game with the duplicants running around in there. 

Also, I am very curious if my computer would be able to hand a mini-cpu with a register file and RAM.

Would be very interesting to see.



[klei_link]: https://klei.com/
[oxygen_link]: https://klei.com/games/oxygen-not-included
[dontstarve_link]: https:////klei.com/games/dont-starve
