# Reference
[en]

Programming Robots with ROS: A Practical Introduction to the Robot Operating

Morgan Quigley, Brian Gerkey, William D. Smart

[jp]

プログラミングROS --Pythonによるロボットアプリケーション開発

Morgan Quigley, Brian Gerkey, William D. Smart 著,河田 卓志 監訳,松田 晃一,福地 正樹,由谷 哲夫 訳

# How to
Check URDF structure
```
check_urdf urdf/cougarbot.urdf
```

Watch URDF in rviz
```
roslaunch urdf_tutorial display.launch model:=urdf/cougarbot.urdf
```
Launch Gazebo simulator
```
roslaunch cougarbot cougarbot.launch
```