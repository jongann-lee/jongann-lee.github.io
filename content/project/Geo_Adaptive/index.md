---
title: Adaptive Quadrotor Controller
summary: Created an adaptive quadrotor controller by using the geodesic distance of the manifold of physically consistent inertial parameters. The adaptive law was implemented to the geometric tracking controller to create the adaptive quadrotor controller.
tags:
  - Quadrotor
  - Adaptive Control
  - Geometric Tracking Controller
date: '2023-10-01'

# Optional external URL for project (replaces project detail page).
external_link: ''

image: 
  caption: A visual representation of a geodesic
  focal_point: ''

url_code: ''
url_pdf: Geo_Adaptive.pdf
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---

Adaptive control laws allow for stable control of the agent even when the system parameters vary over time. Therefore, adaptive control laws are useful to quadrotors, whose system parameters such as mass and moment of inertia are subject to uncertain measurements and variations over time.

Most adaptive control laws use a simple Euclidian distance between the real and estimated inertial parameters. This however, poses issues as the manifold of physically consistent inertial parameters is not a simple Euclidian space. Thus, the Euclidian distance is an inaccurate distance metric and could potentially assign physically inconsistent values to the estiamted inertial parameters.

We propose using the geodesic distance on the manifold of physically consistent inertial parameters. This is a more accurate distance metric and ensures that the estimated inertial parameters are physically consistent. 

The adaptive control scheme is then combined with the geometric tracking controller for the quadrotor, a trajectory tracking controller that is proven to be stable even with near inverted attitude. The adaptive quadrotor controller was simulated in Matlab where the improvement in performance was confirmed.
