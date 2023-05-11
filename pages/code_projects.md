**Table of Contents**
- [Proudest Achievement: My Own "2D Printer"](#proudest-achievement-my-own-2d-printer)

# Summary
This page showcases some of the things I have done for school and for personal projects. I have
worked with a large variety of systems, languages, and tools over the course of my education. Each
new experience brought its challenges, but I always had fun in the end. 

# "2D Printer"
<!-- insert image of 2D printer results -->
![completed_images](../images/completed_images.jpg)

"Plotter" is definitely the common name for this, but I wasn't aware of it until I did some more 
research. For the Mechatronics class at USU, the main objective of the class was to design a build
a project of your own choosing. My team included myself and two mechanical engineers. We decided we 
wanted to build a "2D Printer", or in other words as described by one of my teammates, a 
"drawing gantry" (I would never have come up with that term. It isn't that I don't like it, but it 
is clearly a mechanical engineer's mind at work, haha).

To summarize:
- Utilized a BeagleBone Black Microcontroller
- Made edge detection, path tracing, and path following code from scratch. No 3rd-party libraries 
for me! (except the ones that ran the Beagle)
- It worked. It also happened to make some really cool images. Below is one that I came up with and 
plotted using some assets I found online.

<!-- Show the LotR image -->
![lotr_images](../images/lotr_progress.jpg)

This project required the development of analog circuitry to control servos that moves the drawing 
utensil around the plotting space, power considerations, 3D printing, image processing, simple path 
planning algorithm considerations, and plenty of programming.

The project utilized Teknic ClearPath Servos to operate. These were controlled by a BeagleBoneBlack 
microcontroller.

The flow of the system was intended as follows:
1. Do edge detection on an image to extract the edges to draw.
2. Store the edge detection and generate paths for the plotter to follow as it drew the image
3. Convert pixel map data to servo commands
4. Iterate through the commands to draw an image.

One additional feature was path scaling, used to convert an image of a given size to be bigger on 
the drawing surface.

The machine was able to produce some simple but quite amazing drawings!

# Minimum Distance Optimal Control of Robotic Manipulator
<!-- Highlight efforts made and what I learned -->

# Simplified Tetris
<!-- Include information about interfacing with the accelerometer -->

# Conway's Game of Life
<!-- Must include Sonic the Hedgehog recording somewhere in here -->

# 