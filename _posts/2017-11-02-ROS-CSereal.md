---
title: "ROS & ROS CSereal"
---
A major part of the Bishop's Hand project is a robust logging backend in for recording kinematic data from Unity. We chose ROS as our backend.

### ROS? ###
[ROS](//ros.org) "The Robot Operating System (ROS) is a set of software libraries and tools that help you build robot applications. From drivers to state-of-the-art algorithms, and with powerful developer tools, ROS has what you need for your next robotics project. And it's all open source."

### Why ROS? ###
What sold me (or [who](//rombokas.com/eric) sold me) was the communication framework provided by ROS. ROS is mainly driven by a message passing system: any number of *nodes* can pass messages to any number of other nodes through *roscore*. A node can publish to a *topic* and not care whether anyone is listening or not. Likewise, another node can subscribe and listen to your topic at their own leisure. A node can be anything: a sensor, a motor driver, a user interface, a simulation or in this case: Unity.

### rosserial ###
A caveat: ROS almost exclusively only runs on Linux. The release cycles are even tied to Canonical's Ubuntu release cycle (with LTS releases too!). So how do we set up a node on Windows? The answer is [rosserial](//github.com/ros-drivers/rosserial): a collection of drivers for running ros-like nodes on embedded systems such as the Arduino and Teensy. Forget about robots, we now have middleware for easily connecting multiple pieces of hardware and software.

![ROSCSereal](/images/roscsereal.png)*ROSCSereal Logo*

### ROS CSereal ###
[ROS CSereal](//github.com/prnthp/ros-csereal-plugin) is a plugin I developed for Unity with rosserial-windows. It provides a simple plug-n-play interface for sending poses (transforms) of gameObjects and other data (vectors, strings, floats) and receiving the same sort of data.

*Insert cool video demonstrating inverse pendulum controlled through ROS with physics in Unity here*

*Also ROS2 is coming very soon and it supports windows and this will all be quite moot.*
