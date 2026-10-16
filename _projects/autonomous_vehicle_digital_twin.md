---
layout: page
title: Autonomous vehicle digital twin
description: A photorealistic Highbay digital twin combining Gaussian splatting, Gazebo vehicle dynamics, and obstacle-aware navigation.
permalink: /project/autonomous_vehicle_digital_twin/
img: assets/img/projects/CS588.png
importance: 4
category: research
start_date: 2026-01
end_date: 2026-05
tags:
  - SLAM
  - Gaussian Splatting
  - LiDAR
---

**CS588 group project · January–May 2026**

[Project report (PDF)]({{ "/assets/pdf/CS588_project.pdf" | relative_url }})

{% include figure.liquid
   path="assets/img/projects/CS588.png"
   alt="Integrated Highbay simulator showing a Gaussian-splat front-camera view and overhead map on the left, with the GEM e4 vehicle in Gazebo on the right."
   caption="The integrated simulator: a photorealistic Gaussian-splat camera stream alongside Gazebo vehicle dynamics."
%}

## Project overview

Our team built a photorealistic digital twin of the Highbay driving environment to test autonomous navigation before deployment on a physical GEM e4 vehicle. The system combines **3D Gaussian Splatting (3DGS)** for realistic camera images with **Gazebo** for vehicle dynamics and state updates. This gives perception algorithms a camera stream reconstructed from the real site while retaining the existing simulation and control pipeline.

The complete system connects **RGB-D obstacle detection**, a **Frenet-frame replanner**, and a **Stanley tracking controller**. YOLO detections and depth measurements provide obstacle locations; the replanner generates feasible detours, and the controller follows the selected trajectory. Separately reconstructed objects can be inserted into the digital twin to create repeatable obstacle-avoidance scenarios.

The perception–planning–control loop was evaluated in the 3DGS-integrated simulator. Planning and tracking were also tested on the real GEM e4 using a known obstacle pose; integrating live obstacle detections into the hardware loop remained future work.

## My contribution

I developed the **metric reconstruction and 3DGS training pipeline** that produced the Highbay scene:

- **LiDAR mapping:** Registered 651 GEM e4 LiDAR sweeps using KISS-ICP to reconstruct the environment from a full-loop recording.
- **Pose optimization:** Fused relative LiDAR odometry with GNSS positions in a GTSAM SE(2) pose graph, improving the consistency of the combined map.
- **Metric initialization:** Used the fused LiDAR map to initialize the Gaussian reconstruction and aligned COLMAP camera poses to the map’s metric coordinate frame. The scene initialization combined approximately two million LiDAR points with COLMAP structure and synthetic sky points for regions beyond LiDAR coverage.
- **3DGS training:** Trained the Highbay Gaussian-splat model for 30,000 iterations, using anti-aliasing and a shorter densification schedule to produce the photorealistic scene representation.

My teammates then integrated the trained scene into Gazebo and ROS, added compositional objects, and implemented the obstacle-detection, planning, and tracking modules.

**Team:** Minkyung Kim, Minhyuk Jang, Dong-Hwan Jang, and Jongann Lee.
