# DouBOL Dash
DouBOL Dash was a editor I started back during the summer of 2016 and ended up trashing because I didn't know a thing or two how to code a proper editor. But now it's back!

It is written in C# and uses OpenTK for rendering. Big shoutout to StapleButter for the BMD rendering code, and miluaces for his few patches that I will be using.

# How to use
First, clone or download the repo. To run from source, simply click the solution and set it up (OpenTK references may be missing, it's normal). I used Visual Studio 2015 for this project, and .NET Framework 4.5.2.

If you want to run the EXE, it's located in DouBOLDash/bin/Debug. Note: You have to have the game extracted, and be sure that the BOL you're opening is in the same directory as the bmd course model! If you just extracted the arc and did nothing else, it should be structured fine to work with the editor.

# What's supported
Currently DouBOL Dash can read, render, and save everything except for the last 2 sections, which don't crash the game if removed. The editor just defaults their offsets to the filesize (which is what retail does), so it avoids a crash. Also, rotations are not saved, as they are defaulted to 0f, 0f, 0f until reversing the algorithm is fixed. Please report saving bugs to me!

There is also a BTI viewer for the BTI format, BMD viewer for the model format, the ability to insert your own BMD into the stage while replacing the current course model, and a BCO viewer, which is for collision. Documentation for collision types would be greatly appreciated. Currently, here are the known collision flags:

```
0x000x Sand
0x0100 Road
0x0101 Bridge / Wood
0x0102 Cage Road
0x0103 Dirt Road
0x0104 Carpet
0x0105 Metal Cage
0x020x Bottom part of wall / dead zone border
0x0300 Grass
0x0400 Slippery Ice
0x050x Wario Colosseum cage / Baby Park dead zones / Mushroom City car ports
0x0600 Mario #6 (grassy wall), 
0x070x Wario Colosseum/Bowser's Castle Zipper (zipper on a ramp)
0x0800 Speed Boost
0x0900 Cannon Boost
0x0A0x Rainbow Road/Wario Colosseum dead zones - when falling into air
0x0C00 Yellow Dry Dry Desert sand
0x0D00 Mushroom Brdige warp pipe / Peach Beach warp pipe
0x0E0x Dead Zone Sand
0x0F0x Dead Zone Water/Lava
0x0F01 Lava (might just be like water?)
0x1000 Quicksand Sinkhole
0x110x Peach Beach sand
0x120x Wall
0x1300 Orange out of bounds sand
0x3708 Bowser's Castle zippers
0x470x Area zipper

A 120x is always stacked on a 020x to form a wall
the numbers are for respawns?
```

# Credits
Thanks to Shibbo for originally making this 2 years ago.
Thanks to tarsa for actually wanting to make custom courses for Double Dash and giving me a reason to update this.
Also thanks to tarsa for providing an updated collision flag list.

Thanks to StapleButter for the main BMD rendering code, and miluaces for minor changes. Icons for the project were made by MelonSpeedruns.

# License and Distribution
DouBOL Dash is licensed under the GPL. It is a free program for all users to use. Under this license, a person may not redistribute without credit, or make any profit money-wise.


tl;dr if you take this and make money off of it you will never see the light of day ever again

- shibboleet
