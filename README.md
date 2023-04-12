## Setup
Create a workspace folder (eg. `ros2_ws`)

In the workspace folder create an `src` folder

Clone this repo inside the `src` folder

`cd ..` to go back to the `ros2_ws` directory, and then create your ros package with `colcon build --symlink-install`

## Sourcing
`cd ros2_ws/`

`source install/setup.bash`

`source /opt/ros/foxy/setup.bash`

Stay in ros2_ws directory when launching files from this project.

## URDF Commands
Recommended in order in separate terminal tabs

Robot State Publisher: `ros2 launch billee_bot rsp.launch.py`

Joint State Publisher GUI: `ros2 run joint_state_publisher_gui joint_state_publisher_gui`

RViz (from ~/ros2_ws): `rviz2 -d src/billee_bot/config/view_bot.rviz`

## Full Sim Launch File
RSP with Gazebo world: `ros2 launch billee_bot launch_sim.launch.py world:=./src/billee_bot/worlds/cone_obstacles.world`

Rviz Config: `rviz2 -d src/billee_bot/config/depth_camera.rviz`

Teleop Keyboard Control: `ros2 run teleop_twist_keyboard teleop_twist_keyboard`
