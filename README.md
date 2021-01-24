# lidar_simulator

- Gazebo simulation models for different LiDAR sensors (Velodyne, Ouster, ...). This is a customized version of an open-source repo originally developed by [Dataspeed](https://bitbucket.org/DataspeedInc/velodyne_simulator).
- The lidar model could be selected using following names: VLP-16, HDL-32E,O1-64

### Build
tested on Ubuntu 18.04 ROS Melodic
```
cd ~/catkin_ws/src
git clone https://github.com/wuhan-geodesy/lidar_simulator.git
cd ../
catkin build

```

### Test

```
source ~/catkin_ws/devel/setup.bash
roslaunch lidar_description example.launch
```
If you have downloaded world models from [here](https://github.com/osrf/gazebo_models),
and put them to either .gazebo/models or /user/share/gazebo-9/models.
Then you may use an alternative world model.
```
roslaunch lidar_description example.launch world_name:=/usr/share/gazebo-9/worlds/willowgarage.world
```

### Todo:
- Add O1-16, O0-128.

### Known issues:
- Option with GPU might not work: check this [note](https://github.com/tungdanganh/velodyne_simulator/blob/master/gazebo_upgrade.md)
