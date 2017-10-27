---
title: Anomalies in the Rift
---
Here I describe some issues with the Oculus Rift hardware when used for motion tracking.

**Touch controllers turn off or go into standby when not interacted with.**

We use the controller to track the orientation of an object that will be stationary (untouched) most of the time over a long duration. The Touch controller will go to sleep or turn off after ~1 minute of inactivity, we have to manually depress a button on the controller to wake it up again. Taping a button down does not work.

*Current solution* Manually depressing buttons once in a while or before starting sessions that require moving the controller

**Calibrated home (origin) of coordinate system changes over each session.**

Our calibration procedure involves calibrating the coordinate frame of a real world robot to the Rift’s coordinate system. However, the Rift’s coordinate frame changes every once in a while - sometimes after temporarily losing tracking and sometimes after the controllers go into standby. This shouldn't happen because ground-truth should be achievable by the cameras and the only (precalibrated) unknown is the floor "height".

*Current solution* Run our calibration between sessions and base all data on real world robot’s coordinate frame.
