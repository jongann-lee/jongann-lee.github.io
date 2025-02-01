---
title: PIEJAM(Passive Inversion and Eversion Joint Ankle Mechanism)
summary: PIEJAM is an inversion and eversion ankle joint mechanism that allows the user to perform ankle inversion and eversion while using an ankle exoskeleton.
tags:
  - Compliant Mechanism
  - Hardware
date: '2024-10-11'

# Optional external URL for project (replaces project detail page).
external_link: ''

image: 
  caption: An exploded view of PIEJAM
  focal_point: ''

url_code: ''
url_pdf: PIEJAM_Report.pdf
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---

Inversion and eversion is the rotation of the foot about the axis parallel to the toes. In simpler terms, its the rotation that makes the bottom of your foot face the left or right. This movement is crucial for maintaining balance and traversing uneven terrain. Yet many current ankle exoskeletons do not allow the user to perform inversion and eversion. The goal of this project was to develop an inversion and eversion ankle joint mechanism that would allow augment this capability to an existing ankle exoskeleton(speifically PERL from POLAR lab at Polytechnique Montreal).

The primary feature of this mechanism is the compliant mechanism based joint. Typical revolute joints use bearings and pins to create the rotational degree of freedom, but this increases the complexity and manufacturing and maintaining the joint. PIEJAM uses compliant mechanisms, which are flexible mechanisms that achieve force and motion transmission through elastic body deformation. It has been implemented in the form of a x-shaped cross-axis flexural pivot, which enables the rotational motion and at the same time provides adverse torque feedback like a torsional spring. The overall joint mechanism designs also limits the range of motion, which is important for preventing injuries. 

A test of using PIEJAM with PERL showed that the desired inversion and eversion movement characteristics while not comprimising the requirements for dorsiflexion and plantarflexion actuation. 
