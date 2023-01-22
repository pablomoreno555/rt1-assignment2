Research Track I - Assignment 2  
Pablo Moreno Moreno - S5646698 
----------------------

This repository contains the ROS package developed for the second assignment: *my_assignment_2*.


## Required applications/packages
- You need to have the package *assignment_2_2022* within your workspace.
- You need to have the *konsole* application installed in your machine, since it is used to display the different terminals.


## Building and running the code
Once the previous pre-requisites are met, you can build the package by executing the command `catkin_make` within the root directory of your workspace.

On the other hand, a launch file has been created in order to start the whole simulation. It's name is *my_assignment_2.launch*, so you can run the simulation by executing the following command:
```console
roslaunch my_assignment_2 my_assignment_2.launch
```

The following windows will pop up:
- **Gazebo**, where we can see the simulation of the robot within the environment.
- **RViz**, where we can also visualize the robot.
- **node_a**: the terminal associated to the action client (*node_a*).
- **node_b**: the terminal associated to the service node (*node_b*).
- **node_c**: the terminal associated to *node_c*.


## Content of the Repository
The package "my_assignment_2", is organized as follows:
- The `scripts` folder, which contains the Python scripts corresponding to the three nodes: *node_a.py*, *node_b.py* and *node_c.py*.
- The `msg` folder, which contains the definition of the custom message *PosVel*.
- The `srv` folder, which contains the definition of the custom service "GoalsResults".
- The `launch` folder, that contains the launch file (*my_assignment_2.launch*).
- The *CMakeLists.txt* file.
- The package manifest (*package.xml*).


## Description of the nodes
- **node_a**. It implements an action client for the action service *reaching_goal*, implemented within the package *assignment_2_2022*. Through a small User Interface, it allows the user to set a new target (x, y) or to cancel the current target. It also publishes the robot position and velocity using the custom message *PosVel*, composed by the fields *x*, *y*, *vel_x* and vel_y*.
