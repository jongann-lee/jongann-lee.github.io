---
title: Unicycle Control using Disturbance Observer
summary: Augmented an existing PD controller for a unicycle by adding a disturbance observer inner loop, improving the performance by reducing the overshoot. Implemented and tested the controller in Matlab and Simulink, confirming the performance improvement.
tags:
  - Disturbance Observer 
  - Non-Linear Control
  - Matlab
  - Simulink
date: '2023-12-01'

# Optional external URL for project (replaces project detail page).
external_link: ''

image: 
  caption: Diagram showing the mission of the 2023 Korea Robot Aircraft Competition
  focal_point: ''

url_code: https://github.com/jongann-lee/DOB-for-Unicycle
url_pdf: DOB_Unicycle.pdf
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---

This was a project done as part of the advanced control methods class, where the goal was to freely implement a controller that was taught during class. One of the control methods taught was the disturbance observer or DOB. DOB makes the inner loop dynamics behave like the nominal plant, eliminating the effects of model uncertainty. It also has an added bonus of disturbance rejection making it a very versatile controller. This project implemented a DOB inner loop to a unicycle, which had previously been controlled using a PD controller. The PD controller was designed using the linearized plant dynamics. The goal of the DOB was to improve the controller’s performance on the real, non-linear plant dynamics by stabilizing the plant behaviour while under control. A Simulink simulation of the controller confirmed the improvement in performance. While there was an improvement in performance, the overall robustness of the original PD controller meant that the improvement in performance was marginal.
