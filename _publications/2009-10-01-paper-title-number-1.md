---
title: "Change log Dec 04, 2022"
collection: publications
permalink: /publication/2009-10-01-paper-title-number-1
excerpt: 'This log is the first log about the basic information for the fundamental simulator . The second is left for future work.'
date: 2022-12-05
venue: 'Fundamental log'
paperurl: 'log1205.pdf'
citation: 'change log dec 05, 2022'
---

This log is the first log about the basic information for the fundamental simulator . The second is left for future work.

## Why Choose Fundamental Simulator?

**Unmanned aerial vehicle (UAV) navigation is gaining more and more interest in both research and business. Real UAV experiments could be expensive and time-consuming. As an alternative, the validation and testing of UAV navigational algorithms using simulation is essential in the early phases of development when it is difficult to get high-precision and high-fidelity experiment data.**  They have applications like search and rescue, delivery of goods, security and surveillance, and civil infrastructure inspection [1]. Navigation, including perception, localization, motion planning, and motion control, is the meta-capability for UAVs in successfully performing tasks. The Global Navigation Satellite System (GNSS) is the most common way of navigation. However, the signal of GNSS would be unavailable for indoor environments and vulnerable under forest canopies [2] and in urban or natural canyons.[3] Therefore, the application of UAVs in environments devoid of GNSS service has motivated research into GNSS- independent navigation solutions[4,5]. Nevertheless, although testing and verifying these solutions in realistic scenarios can be more faithful to the real world, it could also be expensive and even dangerous due to the complex hardware setup, safety precautions, and battery constraints [6]. *Simulators*, on the other hand, allow for the safe and economic development and testing of algorithms without the time-consuming and costly process of dealing with real-world hardware. An excellent simulation environment frequently possesses the following characteristics:

1. Conforms to physical principles, i.e., it can faithfully represent the dynamics in the real world;

2. Is fast in simulating, i.e., a large number of simulation data that can be used to verify the algorithm can be obtained quickly within limited resources and time;

3. Mirrors the real-life environment, i.e., maintains as much consistency with the actual scene as possible.

In practice, however, meeting all of the aforementioned attributes at the same time might be challenging, if not impossible. This is due to the fact that increasing scene features and physical characteristics increase the amount of calculation, lowering simulation speed, and implying that these aspects are clashing to some extent. [7]

Despite these constraints, current robotic communities have provided a plethora of very practical and useful simulation settings. Among these simulation environments, many for universal purposes emphasize attribute 1, which means focusing mostly on UAV dynamics with insufficient attention to environmental perception. Environment-integrated simulators, such as the Gazebo-based RotorS [8, 9], which is intended for tackling higher-level problems such as path planning and SLAM, focus more on environment perception so that visual navigational algorithms such as SLAM can be better validated. Furthermore, for better integration and deployment of perception or planning components, most academic developers have focused heavily on ROS[10]. However, because ROS is designed to use a master-centered node communication architecture, it is less robust and may result in the failure of the entire system if the master node crashes; additionally, ROS lacks adaptation for different operating systems, and ROS is not suitable for multi- UAV emulation due to memory management and network security limitations[11]. Furthermore, because the development and maintenance of the most recent ROS Noetic will end in 2025[12] and will be replaced by ROS2, it is worthwhile to design and implement a simulation platform based on ROS2, which can meet the requirement for long-term simulation iteration while making the simulation platform more stable and improving the performance and robustness of the entire system operation process[13]. We will present a simulation environment based on ROS2, PX4[14], and Gazebo in this concept. Once created, end-users can easily convert the customized solution for visual navigation to real-world hardware. Software engineering ideas will also be implemented to improve quality and procedure management. We will present a simulation environment based on ROS2, PX4[14], and Gazebo in this concept. Once accomplished, end-users can easily convert the customized solution for visual navigation to real-world hardware. Software engineering ideas will also be implemented to improve quality and procedure management.
