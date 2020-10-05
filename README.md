# Project-6-Robot-Arm
6. Robot Arm Simulation


https://www.kuka.com/-/media/kuka-downloads/imported/9cb8e311bfd744b4b0eab25ca883f6d3/kuka_pb_schwere_tl_en.pdf

roslaunch urdf_tutorial display.launch model:='$(find hurba_robot_arm)/urdf/robot_arm.urdf'
rostopic pub robot_arm/arm_controller/command trajectory_msgs/JointTrajectory '{joint_names:["First_joint","Third_joint","Fourth_joint","Fifth_joint","Sixth_joint","Gripper_Base_joint"],points:[{positions:[0.0,-0.2,0.3,0.0,0.3,0.0],time_from_start:[1,0]}]}'

rosrun rqt_joint_trajectory_controller rqt_joint_trajectory_controller

PID tuning:
rosrun rqt_reconfigure rqt_reconfigure
