# Summer Internship at Rincon Research Corporation
I was privileged to go to Tucson, AZ to work as an intern in the summer of 2022. This was between
finishing my senior year of my undergraduate program at Utah State and starting my last year of my
graduate program (I was in a concurrent program, so got a bit of a fast track). I was selected along
with five others to participate. Three of us were in electrical engineering with a signal processing
background, and two were majoring in computer science. The last intern was actually still in high
school and was functioning as the IT guy for the rest of the interns. He did a fantastic job for not
having any prior experience with Linux or many IT-related skills.

The project us interns had the opportunity to work on was a machine-learning-based indoor geolocation
system. In other words, indoor GPS. For the purposes of our internship, we assumed that the target
to be tracked would have a radio transmitter (which I agree, is part of what GPS is, but the 
research direction was to be able to do it without a transmitter on the target. Thus, I bring it up).

The project was considered a success. By the end of the internship (two months), we were able to get 
a general position in the Rincon building of the transmitter, which could be displayed in real-time
at a rate of 5 Hz on a webserver. Were there a lot of problems still? Absolutely, but it goes to 
show how complex an indoor GPS can be.

You might be wondering, "what did this thing look like"? Well, not very exciting in a shiny and 
fancy new technology sort of way. Most everything was done over a wireless network since we needed
to plant Ettus Research radios across the first floor of the building we were working in. The processing
for the data was distributed between some workstation-esque laptops connected to each radio in use
and some desktops supporting the synchronization of data and porting some of that data to a webserver
for transmitter location display. In the end there were just two receivers and one transmitter. 
More receivers would usually mean better in a situation like this. For any machine-learning problem, 
extra data never seems to hurt, but we didn't have the time nor the resources to get more receivers
integrated into the system.

The key things I learned as part of this internship include:
- Network communication protocols
- GNU Radio capabilities (to add to what I began to learn at the [IDL](./idl.md))
- Needs for team goal setting and planning
- Digital spread-spectrum (DSS) communication
- 

Below I will go over a few of the things that I worked on in this system.

## System Overview
![system_diagram](../images/rincon/overview_restruct.svg)

Aside from a few things I will explain here, the diagram is fairly straightforward regarding the
process of data in to data out. The confusing part is probably the red arrows and the components
split onto the lower line. The red arrows indicate that a particular block is either completely
designed for real-time operation, or has a separate part of it designed specifically for a real-time
implementation. 

The components I played a role in developing are:
- The entirety of the contents of the first dotted box, all of which are part of GNU Radio
- Entirety of contents of second dotted box, the real-time GNU Radio components
- `Data Sync` block
- Real-time parts of the `File System` block

## PN Sequences and Raw Data Collection
I won't go into a lot of detail here, but for the interested reader, you can take a look at my
[end-of-internship report](../docs/rincon_report_signed.pdf) for more information.

A pseudo-noise (PN) sequence can be used in digital communications to spread out a signal across
the frequency spectrum, called a spread-spectrum signal. All the PN sequence is is a sequence of numbers
typically `2^n` in length, with random values. If those values were considered in the time-domain,
they would look very sharp. In the frequency domain, the power is spread across a huge range of
frequencies. What this accomplishes is pretty awesome. 
Usually in digital communications, engineers need to be concerned about the noise floor, or the 
power level of the random radio signals floating around in the air. If a particular signal is below 
the power level of the noise floor, it can be really difficult to pick up on the receiver side of 
the signal. However, with a spread-spectrum signal, as long as the receiver know

