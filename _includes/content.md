
---

*The following are some highlights from my research*

[**Project SuperDex**](https://projectsuperdex.com/) is an open-source simulation platform from Meta for robotic dexterous manipulation, built around a custom physics engine for complex, contact-first interactions.

<video width="100%" controls>
     <source src="//projectsuperdex.com/img/gallery/threadedrodandnut_low.mp4">
</video>

I mainly worked on asset authoring pipelines, including the [SuperDex CAD Exporter](https://projectsuperdex.com/studio/docs/cad_exporter/) and some parts of [SuperDex Studio](https://projectsuperdex.com/studio/docs/overview/).

![CAD Exporter](https://projectsuperdex.com/studio/img/cad_exporter/superdex_cad_exporter.jpg)

---

<!-- ![EMG](/images/emgKeyshot.jpg) -->

**Untitled EMG Project** is an ongoing project where we are trying to learn hand kinematics from a forearm-worn EMG array. For data collection, I built a custom 8-channel EMG armband from scratch based on the ADS1299. The electrodes are 3D printed from electrically conductive TPU. The nRF-based wireless communication, based off of technology developed for our haptics projects, enable low latency (1 ms) streaming to a USB dongle. We stream 1000 Hz data directly to a Meta Quest 2 so we can collect hand tracking data and EMG signals simultaneously, all locally on the headset. This is great for deployment for user studies without the hassle of hardware setup, just plug-n-play. 

![EMG Band Prototype](/images/emgBandPrototype.jpg)

I also developed a data collection VR app that uses physics-based hands with hand tracking to simulate tasks such as pick-and-place (for unstructured data), AR/VR-type gestures and common EMG gestures. The data is also uploaded to AWS S3 storage automatically. Real-time plots and debug interface were drawn using [imgui](https://github.com/ocornut/imgui) + [implot](https://github.com/epezent/implot).

<video width="100%" controls>
     <source src="//user-images.githubusercontent.com/25041773/157564522-c7b8c7fa-c504-42df-85a7-2076a20988bc.mp4">
</video>

I also made this sick data visualizer for the collected EMG and kinematic data. 

<video width="100%" controls>
     <source src="//user-images.githubusercontent.com/25041773/157564826-d1eea89a-9a4d-4ef1-ba22-0f7e73195a99.mp4">
</video>

And lastly, a rather unrelated, proof-of-concept of EMG + Physics Hands 🤝

<video width="100%" controls>
     <source src="//user-images.githubusercontent.com/25041773/159648690-ab742d24-0c57-467c-bf16-f396df00cb52.mp4">
</video>

*We are currently in the process of crunching our numbers from the collected data.*

---

<a href="//github.com/prnthp/experiment-structures">![Bricklayer](https://raw.githubusercontent.com/prnthp/experiment-structures/main/Images~/bricklayer-logo.svg)</a>

**[Bricklayer (Experiment Structures)](https://github.com/prnthp/experiment-structures)** is a framework for a finite state machine that exploits Unity's Scene hierarchy for reordering the states and utilizes Unity's Inspector for configuration. The framework has been used mainly for creating human behavioral experiments (psychophysics) and data collection applications (Haplets, the EMG project, and Chasm, amongst others).
![Bricklayer Demo](https://user-images.githubusercontent.com/25041773/149586598-68d32c66-2e02-4784-9491-6211f6e3d742.gif)


Also works with [AEPsych](https://github.com/facebookresearch/aepsych), from the good folks at Meta. (Adaptive nonparametric psychophysics server for speeding up your experiments)
[AEPsych driven samples for Bricklayer](https://github.com/prnthp/experiment-structures/tree/main/Samples~/AEPsychDriven)


<video width="100%" controls>
    <source src="//user-images.githubusercontent.com/25041773/149590225-a54b8d75-98ba-41a9-8b3d-4c4b7479fba0.mp4">
</video>

**Links**
- [🐙 GitHub Repository](https://github.com/prnthp/experiment-structures)

---

![Haplets Keyshot](/images/hapletKeyshot.jpg)

**[Haplets](https://www.frontiersin.org/articles/10.3389/frvir.2021.738613/full)** are wireless, finger-worn LRAs. They were created to answer the question: “What is the minimum viable haptics that we can add to the fingers to augment hand tracking in AR?”. Our paper covers the hardware design, validation and a user study with Haplets used in conjunction with a pen. Our results suggest that users are more accurate when drawing with Haplets.

![Haplets with a pen](images/hapletsInHand.jpg)

<iframe width="100%" height="340" src="https://www.youtube.com/embed/59zq2DoJdJo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

**Cool facts about Haplets**
- They are wireless but have incredibly low latency (1-4 ms).
- I wrote a semi-custom wireless protocol for them on top of ESB (Enhanced ShockBurst for the nRF SoCs from Nordic Semiconductors).
- Using them with the Quest 2 requires only a dongle plugged into the USB port. No PC required!
- The user study was driven using Bricklayer.
- Visuals are equally important for haptics, so the virtual hands are fully physics-driven and behave semi-realistically.

**Links**
- [📄 Full Paper (Frontiers in VR)](https://www.frontiersin.org/articles/10.3389/frvir.2021.738613/full)
- [🎥 Video](https://www.youtube.com/watch?v=59zq2DoJdJo)

---

![Chasm Header Image](/images/chasmPromo.png)
**[Chasm](https://research.fb.com/publications/chasm-a-screw-based-expressive-compact-haptic-actuator/)** was my project during my 6-month internship at Meta Reality Labs. Chasm is a haptic actuator that is designed to render shear forces and vibrations simultaneously in a form factor no larger than a AAA battery. We prototyped Chasm in a bunch of form factors including a headband, marker, and VR controllers. With the headband, Chasm can be used to nudge user's temples to provide navigation cues. With the marker, Chasm can render high fidelity haptics that simulate textures, forces and even elasticity.

The full presentation given at CHI2020 can be watched here:

<iframe width="100%" height="340" src="https://www.youtube.com/embed/KKBP8giaisY" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

**Cool facts about Chasm**
- Chasm is leadscrew based. We had a custom tiny leadscrew made for it.
- Chasm can exert up to 5 N of force, but we only needed 1-2 N.
- Your fingertips are extremely sensitive, so we only needed to move Chasm's nub by less than a millimeter to generate the illusion of force.
- Two Chasms also work to reduce motion sickness when worn on the head. We used a simple gaiting pattern (tip-tap) on the temples that seemed to do the trick.

**Links**
- [📄 Full Paper (ACM SIGCHI)](https://research.fb.com/publications/chasm-a-screw-based-expressive-compact-haptic-actuator/)
- [🎥 Overview Video](https://www.youtube.com/watch?v=59zq2DoJdJo)
- [🙋 CHI2020 Talk](https://www.youtube.com/watch?v=KKBP8giaisY)

---

![Negshell](//negshell.github.io/images/tripodHeroText.jpg)
**[Negshell](//negshell.github.io/)** is a casting technique that exploits the fragility of thin-walled SLA resin parts to create complex internal structures for soft robots. [Website](//negshell.github.io/), [Full Paper (MDPI)](//journals.plos.org/plosone/article?id=10.1371/journal.pone.0234354)

![ConTact Sensor](/images/contact-sensor-plaque.jpg)
**[ConTact Sensor](//softroboticstoolkit.com/contact-sensor)** is a simple soft robotic sensor that can simultaneously sense force and area. [Soft Robotics Toolkit](//softroboticstoolkit.com/contact-sensor), [Conference Paper (IEEE RoboSoft)](//ieeexplore.ieee.org/document/8722757)

<!-- ![Robot Stabbing](//j.gifs.com/YvW3B0.gif) -->
<video width="100%" controls>
    <source src="//user-images.githubusercontent.com/25041773/158678441-099d7942-f214-427d-b13f-5d79a10a37f1.mp4">
</video>
**[Bishop's Hand](/projects#bishops-hand)** was a project that aimed to measure limb ownership by having users play the knife game on themselves. The video shown is what we *should* have done.

![Prosthetic Hand](/images/prosthetichand.png)
**[My Undergraduate Project](projects/#electric-prosthetic-hand-with-slip-sensor)** was a prosthetic hand with a fingertip sensor that could detect the onset of slip. We CNC machined almost every part of the hand ourselves on a Mazak Integrex. One of the coolest experiences I've ever had. The slip detection sensor deserved a publication of its own!
