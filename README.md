RPLIDAR ROS package
=====================================================================

ROS node and test application for RPLIDAR

Visit following Website for more details about RPLIDAR:

rplidar roswiki: http://wiki.ros.org/rplidar

rplidar HomePage:   http://www.slamtec.com/en/Lidar

rplidar SDK: https://github.com/Slamtec/rplidar_sdk

rplidar Tutorial:  https://github.com/robopeak/rplidar_ros/wiki

How to build rplidar ros package
=====================================================================
    1) Clone this project to your catkin's workspace src folder
    2) Running catkin_make to build rplidarNode and rplidarNodeClient

How to run rplidar ros package
=====================================================================
There're two ways to run rplidar ros package

I. Run rplidar node and view in the rviz
------------------------------------------------------------
roslaunch rplidar_ros view_rplidar.launch (for RPLIDAR A1/A2)

or
roslaunch rplidar_ros view_rplidar_a3.launch (for RPLIDAR A3)


You should see rplidar's scan result in the rviz.

II. Run rplidar node and view using test application
------------------------------------------------------------
roslaunch rplidar_ros rplidar.launch (for RPLIDAR A1/A2)

or

roslaunch rplidar_ros rplidar_a3.launch (for RPLIDAR A3)

rosrun rplidar_ros rplidarNodeClient

You should see rplidar's scan result in the console

Notice: the different is serial_baudrate between A1/A2 and A3



## Install
Use the following commands to download and compile the package.

```
cd ~/catkin_ws/src
git clone https://github.com/asimfathekhani/RP_LIDAR
cd ..
catkin_make

## How to run rplidar ros package
=====================================================================
Check the authority of rplidar's serial-port :

ls -l /dev |grep ttyUSB

Add the authority of write: (such as /dev/ttyUSB0)

sudo chmod 666 /dev/ttyUSB0

There're two ways to run rplidar ros package
I. Run rplidar node and view in the rviz

roslaunch rplidar_ros view_rplidar.launch

You should see rplidar's scan result in the rviz.
