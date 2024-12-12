---
title: "Geometric Tracking Controller for a Multirotor UAV with Collective Pitch-Tilting"
authors:
- admin
- Taekyun Kim
- Dongjun Lee
date: "2024-09-19"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2024-09-19"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article"]

# Publication name and optional abbreviated publication name.
publication: ""
publication_short: ""

abstract: This paper introduces a controller for the tracking control of a multirotor UAV with 5 control degrees of freedom (CDoF), which is capable of generating three-dimensional torque about its center of mass and thrusts in both the upward and forward directions of the vehicle. This vehicle design offers several advantages over traditional multirotors, including the ability to exert a frontal force without changing attitude, which is beneficial for aerial manipulation, and the capability to orient the front of the vehicle in any direction, making it ideal for surveillance applications. We show that the 5-CDoF multirotor system dynamics is differentially flat with its center of mass position, yaw angle and pitch angle being the flat outputs. To track trajectories of the flat outputs, we propose a geometric tracking controller based on the nonlinear SE(3) dynamics of the vehicle, which makes the controller free of linearization errors and singularities. The controller exhibits desirable closed-loop properties, with the ability to recover from a near-inverted attitude, which is proven using Lyapunov analysis. A numerical simulation of the controller showcases the stability and efficacy of the proposed controller.

# Summary. An optional shortened abstract.
summary: ""

tags:
 - 
featured: false

links:
#- name: Custom Link
#  url: http://example.org
url_pdf: http://arxiv.org/pdf/1512.04133v1
#url_code: 'https://github.com/HugoBlox/hugo-blox-builder'
#url_dataset: '#'
#url_poster: '#'
#url_project: ''
#url_slides: ''
#url_source: '#'
#url_video: '#'

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: '3D diagram of an example 5-CDoF multirotorwith rotors capable of tilting synchronously'
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
- []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---

<!-- {{% callout note %}}
Create your slides in Markdown - click the *Slides* button to check out the example.
{{% /callout %}} -->

<!-- Add the publication's **full text** or **supplementary notes** here. You can use rich formatting such as including [code, math, and images](https://docs.hugoblox.com/content/writing-markdown-latex/). -->
