---
title: Tools
permalink: /tools/
---
A collection of tools (usually built out of frustration), both software and hardware I've made or contributed towards.

## Drill bit adapter and handle for drilling/reaming 3D prints
These adapters are for adding a small handle for your drill bits or reamers so you can hold them without using pliers that might mar the shank or having to chuck the bit in a larger tool. You can also print the handle for more ergonomic drilling.

![Drill bits and adapters](//media.printables.com/media/prints/77174/images/834471_cb9eddba-7b18-4e23-93eb-f4ceb60249a1/thumbs/cover/1280x960/jpg/hero.webp)

**Links**
- [🖨️ Printables](//www.printables.com/prints/77174-drill-bit-adapter-and-handle-for-reaming-3d-prints)

---

## Bricklayer - Experiment Structures for User Studies in Unity
Bricklayer (Experiment Structures) is a framework for a finite state machine that exploits Unity’s Scene hierarchy for reordering the states and utilizes Unity’s Inspector for configuration. The framework has been used mainly for creating human behavioral experiments (psychophysics) and data collection applications (Haplets, the EMG project, and Chasm, amongst others).

![Bricklayer logo](//raw.githubusercontent.com/prnthp/experiment-structures/main/Images~/bricklayer-logo.svg)
![Bricklayer Example](//user-images.githubusercontent.com/25041773/149586598-68d32c66-2e02-4784-9491-6211f6e3d742.gif)

**Links**
- [🐙 GitHub Repository](//github.com/prnthp/experiment-structures)

---

## UnityPhysXPlugin - Android (armeabi-v7a + arm64-v8a, IL2CPP support)
I built this out of frustration of the lack of support from NVIDIA 😔. This is a fork of an existing repository.

Experimental Unity package to enable access to NVIDIA PhysX SDK 4 from within Unity.
This fork is specifically set up for building for Android. All references to CUDA have been commented out.
Tested on Unity 2020.2.0f1, built with NDK v23's cmake toolchain on macOS 10.15

Example running on Quest 2:
<video width="100%" controls>
     <source src="//user-images.githubusercontent.com/25041773/128762055-aa27b915-9534-4060-b4cf-142b52b2cd1f.mp4">
</video>

**Links**
- [🐙 GitHub Repository](//github.com/prnthp/UnityPhysXPlugin/tree/android)

---

## Copy-Pasta for exporting high quality MATLAB figures
I always want to export the highest quality plots possible for my publications. I needed some easily copy-pasta'd code to export high resolution plots.

This will produce nice vector figures and rasters at a nice crispy 300 DPI

Add this to the top of your script
```matlab
fontname = 'Arial'; % or your favorite font, IEEE prefers Arial in figures. Helvetica is also sexy.
set(0,'DefaultAxesFontName',fontname,'DefaultTextFontName',fontname);
set(0,'DefaultAxesFontSize',8);
set(0,'DefaultLineLineWidth',1.2);
colors = get(0, 'DefaultAxesColorOrder');
```

When creating a new figure window
```matlab
fignum = 1;
fig = figure(fignum); clf; hold on; grid on; box on;
fig.Renderer = 'Painters'; % this ensures that your figure will be vector/ps
```

When you are ready to save
```matlab
fig.PaperUnits = 'inches';
fig.PaperPosition = [0 0 6 4]; % adjust this to the aspect ratio you want in your publication
figpath = strcat('figure_',num2str(fignum));
print(figpath,'-dpng','-r300') % or change this to 600 (dpi) for crispier figs
print(figpath,'-depsc','-r300') % or change this to 600 (dpi) for crispier figs
```

*Optional: Use ghostscript-based [eps2pdf](//www.mathworks.com/matlabcentral/fileexchange/5782-eps2pdf) MATLAB function to generate pdf*
```matlab
eps2pdf(strcat(figpath,'.eps'),'/usr/local/bin/gs') % second parameter is path to ghostscript exec
```

For best results, use the .pdf in LaTeX!

**Links**
- [🍢 GitHub Gist](//gist.github.com/prnthp/b7e4c6d0a25e51d93bb95dbbb34241c1)

---

## OpenSim STL export
So I wanted to 3D print some hand bones and pose them within SolidWorks with accurate kinematics. The best models at the time were available as OpenSim models. OpenSim uses this ancient 3D model format that isn't so friendly.
Luckily, OpenSim has a python 2.7 API. So I wrote a script to extract those models. Yay bones!

![Converted bones](//github.com/prnthp/opensim-stl-export/raw/master/osim2stl.jpg)

**Links**
- [🐙 GitHub Repository](//github.com/prnthp/opensim-stl-export)

---

## AWS S3 asynchronous automatic upload
Quick and dirty Unity singleton to queue up files for AWS S3 upload. Probably not the best design for security. But it should be ideal for small labs running user studies.

**Links**
- [🍢 GitHub Gist](//gist.github.com/prnthp/20423d8c2ade8730849766b81ee16552)

---

## 3D-printed Vive Tracker hand/wrist mount
A blatant rip-off of a famous sports camera hand/body mount. Just add velcro straps!

![Vive tracker mounted](//camo.githubusercontent.com/b870f88858af9384e00518aaeef4f82455b34a8d19cf3b3e3b4f1437ce64b787/687474703a2f2f692e696d6775722e636f6d2f5a693869307a612e6a7067)

**Vitamins Required**
- 1/4" - 20 TPI Screw: Any screw shorter than 0.35" should work
- Velcro: Any hook-and-loop long enough to wrap around your hand twice should work

**Links**
- [🖨️ Printables](//www.printables.com/prints/151838-vive-tracker-handwrist-mount)
- [🐙 GitHub Repository (STL file)](//github.com/prnthp/vive-tracker-ghost)