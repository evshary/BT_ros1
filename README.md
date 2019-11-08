# Before usage
1. You need to install ros1 and Gazebo first.

```
sudo apt install ros-melodic-desktop-full ros-melodic-turtlebot3 ros-melodic-turtlebot3-gazebo
```

2. Run Gazebo Emulator

```
export TURTLEBOT3_MODEL=waffle_pi
roslaunch turtlebot3_gazebo turtlebot3_world.launch
```

3. Open another terminal and run teleop

```
export TURTLEBOT3_MODEL=waffle_pi
roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```

4. Open another terminal and Run SLAM

```
export TURTLEBOT3_MODEL=waffle_pi
roslaunch turtlebot3_slam turtlebot3_slam.launch
```

5. Open another terminal and Save map

```
rosrun map_server map_saver -f ~/sim_map
```

6. Open another terminal and Run navigation

```
export TURTLEBOT3_MODEL=waffle_pi
roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/sim_map.yaml
```

# Usage
1. Download and build the code

```
cd BT_ros1
catkin_make
```

2. You can modify `bt_test.xml` for behavior tree.
3. Start to run

```
source devel/local_setup.bash
rosrun bt_sample node _file:=absolute_path/bt_test.xml
```
