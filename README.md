# ROS2 Turtlesim Manipulation Task

## Environment
- VirtualBox running Ubuntu MATE
- ROS2 (e.g., Humble)
- turtlesim package

## Description
This project demonstrates how to launch and control the turtlesim simulator using ROS2 commands. It shows how to open the turtlesim node, control the turtle with keyboard inputs, and inspect active topics, nodes, and services.

## How to Run

Terminal 1: Launch the turtlesim simulator window
This command starts the turtlesim node and opens the graphical window with the turtle.

ros2 run turtlesim turtlesim_node

Terminal 2: Control the turtle using keyboard input
First, source the ROS2 environment so the commands work properly:

source /opt/ros/humble/setup.bash

Then run the teleoperation node that allows you to control the turtle with arrow keys:

ros2 run turtlesim turtle_teleop_key

Terminal 3: List all active topics
This command shows all the communication topics currently active in ROS2:

ros2 topic list

Terminal 4: List all active nodes
This command lists all running ROS2 nodes (programs) in your system:

ros2 node list


Terminal 5: List all active services
This command lists all available ROS2 services you can call:

ros2 service list

What is a Topic in ROS2?
A topic is a communication channel used by ROS2 nodes to exchange messages asynchronously.

Nodes publish messages to topics.

Other nodes subscribe to those topics to receive messages.

In this task:

turtle_teleop_key node publishes velocity commands to the topic /turtle1/cmd_vel.

turtlesim_node node subscribes to /turtle1/cmd_vel and moves the turtle accordingly.

Notes
This setup was tested inside VirtualBox running Ubuntu MATE.
