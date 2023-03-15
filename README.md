## Robot Package Template

This is a GitHub template. You can make your own copy by clicking the green "Use this template" button.

It is recommended that you keep the repo/package name the same, but if you do change it, ensure you do a "Find all" using your IDE (or the built-in GitHub IDE by hitting the `.` key) and rename all instances of `my_bot` to whatever your project's name is.

Note that each directory currently has at least one file in it to ensure that git tracks the files (and, consequently, that a fresh clone has direcctories present for CMake to find). These example files can be removed if required (and the directories can be removed if `CMakeLists.txt` is adjusted accordingly).

## Sourcing
`cd ros2_ws/`
`source install/setup.bash`
Stay in ros2_ws directory when launching files from this project.

## URDF Commands
Recommended in order in separate terminal tabs
Robot State Publisher: `ros2 launch billee_bot rsp.launch.py`
Joint State Publisher GUI: `ros2 run joint_state_publisher_gui joint_state_publisher_gui`
RViz (from ~/ros2_ws): `rviz2 -d src/billee_bot/config/view_bot.rviz`
