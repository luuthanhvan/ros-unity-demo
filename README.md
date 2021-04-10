# ROS and Uniy connection demo

# Installation ROS
- Ubuntu 16.04: install ROS Kinetic - full desktop version at http://wiki.ros.org/kinetic/Installation/Ubuntu
- Ubuntu 18.04: install ROS Melodic - full desktop version at http://wiki.ros.org/melodic/Installation/Ubuntu
- Rosbridge: sudo apt-get install ros-melodic-rosbridge-server

# Installation Unity
https://www.youtube.com/watch?v=BB4Hvjxhq08&ab_channel=LinuxH2O

# Downloading RosSharp
https://github.com/siemens/ros-sharp

# Create ROS Workspace (Practice)

            mkdir ros_unity
            cd ros_unity
            mkdir src
            cd src
            catkin_init_workspace
            catkin_create_pkg test std_msgs geometry_msgs roscpp rospy
            cd ..
            catkin_make
            echo "source ${PWD}/devel/setup.bash" >> ~/.bashrc
            
# Running ROS
- Open the terminal 1:

            roslaunch rosbridge_server rosbridge_websocket.launch

- Open the terminal 2:

            cd ros_unity
            rosrun test talker.py
    
# Running Unity
https://www.youtube.com/watch?v=lVa_bb0UFMs&ab_channel=bryansgue

* Note: Ros bridge server url is ws://localhost:9090 and topic name is "/chatter_"