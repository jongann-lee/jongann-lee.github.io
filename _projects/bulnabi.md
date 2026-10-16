---
layout: page
title: Autonomous Quadrotor System for Payload Delivery
description: Created an autonomous quadrotor capable of detecting and avoiding obstacles, automatically landing on a designated landing
  area, detecting a pre‑determined delivery point and delivering a payload to it.
permalink: /project/bulnabi/
img: assets/img/projects/bulnabi.png
importance: 11
category: research
tags:
  - Quadrotor
  - PX4-Autopilot
  - ROS2
start_date: 2022-07
end_date: 2023-07
---

{% include figure.liquid path="assets/img/projects/bulnabi.png" title="Diagram showing the mission of the 2023 Korea Robot Aircraft Competition" %}

_Diagram showing the mission of the 2023 Korea Robot Aircraft Competition_

Created an autonomous quadrotor capable of detecting and avoiding obstacles, automatically landing on a designated landing area, detecting a pre‑determined delivery point and delivering a payload to it.

[Project report]({{ "/project/bulnabi/bulnabi.pdf" | relative_url }})

During my undergraduate studies, I was a member, and later president, of the Seoul National University drone club Bulnabi. Over the years, I have participated in many projects within the club, but the 2023 Korea Robot Aircraft Competition is the one that I worked on the hardest, and therefore I chose to discuss it here.

The objective of the competition could be split into several parts. The aircraft had to take off and fly in a stable manner automatically without human input. Next, it had to navigate between two ladders and fly inbetween them. After doing this, the vehicle had to locate the delivery point located on the third floor balcony, which had been marked with a cross. A pizza box would then be delivered and the drone would return to a designated position and land automatically.

All of the above mentioned tasks had to be performed automatically without human intervention. For this, we decided to utilize two computers: a Pixhawk flight computer(FC) running PX4, and a NVIDIA Jetson Xavier companion computer(CC) running ROS2. The CC would take sensor data, such as camera images, and use it to determine the action needed to be taken (go forward, release cargo etc.). The FC would then receive these actions and calculate the appropriate commands to be given to the motors in order to follow the action and maintain stability at the same time.

I implemented a Fast DDS communication system between the PX4-Autopilot flight computer and the ROS2 companion computer, allowing flight data and commands to pass between the two systems.

I also worked on the trajectory generation module, which was necessary to continuously provide a smooth trajectory for the vehicle to follow. The module utilized a 4-point Bezier curve, which was defined using the current position, current velocity, desired position, and desired velocity. The design allowed the vehicle to smoothly enter from the current state and exit to the desired state in a continuous manner as well.

## Club leadership

I was a member of SNU Drone Club Bulnabi from March 2019 to June 2024, serving as Vice President from January 2022 to July 2023 and President from August 2023 to June 2024.

As President, I grew the club from 10 to 40 members, organized weekly seminars and winter-break projects, and assembled a 25-member team that went on to win the 2024 Korea Robot Aircraft Competition.
