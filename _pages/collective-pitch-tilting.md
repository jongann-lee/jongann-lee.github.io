---
layout: page
title: Geometric Tracking Controller for a Multirotor UAV with Collective Pitch-Tilting
permalink: /publication/multirotor_with_collective_pitch_tilting/
description: Research project in geometric control and aerial robotics.
---

This work is presented as a [research project]({{ "/project/collective_pitch_tilting/" | relative_url }}).

Research at the Interactive and Networked Robotics Laboratory, Seoul National University, with Prof. Dongjun Lee. Collaborators: Taekyun Kim and Dongjun Lee.

{% include figure.liquid path="assets/img/publication_preview/collective-pitch-tilting.png" title="Multirotor with collective pitch-tilting" %}

I derived a geometric trajectory-tracking controller for a multirotor with collective pitch-tilting and established position, yaw, and pitch as differentially flat outputs. Using Lyapunov analysis, I proved almost-global exponential attractiveness of the closed-loop dynamics and demonstrated the controller's performance in MATLAB simulations.

The vehicle can produce thrust in both upward and forward directions, allowing force generation without the attitude changes required by a conventional multirotor.

[Technical manuscript]({{ "/publication/multirotor_with_collective_pitch_tilting/Geometric_Control_of_a_Multirotor_UAV_with_Collective_Pitch_Tilting__IJCAS_.pdf" | relative_url }})
