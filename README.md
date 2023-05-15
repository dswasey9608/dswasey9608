### Daren Swasey's Coding Portfolio

Howdy! I am Daren Swasey. I graduated in May 2023 with a Master's Degree in Electrical Engineering 
with an emphasis in Controls and Signal Processing from Utah State University. In 2021 at the 
beginning of my professional program, I held a job as an undergraduate researcher in signal processing 
under Dr. Todd Moon. In that research I used MATLAB for designing and testing algorithms. I used 
Python and C++ for implementing the algorithms in custom GNU Radio blocks. Since August of 2022 
until my graduation, I worked with Dr. Greg Droge as a research assistant. I learned to develop 
components of the ROS2 framework for a simulation environment that was utilized for testing UAV 
path planning under uncertainty. I became more familiar with real-time programming practices and 
utilized C++ and Python.

I have been coding since my middle-school years, dabbling in C# briefly before moving on to C++ in 
high-school. Since then, I have grown to learn Python, Java, C, MATLAB, Assembly, VHDL, Verilog, 
and some Bash scripting. I have a few years of experience with Linux and Git VCS as well, rounding 
off some good software development skills that I have learned over the years in my EE degree and 
from the classes I took in my Computer Science minor. Way before then, my experiences as a member 
of a FIRST Robotics programming team and what I learned from playing with LEGO Mindstorms set really 
showed me the potential of what can be done with code and hardware combined. I have been coding and 
learning how to code better ever since.

I would like to showcase a few things I have done over the years. There's a lot of stuff I 
have done with my skills in electrical engineering and coding. Use the links below to check them out!
Other sections about jobs, internships, and another hobby of mine are on their way soon, so the 
other two sections and other additional sections will be linked accordingly when they are ready.

### [School and Personal Projects](pages/code_projects.md)

### Indoor Geolocation via Machine Learning with Rincon Research Inc.
For an internship in the summer of 2022 at Rincon Research, I had the opportunity to learn how to 
develop a real-time system with the GNU Radio ecosystem. I worked alongside five other interns that had 
experience in signal processing, machine-learning, web-development, and Linux administration. In 
part of my work, I developed a method of synchronizing incoming data from 2 USRP B210 radios linked 
to separate computers. I utilized the ZMQ library in Python with a TCP protocol for message 
transmission between computers on the same network. A server-side desktop received the data from 
both radios and fed it through a neural network to get predictions about the location of a radio 
transmitter. These prediction outputs were then stored in JSON files and sent to a web client 
that would display the data. The goal for the system was to operate at around 5 Hz in real-time and 
I was able to achieve that design goal.

### GNU Radio Multi-Antenna Real-Time Intrusion Detection System
In March of 2021, I began work with Dr. Todd K. Moon, a professor at USU who teaches primarily 
signal processing classes. At the time, I was tasked with the goal of what amounted to an indoor 
"burglar alarm" that ran off of radio signals and software-defined radios (SDRs). After a grueling
process of study, research, testing, failing, testing, progress, and more testing, I was able to 
come up with several algorithms for intrusion detection. These algorithms ran in the GNU Radio 
environment in sort of a pseudo-real-time fashion, and the results were actually quite surprising
in a positive way. Check out my video from GRCon [here](https://www.youtube.com/watch?v=JcKWgyM55To&t=1s). 
It's funny how much work went into this block. It can now be dragged from a menu in two seconds, 
but it took 5 months to make.

![rid_block](images/idl/RID_block.png)
<!--
**dswasey9608/dswasey9608** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

Outline:

- Short intro to myself
- Backstory of how I came to be an EE and software developer
- List of skills and favorite things to do in code
- List of my favorite projects
  - Show images of the absolute best
  - Keep images of others in a folder on GitHub
-->
