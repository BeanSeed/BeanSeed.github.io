---
layout: single
title: Simple Compiler 
author_profile: false
---

### The Origin
Recently, I have been working as a Computer Science Tutor.

I have had students come to me with questions from all areas of the computer sciencey bits: programming introduction classes, data structures, assembly, machine learning, and compilers to name a few.
The languages the students were working with covered mostly C, Java, Python, C++, and a couple assembly languages.

However, there was this one assignment a student was working on that really got to me.
It got to me in such a way that it made me want to write a simple language for the assembly language we were working with.
The assembly language was for the Simple Computer, found in the book [Logic and Computer Design Fundamentals], it is an Academic assembly language tool that is used in conjunction
with teaching digital components. The student had to write a program that would run on a 16 bit Simple Computer CPU. 


![there should be a picture of the language here](../../assets/images/blogs/simple_assembly_language_instructions.PNG)


The program itself wasn't difficult to write, however, the limitations of the language made it infuriating to work with.

First annoyance arose from the fact that the Simple CPU accepted 16 bit instructions.
This means that the immediate values that we can store into registers are going to be small.
For instance, loading the immediate value of 0xFFFF into a register for masking becomes an annoying task. 
Instead of loading in the mask, you have to load in 0x7 then bit shift to the left and add one, **thirteen times**!
That is twenty-four instructions instead of one just to create the mask!

Another annoyance was that there are no labels in the Simple Computer Assembly language.
You have to manually count out the instruction numbers and assign that number to a register so that you can jump to it.
This increases the amount of tedious work you have to do, something that gets in the way of understanding how CPU's work.
It also makes maintaining your code impossible! Adding or changing the amount of instructions before a jump requires you to recount
and recompute the jump addresses!


These problems have got to go!

### Similar Problems
This same problem can be seen in other areas of academia.
In my years at UCSD, I worked as a tutor and while working there I noticed a strange pattern that exams had when it came to testing students.
The pattern was predominantly visible in classes that require very meticulous work, computer architecture classes for example.
The exams had multiple questions that involved the same mundane work.

An example of this mundane work is creating a K-map for 4 literals. 
Why have the student create 3 K-maps on a timed test? This only consumes time for the student and makes the student repeat the same steps they would have on the first K-map.
This means that testing the student on one K-map would be sufficient enough to understand if they know how to create a K-map.

In believing so, this means that having the student count out the instruction number in their assembly language does not facilitate learning of the assembly language, but
instead just irritates the student and robs them of the precious time they have to learn something useful.
This is why I set out to create a simple language! 


Also, because I am a bit bored.


[This link will be to the completed project](#)

[Logic and Computer Design Fundamentals]: https://www.amazon.com/Logic-Computer-Design-Fundamentals-4th/dp/013198926X