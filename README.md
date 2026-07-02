# DIY-CNC
<img width="1637" height="672" alt="image" src="https://github.com/user-attachments/assets/de0ab22d-49a0-412b-84ac-c37376fa8d15" />

## Overview
**IMPORTANT**: The BOM in this repo is NOT the full BOM. It is my BOM, with only the stuff that I do not have. It is a list of what I had to order. For the full, interactive BOM, please visit [this](https://docs.google.com/spreadsheets/d/1c5oY7mJT4-IrlBDl83cxZs2LZfODYT7Jo5wKYS-iBsA/copy?usp=sharing) google sheets (the apps script thing is a BOM generator, its the only AI used on this project).

This repo contains all the project files for my CNC milling machine. It is based off the IndyMill[^1]/CindyMill[^2], with heavily upgraded electronics based off the PrintNC V4[^3]. The main goal of this project was to make a relatively low-cost CNC machine tuned towards FTC (First Tech Challenge) and FRC (First Robotics Challenge). Unfortunately, due to tariffs and other economic issues caused by the US Government, it ended up being a little more than expected. If you are reading this sometime in the future when the tariffs have been removed, it will most likely be <1000 USD, and probably in the 800 range

While designing this, I tried to take the best parts of both open-source CNC 'archetypes': The Indymill and the PrintNC, while also keeping costs low. I based my frame off the standardized, easy to modify frame of the Indymill, while also beefing up the gantry and frame to mitigate the flexing issues as described in the Cindymill's study of the Indymill[^4]. I based most of the electronics off the PrintNC V4, as they are superior to that of the Cindymill, have better documentation, and are only slightly more expensive (probably added only about $50 USD). It is also more compact, and includes extrusions on the outside of the frame to easily mount a cover/shield.

However, cost was still a big factor in this build, so in order to reduce cost, I made a few cuts. I swapped out the 1.5kw Spindle used by both the PrintNC and Cindymill for the 500w one used in the Indymill, as it would still be enough to cut most things that a high school robotics team would need. Instead of using a Flexihal to control the cnc, as recommened by the PrintNC, I used the PicoBOB + Mach3 Breakout Board, as it is cheaper and provides enough features. I didn't make it as beefy as the Cindymill, as it would have cost a lot more, but I did make it beefier than the Indymill.

The design was done from the ground up, using the Cindymill CAD as a basis for things like the linear motion assemblies.

A build tutorial, firmware settings, and a usage guide will be uploaded once the build is complete and I have done all the necessary adjustments and tunings.

## Build Summary
Mechanical Parts:
- Aluminum Extrusion + 1/4in (or 6mm) Steel Plates for the structure
- SFU1605 (x- and y-axis) and SFU1204 (z-axis) ball screws
- MGN12 Linear Rails with MGN12H blocks
- 2.4NM Open-Loop Stepper Motors + DM542TE Drivers
- 500W Spindle + driver and PSU

Electrical Parts:
- PicoBOB B1 + Mach3 BOB Control System
- 36V 16.6a PSU

## Gallery:
Full Build:

<img width="1482" height="705" alt="image" src="https://github.com/user-attachments/assets/7e89adb9-b58b-4216-a86e-8c1bc72f6744" />

Y-Axis Linear Motion Assembly:

<img width="1253" height="585" alt="image" src="https://github.com/user-attachments/assets/5b95c6ff-432a-4243-8005-d96945510658" />

X-Axis Linear Motion Assembly:

<img width="897" height="502" alt="image" src="https://github.com/user-attachments/assets/2ec83d98-f156-49e9-aff8-e530b4bb6f65" />

Z-Axis Linear Motion Assembly:

<img width="375" height="737" alt="image" src="https://github.com/user-attachments/assets/fae15d9d-abe5-4e9d-bf91-026e031c9132" />

Electrical Box:

<img width="747" height="710" alt="image" src="https://github.com/user-attachments/assets/dd5c7e16-e570-4171-80df-2f685a50eb28" />

For more information, look at the CAD models, my finalized BOM in this repo (does not include all parts as I already have some) or the interactive BOM [here](https://docs.google.com/spreadsheets/d/1c5oY7mJT4-IrlBDl83cxZs2LZfODYT7Jo5wKYS-iBsA/edit?usp=sharing).

## Acknowledgements
I would like to thank Hack Club and Macondo for (hopefully) helping fund this project.

## Sources
[^1]: https://indystry.cc/indymill/
[^2]: http://cindymill.xyz/
[^3]: https://wiki.printnc.info/en/home
[^4]: http://cindymill.xyz/start/2021/07/24/Rigidity.html
