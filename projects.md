---
title: Projects
permalink: /projects/
---
## Chasm: A Screw Based Compact Haptic Actuator

*Co-authors: Ali Israr, Majed Samad*

*Made with: DC Motors, Leadscrews, Oculus Quest, Unity, Teensy 4.0*

**Chasm has received an 🏆Honorable Mention Award (Top 5%)!**

[Full Paper](https://research.fb.com/wp-content/uploads/2020/02/Chasm-A-Screw-Based-Expressive-Compact-Haptic-Actuator.pdf?)

<iframe width="580" height="340" src="https://www.youtube.com/embed/kqBE4JDJ7QI" frameborder="0" gesture="media" allowfullscreen></iframe>

<iframe width="580" height="340" src="https://www.youtube.com/embed/KKBP8giaisY" frameborder="0" gesture="media" allowfullscreen></iframe>

Chasm was my primary internship project at [Facebook Reality Labs](https://research.fb.com/category/augmented-reality-virtual-reality/)! Chasm is a miniature haptic actuator that can render shear forces and vibrations both independently and simultaneously through a single tactor. Chasm can render constant shear forces up to 4.8 N at 3.4 mm and vibrations perceivable up to 170 Hz. The underlying mechanism is as simple as it gets: a leadscrew coupled directly to a DC motor. I designed and developed Chasm from the ground up, starting from the selection of the motor and leadscrew. We had to order custom leadscrews due to the unconventional usage! Underneath the leadscrew nut, there is an ams AS5311 magnetic linear encoder that lets me control the motor at 1000 Hz with sub micron accuracy. Chasm has a Teensy 3.5 (and later on, a Teensy 4.0) microcontroller running the closed-loop control. I also developed a whole HID-based haptic interface so Chasm can be used with VR devices like the [Oculus Quest](https://oculus.com/quest). (also android phones, macOS, Windows, etc.) This means Chasm's firmware can communicate with the host device (the Quest) at an ideal 1 ms latency!

![Promo](/images/chasmPromo.png)

![Marker](/images/chasmMarker.jpg)
Here is Chasm in one of its many form-factors: the marker. The user places their thumb on Chasm's tactor and together with VR, Chasm can render extremely convincing haptic illusions of texture, weight, stiffness and impact. The marker itself doesn't have any tracking so its tracked with Oculus Touch controller strapped to the user's hand. The strap alone is a marvel of accidental engineering - getting the controller to sit on the hand like that took so much fiddling around with how the strap loops around.

![Demos](/images/penDemos_transparent.png)
I also made a bunch of demos in Unity for Chasm that highlight how Chasm can render a wide range of modalities and bandwidth. It's hard to convey with pictures or a video, but the haptics are freakin' amazing! Even the simplest drawing demo, where Chasm renders a constant pressure when you press the pen against the board along with vibrations to simulate friction when you write, is extremely convincing.

<hr>

## ovrseer

*Made with: Unity, OculusSDK*

![ovrseer preview](/images/ovrseer.png)

**ovrseer** is a psychophysics experiment framework for Unity/VR that enables rapid prototyping for creating experiences. ovrseer has a finite-state-machine backbone that splits experiment into "Phases", multiple Phases into "Trials" and multiple Trials into "Blocks". Each Phase is a finite state that does something upon start (Enter()), during the game loop (tied to Unity's Update()) and at the end (OnExit()). Phases are often treated as events that change the behavior of things in the scene such as: showing a target, moving and object, start recording kinematic data, blindfold the subject, etc. . Trials, with their multiple Phases can then be repeated. And finally a chain of Trials make up a block. All of which is maintained using Unity's Scene Hierarchy, which means Phases can be drag-and-dropped, copy-pasted and moved around freely to rearrange their order.

<iframe width="580" height="340" src="https://www.youtube.com/embed/XVP5OJemTsg" frameborder="0" gesture="media" allowfullscreen></iframe>

ovrseer also has built-in recording capabilities for saving kinematic data (tracked controllers) and experiment logs.

<iframe width="580" height="340" src="https://www.youtube.com/embed/fV_7ZzRXQIE" frameborder="0" gesture="media" allowfullscreen></iframe>

<hr>

## ConTact sensor

*Made with: PlatSil-Gel 25, Chopped Carbon Fibers, ROS, LABView, NIDAQ*

**Full paper available [here](/publications)**

**Good News! We got a honorable mention from the competition!**

**Published on the Soft Robotics Toolkit [here](https://softroboticstoolkit.com/contact-sensor)**


The ConTact sensor is my entry for the 2018 [soft robotics toolkit](https://softroboticstoolkit.com) competition for contribution to soft robotics research. It is part of Rombolab's Pneudraulique research theme.

<iframe width="580" height="340" src="https://www.youtube.com/embed/XoLCroADij8" frameborder="0" gesture="media" allowfullscreen></iframe>

The ConTact Sensor is a force and contact area sensitive sensor developed at rombolabs at the University of Washington that can be easily integrated into most soft-robotics designs. Using the fluidic conductive medium already inherent in soft robots, the sensor can sense the force and size of an object pressing into it. The main sensing element is a conductive fluid core with conductive rubber leads and the force and size is derived by measuring the resistance and pressure changes of the fluid. The sensor is mostly fabricated from silicone rubber with minimal external components. This guide provides details on how the sensor works, how to fabricate the sensor and how the sensor was tested and validated.

*The name ConTact is from the main principle of sensing: a Conductive fluid and the sensor itself being a Tactile sensor*

Below are examples of raw sensor readings. When objects of different sizes are pressed against the sensor with the same amount of force, the sensor shows distinct responses for each object size.

![Graphs](https://rombolabs.github.io/img/portfolio/contact-graphs.png)

<hr>

## Bishop's Hand

*Made with: Unity, ROS, SteamVR, C#, C++, Shimmer GSR+, Oculus Rift & Geomagic Phantom*

A project that involves Psychophysics, Virtual Reality and stabbing hands.
![VR Hand](/images/bishopshand.png)

How much would you trust the robot you programmed? (This robot is animated directly from Unity!)
![Stabby mcstabface](//j.gifs.com/YvW3B0.gif)

<hr>

## Pneudraulique

*Made with: SolidWorks, Matlab, NIDAQ, ROS & Teensyduino*

Peudraulique is a blanket term for adventures into the soft-robotics space. We're currently trying to use fluid filled volumes to become both actuators and sensors in the same embodiment.
![Soft finger concept](/images/pneudraulique.png)

See [blog](/ramblings) for updates!

<hr>

## Scalpl

*Made with: C++, CUDA-C, VB, SolidWorks & GLUI*

<iframe width="580" height="340" src="https://www.youtube.com/embed/5oqBlZqFfIU" frameborder="0" gesture="media" allowfullscreen></iframe>

A project for [Prof. Duane Storti](//www.me.washington.edu/people/faculty/duane_storti)'s [Voxel Modeling](//blogs.uw.edu/ceadvice/2015/11/17/voxel-modeling-introduction-to-applied-gpu-based-parallel-computing-course/) class. Scalpl is comprised of two separate pieces of software: 1) a SolidWorks plugin and 2) a CUDA accelerated voxel editor. The aim of the project is to prepare files for ingestion by a Stratasys Objet 3D printer in order to print voxels directly.

![Slicing](/images/slicing.gif){:width="250px"}
*Literal slicing in SolidWorks*

![Scalpl's UI](/images/scalpl2.PNG)

Additionally, Scalpl can modify exported voxels directly and create lattices or porous volumes. Although by the end of the course Stratasys has yet to make voxel printing available to our lab, Scalpl is ready to be modified to support any format Stratasys wants.

![Scalpl's Voxel Editing](/images/scalpl3.PNG)
![Results](/images/result1.gif){:width="250px"}
*Voxels!*

<!-- *PS: Fuck you SolidWorks API SDK* -->

<hr>

## Cobalt Chromium Femoral Heads

*Made with: Okuma LB-3000 EX MYW, Catia, Blood, Sweat & Tears*

A project under [Prof. Pairat Tangpornprasert](//www.researchgate.net/profile/Pairat_Tangpornprasert) & [Prof. Chanyaphan Virulsri](//www.researchgate.net/profile/Chanyaphan_Virulsri) of the Biomechanical Design and Manufacturing Laboratory, Thailand. One of the most arduous projects to date. The goal was to produce Cobalt Chromium femoral heads with sub 5-micron roundness using a traditional 4-axis CNC lathe. These femoral head implants are normally *ground* to shape. In my brief stint as a machinist, this project has taught me a lot on how to machine to extremely close tolerances. Despite that, I am nowhere near a true machinist, I highly respect them and the [work](//www.youtube.com/user/oxtoolco) that they do.

![Cobalt Chromium Heads](/images/cocrheads.jpg)

<!-- *PS: Fuck you Okuma's ADMAC-Parts* -->

<hr>

## Electric Prosthetic Hand with Slip Sensor

*Made with: Mazak Integrex 200, Maxon Motors, VB, C, Teensyduino, Smooth-on PMC*

[Poster for Project](/media/handposter.pdf)

A senior project with [Pongsakorn Laiwattanapaisan](//www.facebook.com/pongsakorn.laiwatthanapaisan) & [Possawat Munnitivorakul](//www.facebook.com/possawat.munnithivorakul).

We designed, programmed, CNC-machined almost *every single part* aside from the motor and gearbox, ourselves.

![Electric Prosthetic Hand](/images/prosthetichand.png)

Here's slow motion footage of our slip detection working on a 500g weighted glass jar:

![Slip detection on glass](//j.gifs.com/N9L316.gif)

And grasping a jar with the slip detection turned off:
![No slip detection on glass](//j.gifs.com/xvnKzr.gif)

And yes it is delicate enough to handle an egg:
![Egg!](/images/egg.jpg)

<hr>

## Undergraduate CAD project

*Made with: CATIA V5, Keyshot*

Final project for CATIA class: Mazda 13B Rotary Engine
![13B Shaft](/images/13b-shaft.png)
![13B Engine](/images/13b-1.jpg)
![13B Engine 2](/images/13b-2.jpg)
