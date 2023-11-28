# Robot Targets Generator
> Target generation system for autonomous exploration of mobile robots in unknown indoor environments.

This ROS package provides autonomous navigation and mapping of mobile robots in unknown environments. Upon receiving an occupancy grid from the /SLAM node, which performs simultaneous mapping and localization, it transforms the map into an objective function surface and runs optimization algorithms to search for the most interesting points on the map for the robots. When the best point is found, it is sent to the robot, and then the robot navigates there.

System tested in simulation using the robotic simulator [V-REP](http://www.coppeliarobotics.com/). The scenes used are available in the ./scenes/ directory. 

It is necessary to install the packages [navigation](http://wiki.ros.org/navigation), [move_base](http://wiki.ros.org/move_base), [youbot_navigation](http://wiki.ros .org/youbot_navigation) and [gmapping](http://wiki.ros.org/gmapping).

![](../header.png)

## How to run

Start ros:

```sh
roscore
```

Enable use_sim_time ( ): 

```sh
rosparam set use_sim_time true
```

Start the necessary nodes of the gmapping, ros navigation and youbot_navigation packages:

```sh
roslaunch target_generator target_generator.launch
```

Start the target generator node:

```sh
rosrun target_generator target_generator
```

Open V-REP and start the simulation.

## How to build

Clone the github project into the src folder of your ros workspace:

```sh
cd (your_ros_ws)/src
git clone https://github.com/yourname/github-link
```

Build (We recommend use [Catkin Command Line Tools](http://mcs.une.edu.au/doc/python-catkin_tools-doc/html/)):

```sh
cd ..
catkin build
```


<!--- ## Meta --->

Distributed under the XYZ license. See `LICENSE` for more information.

[https://github.com/yourname/github-link]()


###### Contributors:

Raphael Gomes – https://github.com/raphaelgoms / raphaelgoms@gmail.com

## Contributing

1. Fork the project (<https://github.com/yourname/yourproject/fork>)
2. Create a _branch_ for your modification (`git checkout -b feature/fooBar`)
3. Do _commit_ (`git commit -am 'Add some fooBar'`)
4. _Push_ (`git push origin feature/fooBar`)
5. Create a new _Pull Request_

