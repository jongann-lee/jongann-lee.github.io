---
title: Autonomous Quadrotor System for Payload Delivery
summary: created an autonomous quadrotor capable of detecting and avoiding obstacles, automatically landing on a designated landing area, detecting a pre‑determined delivery point and delivering a payload to it.
tags:
  - Quadrotor, PX4-Autopilot, ROS2
date: '2023-08-01'

# Optional external URL for project (replaces project detail page).
external_link: ''

image: 'competition_diagram.png'
  caption: 'Diagram showing the mission of the 2023 Korea Robot Aircraft Competition'
  focal_point: ''

url_code: ''
url_pdf: uploads/RL_tuner.pdf
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ''
---

During my undergraduate studies, I was a member, and later president, of the Seoul National University drone club Bulnabi. Over the years, I have participated in many projects within the club, but the 2023 Korea Robot Aircraft Competition is the one that I worked on the hardest, and therefore I chose to discuss it here.

The objective of the competition could be split into several parts. The aircraft had to take off and fly in a stable manner automatically without human input. Next, it had to navigate between two ladders and fly inbetween them. After doing this, the vehicle had to locate the delivery point located on the third floor balcony, which had been marked with a cross. A pizza box would then be delivered and the drone would return to a designated position and land automatically.

All of the above mentioned tasks had to be performed automatically without human intervention. For this, we decided to utilize two computers: a Pixhawk flight computer(FC) running PX4, and a NVIDIA Jetson Xavier companion computer(CC) running ROS2. The CC would take sensor data, such as camera images, and use it to determine the action needed to be taken (go forward, release cargo etc.). The FC would then receive these actions and calculate the appropriate commands to be given to the motors in order to follow the action and maintain stability at the same time.

This requires a good communications bridge between the FC and the CC. I implmented a communications bridge between the PX4-Autopilot FC software and the ROS2 software on the CC by utilizing the XRCE-DDS prptocol. This protocol was used to  convert ROS2 messages into uORB messages used by PX4, which allowed the FC to send vehicle sensor data to the CC, and for the CC to send kinematic commands to the FC. 

I also worked on the trajectory generation module, which was necessary to continously provide a smoothe trajectory for the vehicle to follow. The module utilized a 4-point Bezier curve, which was defined using the current position, current velocity, desired position, and desired velocity. The design allowed the vehicle to smoothly enter from the current state and exit to the desired state in a continous manner as well.
