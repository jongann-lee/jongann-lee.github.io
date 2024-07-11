---
title: Reinforcement Learning based Tuner for the Geometric Tracking Attitude Controller
summary: A reinforcement learning algorithm designed to tune the attitude controller gains for the geometric tracking controller for the quadrotor.
tags:
  - Reinforcement Learning, Quadrotor, Geometric Tracking Controller
date: '2024-06-05'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Controller diagram of the RL tuner
  focal_point: ''

url_code: https://github.com/jongann-lee/RL-Tuner-Geo-Quad-Controller
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

PID controllers are widely used across many applications including quadrotors. A variant of the PD controller is the geometric tracking controller, which utilizes the rotation matrix and the non-linear quadrotor dynamics. However, PID controllers require gain tuning, and their fixed gains render them incapable of responding to changes in the system in real-time. We propose a reinforcement learning based tuner for the attitude controller gains, which updates the gain in real time based on the history of the vehicle attitude error. The trained RL tuner is shown to be capable of stabilizing a vehicle with an unstable initial controller gain.
