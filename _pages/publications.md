---
layout: archive
title: "Fundamental Simulator"
permalink: /publications/
author_profile: true
---

{% include base_path %}

The Fundamental Simulator is the subsystem to be implemented in the Fundamental System. The draft framework will be shown as follows:

![frameSimulator](../images/arch.png)

As illustrated in the graph above, we design an architecture for the simulation environment. The end-user parts are considered to show the interaction with the simulator in order to better illustrate the workflow of the proposed architecture. The simulator will support both SITL and HITL modes for smooth transitions from simulation to real-world UAV tasks. Depending on the algorithms used, the Gazebo provides world and UAV models, as well as custom-define sensor models. Users can then operate the UAVs with keyboard controllers to perceive the environment and compare the algorithm's estimation with the simulator's ground truth. The navigation modules are divided into separate modules that include localization, planning, and mapping components that the end user can customize for specific usage. Furthermore, because

the simulator runs on ROS2, these modules communicate and coordinate with one another via ROS2 topics. The communication between ROS2 and PX4 will also include PX4-supplied methods. In the early stages of SITL, the perception and planning modules, along with other components, run on the host. The user can begin by using QgroundControl to schedule flights and monitor drone status. The simulator will then instruct the sensors plugin in Gazebo to retrieve data from the environment and send it for navigation tasks such as perception and mapping. The situation in HITL would become more complicated with the introduction of environmental factors such as drone communications, weather, and human interruptions. In HITL mode, the navigation modules run on the UAV's onboard computer, and the Gazebo serves as an intermediary between the PX4 controller and the navigational modules.

The development of the Fundamental Simulator will follow the procedure of Model-driven Architecture (MDA). 

Model-driven Architecture (MDA) is a software development approach that focuses on using models to represent and manipulate the elements of a software system. In the context of robotics, MDA can be used to develop and maintain large-scale robotic software systems, such as those used in autonomous vehicles, drones, and other robotics applications.

MDA has many advantages in the context of robotics, including:

- Improved scalability and modularity: MDA allows large-scale robotic software systems to be divided into smaller, independent modules, which can be developed and maintained separately. This makes it easier to scale the software system as needed, and to add or remove modules without affecting the overall system.
- Increased reusability: MDA allows software modules and components to be easily reused in different contexts and applications. This can reduce the time and effort required to develop new robotic software systems, and can help to ensure that the software is of high quality and reliability.
- Better maintainability: MDA provides a clear and consistent framework for developing and maintaining robotic software systems. This makes it easier to understand the software system and to make changes and improvements as needed.
- Improved interoperability: MDA allows robotic software systems to be integrated and combined with other systems and technologies, which can improve the overall functionality and performance of the system.
- Enhanced flexibility and adaptability: MDA allows robotic software systems to be easily adapted and extended to meet changing requirements and needs, which can improve the overall agility and responsiveness of the system.

Overall, using MDA in the development of large-scale robotic software systems can provide many benefits, including improved scalability, modularity, reusability, maintainability, interoperability, and flexibility.

The development of a software system using Model-driven Architecture (MDA) typically involves the following steps:

1. Identify the software system and its requirements, including functional and non-functional requirements, as well as user needs and constraints.
2. Create a domain model that represents the key concepts and relationships within the software system.
3. Create a conceptual model, also known as a Platform Independent Model (PIM), that describes the high-level structure and functionality of the software system, without considering the specific platform or implementation.
4. Transform the PIM into a logical model, also known as a Platform Specific Model (PSM), that represents the detailed design of the software system, including its components, interfaces, and relationships.
5. Transform the PSM into executable code using a model-to-code transformation tool.
6. Test and validate the software system to ensure that it meets the specified requirements and constraints.
7. Deploy and maintain the software system, including making updates and improvements as needed.

For the requirement specification step, we will:

1. Identify the stakeholders for the software system, including the development team, the customer, and any other interested parties.
2. Define the scope and objectives of the software system, including what it should do and what it should not do.
3. Identify the functional and non-functional requirements for the software system, including user needs and constraints.
4. Analyze the requirements to ensure that they are clear, complete, consistent, and feasible.
5. Prioritize the requirements based on their importance and value to the stakeholders.
6. Document the requirements in a Software Requirement Specification (SRS) document, using a clear and consistent format.
7. Review and validate the SRS with the stakeholders, to ensure that it accurately reflects their needs and expectations.
8. Update and maintain the SRS as needed, to reflect any changes or updates to the requirements or constraints of the software system.

After the Requirement Specification, we 



Here will be the changelog 

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}

