---
layout: page
title: Reinforcement learning for attitude-controller tuning
description: A reinforcement learning algorithm designed to tune the attitude controller gains for the geometric tracking controller
  for the quadrotor.
permalink: /project/rl_tuner/
img: assets/img/projects/rl_tuner.png
importance: 7
category: research
date: "2024-06-05"
tags:
  - Reinforcement Learning
  - Quadrotor
  - Geometric Tracking Controller
---

{% include figure.liquid path="assets/img/projects/rl_tuner.png" title="Controller diagram of the RL tuner" %}

_Controller diagram of the RL tuner_

A reinforcement learning algorithm designed to tune the attitude controller gains for the geometric tracking controller for the quadrotor.

[Project report]({{ "/uploads/RL_tuner.pdf" | relative_url }}) · [Code](https://github.com/jongann-lee/RL-Tuner-Geo-Quad-Controller)

PID controllers are widely used across many applications including quadrotors. A variant of the PD controller is the geometric tracking controller, which utilizes the rotation matrix and the non-linear quadrotor dynamics. However, PID controllers require gain tuning, and their fixed gains render them incapable of responding to changes in the system in real-time. We propose a reinforcement learning based tuner for the attitude controller gains, which updates the gain in real time based on the history of the vehicle attitude error. The trained RL tuner is shown to be capable of stabilizing a vehicle with an unstable initial controller gain.

## Bachelor's thesis

This work was my bachelor's thesis at the Lab for Autonomous Robotics Research, Seoul National University, under Prof. H. Jin Kim (September 2023–June 2024).

I used the TD3 reinforcement learning algorithm to tune the geometric tracking attitude controller. A custom state, action, and reward architecture supported stable training while making the tuner's performance independent of the vehicle's physical parameters. Training used a PyBullet quadrotor simulation wrapped in a Gym environment.
