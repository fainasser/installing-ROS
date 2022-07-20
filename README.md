# installing-ROS
The below commands are for installing ROS kinetic kame on Ubuntu 16.04
1-setup sources.list (sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list')

2-adding key(sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654)

3-update package list(sudo apt-get update)

4-installing ROS kinetic full desktop version (sudo apt-get install ros-kinetic-desktop-full)

5-initilize ROS dependencies (sudo rosdep init)
(rosdep update)

6- setting up ROS environment (echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc)
(source ~/.bashrc)

7-installing python packages for ROS(sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential)

(sudo apt install python-rosdep)

8-other important ROS package 

(sudo apt-get install ros-kinetic-moveit)

(sudo apt-get install ros-kinetic-joint-state-publisher ros-kinetic-joint-state-publisher-gui)

(sudo apt-get install ros-kinetic-gazebo-ros-control joint-state-publisher)

(sudo apt-get install ros-kinetic-ros-controllers ros-kinetic-ros-control)

9-creating catkin workspace 
(sudo apt-get install ros-noetic-catkin)

(mkdir -p ~/catkin_ws/src)

(cd ~/catkin_ws/)

(catkin_make)

10-package for robot arm (git clone https://github.com/smart-methods/arduino_robot_arm.git)
11-other important ROS packages 

(rosdep install --from-paths src --ignore-src -r –y)

sudo apt-get install ros-kinetic-moveit

(sudo apt-get install ros-kinetic-joint-state-publisher ros-kinetic-joint-state-publisher-gui)

(sudo apt-get install ros-kinetic-gazebo-ros-control joint-state-publisher)

(sudo apt-get install ros-kinetic-ros-controllers ros-kinetic-ros-control)

12-put the source of setup.bash in bashrc file 

(sudo nano ~/.bashrc)

at the end of the (bashrc) file add the follwing line
(source /home/fay/catkin_ws/devel/setup.bash)
then 
ctrl + o

(source ~/.bashrc)

13- the end 
(roslaunch robot_arm_pkg check_motors.launch)
 
