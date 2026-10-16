---
layout: page
title: Unicycle Control using Disturbance Observer
description: Augmented an existing PD controller for a unicycle by adding a disturbance observer inner loop, improving the performance
  by reducing the overshoot. Implemented and tested the controller in Matlab and Simulink, confirming the performance improvement.
permalink: /project/dob_unicycle/
img: assets/img/projects/dob_unicycle.png
importance: 9
category: research
date: "2023-12-01"
tags:
  - Disturbance Observer
  - Non-Linear Control
  - Matlab
  - Simulink
---

{% include figure.liquid path="assets/img/projects/dob_unicycle.png" title="Unicycle model used to create the controller" %}

_Unicycle model used to create the controller_

Augmented an existing PD controller for a unicycle by adding a disturbance observer inner loop, improving the performance by reducing the overshoot. Implemented and tested the controller in Matlab and Simulink, confirming the performance improvement.

[Project report]({{ "/project/dob_unicycle/DOB_Unicycle.pdf" | relative_url }}) · [Code](https://github.com/jongann-lee/DOB-for-Unicycle)

This was a project done as part of the advanced control methods class, where the goal was to freely implement a controller that was taught during class. One of the control methods taught was the disturbance observer or DOB. DOB makes the inner loop dynamics behave like the nominal plant, eliminating the effects of model uncertainty. It also has an added bonus of disturbance rejection making it a very versatile controller. This project implemented a DOB inner loop to a unicycle, which had previously been controlled using a PD controller. The PD controller was designed using the linearized plant dynamics. The goal of the DOB was to improve the controller’s performance on the real, non-linear plant dynamics by stabilizing the plant behaviour while under control. A Simulink simulation of the controller confirmed the improvement in performance. While there was an improvement in performance, the overall robustness of the original PD controller meant that the improvement in performance was marginal.
