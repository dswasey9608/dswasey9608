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
research. For the Mechatronics class at USU, the main objective of the class was to design and build 
a project of your own choosing. My team included myself and two mechanical engineers. 

To summarize:
- Utilized a BeagleBone Black Microcontroller
- Made edge detection, path tracing, and path following code from scratch.
- It worked. It also happened to make some really cool images. Below is one that I came up with and 
plotted using some assets I found online.

<!-- Show the LotR image -->
![lotr_images](../images/lotr_progress.jpg)

This project required the development of analog circuitry to control servos that moves the drawing 
utensil around the plotting space, power considerations, 3D printing, image processing, simple path 
planning, and plenty of programming.

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
This project was the last project I worked on as part of earning my Master's degree. The design goal
was to move a robotic manipulator end-effector from one point to another in a straight line. I 
learned how to derive simple forward kinematics for robotic manipulators for this which was quite fun.
One can feel pretty powerful once one learns forward kinematics, being able to know any position of
any joint given the joint angles and distances of the robot! Unfortunately I was not able to complete
this project on time due to some struggles with the implementation methods I tried. I used a
optimal control toolbox called [OCS2](https://github.com/leggedrobotics/ocs2) for my initial attempt,
then switched to MATLAB for another attempt. Though neither successfully satisfied the objective
due to lack of development time, I was still able to get part of the problem mostly working in `OCS2`.

The optimal control problem was developed originally as a Bolza problem, and manipulated slightly
to operate within the framework of the tools I used to attempt to implement the solution. The `OCS2`
implementation got the closest to looking like a real solution. The MATLAB implementation got nowhere
close.

The report I wrote regarding the results of the project can be found 
[here](../docs/school_personal/optimal_control_final_project.pdf). Be aware that the link to the
GitLab repository is inaccessible because the project was part of a larger hierarchy for which
I do not have the ability to change access permissions.

# Simplified Tetris
<!-- Include information about interfacing with the accelerometer -->
This project was part of my *Reconfigurable Computing* class at USU. The final project for the class
was to use an Intel DE10-Lite FPGA development board to create a simplified Tetris game, with sound,
score, visuals, and some method of control. Because I was in the graduate version of the class, my
lab partner and I were required to interface with and use an accelerometer to control the location
of the falling block in the game. All code was written in `VHDL`. You can watch a video of the results
[here](https://youtu.be/R3DakccRPjQ).

I spent a ridiculous amount of time working on the accelerometer control while my lab partner did most
everything else. I would have liked to work on more, but I just kept on running into issues with 
the accelerometer. Communication with the onboard accelerometer was achieved using the SPI protocol.
A driver for the low-level SPI communication was created, which passed information to a SPI "controller".
The SPI controller operated on 16-bit input and output data segments while the driver worked with
the individual bits. Only the x-axis data was necessary for the game controller to be implemented,
so that simplified the work a little bit.

The final product of the work on the accelerometer was a game controller that had a center deadzone
to reduce "noise" on the motion from the user. The tilting motion in the left or right direction
would move the block in that respective direction, and the block would persist in a given column
of the game map when the user returned the board to the neutral position within the established
deadzone.

The onboard accelerometer was an ADXL345 accelerometer, with the data rate set to 100 Hz.

# Conway's Game of Life
<!-- Must include Sonic the Hedgehog recording somewhere in here -->

# 