# Reference
[en]

Programming Robots with ROS: A Practical Introduction to the Robot Operating

Morgan Quigley, Brian Gerkey, William D. Smart

[jp]

プログラミングROS --Pythonによるロボットアプリケーション開発

Morgan Quigley, Brian Gerkey, William D. Smart 著,河田 卓志 監訳,松田 晃一,福地 正樹,由谷 哲夫 訳

# How to
## Check URDF structure
```
check_urdf cougarbot.urdf
```

## Watch URDF in rviz
```
roslaunch urdf_tutorial display.launch model:=cougarbot.urdf
```

## Launch Gazebo simulator
```
roslaunch cougarbot cougarbot.launch
```

## Send joint angles
```
rostopic pub /arm_controller/command trajectory_msgs/JointTrajectory '{joint_names: ["hip", "shoulder", "elbow", "wrist"], points: [{positions: [0.1, -0.5, 0.5, 0.75], time_from_start: [1, 0]}]}' -1
```
the elements of time_fron_start must be int type 

## Watch joint states
```
 rostopic echo /joint_states
```

## plot joint states in rqt_plot
```
rqt_plot '/joint_states/position[0]' '/joint_states/position[1]' '/joint_states/position[2]' '/joint_states/position[3]'
```