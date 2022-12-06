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

The development of a robotic software system using Model-driven Architecture (MDA) typically involves the following steps:

1. Identify the requirements for the robotics software system and define the overall functionality and features that it will need to provide. This may include the type of robot that the software will be used for, the tasks that the robot will need to perform, and the operating environment in which the robot will be deployed.
2. Create a high-level model of the robotics software system using a modeling language, such as the Unified Modeling Language (UML) or the Entity-Relationship (ER) model. This model should capture the main components of the system and the relationships between them. For example, the model may include classes for representing the robot, its sensors and actuators, and the algorithms and control logic that govern its behavior.
3. Define the data model for the robotics software system, including the structure and types of data that it will need to manipulate. This model can be created using a specialized modeling language, such as the Eclipse Modeling Framework (EMF) or the Object Constraint Language (OCL). The data model may include classes for representing the robot's state, its sensor readings, and the commands that are sent to its actuators.
4. Use a model-driven development tool, such as the Eclipse Modeling Framework (EMF) or the Model Driven Architecture Development Environment (MDA-DE), to generate the code for the robotics software system from the high-level and data models. This generated code will provide the basic structure and functionality of the software, including classes for representing the robot and its components, as well as methods for manipulating the data and controlling the robot.
5. Implement any custom code or functionality that is not covered by the generated code. This can include the core algorithms and control logic for the robotics software system, as well as user interfaces and other user-facing features.
6. Test and validate the robotics software system to ensure that it meets the requirements and functions as expected. This may involve simulating the robot's environment and tasks, as well as testing the software on a physical robot.
7. Deploy the robotics software system and provide ongoing maintenance and support. This may involve integrating the software with other systems and tools, as well as providing updates and fixes as needed.

For the requirement specification step, we will:

1. Identify the stakeholders for the software system, including the development team, the customer, and any other interested parties.
2. Define the scope and objectives of the software system, including what it should do and what it should not do.
3. Identify the functional and non-functional requirements for the software system, including user needs and constraints.
4. Analyze the requirements to ensure that they are clear, complete, consistent, and feasible.
5. Prioritize the requirements based on their importance and value to the stakeholders.
6. Document the requirements in a Software Requirement Specification (SRS) document, using a clear and consistent format.
7. Review and validate the SRS with the stakeholders, to ensure that it accurately reflects their needs and expectations.
8. Update and maintain the SRS as needed, to reflect any changes or updates to the requirements or constraints of the software system.

After the Requirement Specification, we will then march toward the domain model construction. The steps will be:



# Changelogs

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}

