# ca1_2023s

include your report here. 
Please find results for the CLI's below;
$output for running  $ ros2 run turtlesim turtlesim_node

Warning: Ignoring XDG_SESSION_TYPE=wayland on Gnome. Use QT_QPA_PLATFORM=wayland to run on Wayland anyway.
[INFO] [1675461533.135721514] [turtlesim]: Starting turtlesim with node name /turtlesim
[INFO] [1675461533.168092134] [turtlesim]: Spawning turtle [turtle1] at x=[5.544445], y=[5.544445], theta=[0.000000]


$ Output after running turtlesim turtle_teleop_key

andrews@andrews-virtual-machine:~$ ros2 run turtlesim turtle_teleop_key
Reading from keyboard
---------------------------
Use arrow keys to move the turtle.
Use G|B|V|C|D|E|R|T keys to rotate to absolute orientations. 'F' to cancel a rotation.
'Q' to quit.



$ Output for running ros2 node info /turtlesim 
/turtlesim

andrews@andrews-virtual-machine:~$ ros2 node info /turtlesim 
/turtlesim
/turtlesim
  Subscribers:
    /parameter_events: rcl_interfaces/msg/ParameterEvent
    /turtle1/cmd_vel: geometry_msgs/msg/Twist
  Publishers:
    /parameter_events: rcl_interfaces/msg/ParameterEvent
    /rosout: rcl_interfaces/msg/Log
    /turtle1/color_sensor: turtlesim/msg/Color
    /turtle1/pose: turtlesim/msg/Pose
  Service Servers:
    /clear: std_srvs/srv/Empty
    /kill: turtlesim/srv/Kill
    /reset: std_srvs/srv/Empty
    /spawn: turtlesim/srv/Spawn
    /turtle1/set_pen: turtlesim/srv/SetPen
    /turtle1/teleport_absolute: turtlesim/srv/TeleportAbsolute
    /turtle1/teleport_relative: turtlesim/srv/TeleportRelative
    /turtlesim/describe_parameters: rcl_interfaces/srv/DescribeParameters
    /turtlesim/get_parameter_types: rcl_interfaces/srv/GetParameterTypes
    /turtlesim/get_parameters: rcl_interfaces/srv/GetParameters
    /turtlesim/list_parameters: rcl_interfaces/srv/ListParameters
    /turtlesim/set_parameters: rcl_interfaces/srv/SetParameters
    /turtlesim/set_parameters_atomically: rcl_interfaces/srv/SetParametersAtomically
  Service Clients:

  Action Servers:
    /turtle1/rotate_absolute: turtlesim/action/RotateAbsolute
  Action Clients:

bash: /turtlesim: No such file or directory

$ Output after running :ros2 run turtlesim turtlesim_node --ros-args --remap __node:=my_turtle
andrews@andrews-virtual-machine:~$ ros2 run turtlesim turtlesim_node --ros-args --remap __node:=my_turtle
Warning: Ignoring XDG_SESSION_TYPE=wayland on Gnome. Use QT_QPA_PLATFORM=wayland to run on Wayland anyway.
[INFO] [1675462996.016075616] [my_turtle]: Starting turtlesim with node name /my_turtle
[INFO] [1675462996.047760668] [my_turtle]: Spawning turtle [turtle1] at x=[5.544445], y=[5.544445], theta=[0.000000]

$ Output after running $ ros2 node list again
andrews@andrews-virtual-machine:~$ ros2 node list
/my_turtle
/teleop_turtle
/turtlesim

$ Output after running ros2 topic list
andrews@andrews-virtual-machine:~$ ros2 topic list
/parameter_events
/rosout
/turtle1/cmd_vel
/turtle1/color_sensor
/turtle1/pose

$ Results after running ros2 topic list -t
andrews@andrews-virtual-machine:~$ ros2 topic list -t
/parameter_events [rcl_interfaces/msg/ParameterEvent]
/rosout [rcl_interfaces/msg/Log]
/turtle1/cmd_vel [geometry_msgs/msg/Twist]
/turtle1/color_sensor [turtlesim/msg/Color]
/turtle1/pose [turtlesim/msg/Pose]

$ Results after running ros2 topic echo /turtle1/cmd_vel
andrews@andrews-virtual-machine:~$ ros2 topic echo /turtle1/cmd_vel
linear:
  x: 2.0
  y: 0.0
  z: 0.0
angular:
  x: 0.0
  y: 0.0
  z: 0.0
---
linear:
  x: -2.0
  y: 0.0
  z: 0.0
angular:
  x: 0.0
  y: 0.0
  z: 0.0

  $ Results after running ros2 topic echo /turtle1/pose
  theta: -1.8240000009536743
linear_velocity: 0.0
angular_velocity: 0.0
---
x: 4.1934661865234375
y: 7.496164321899414
theta: -1.8240000009536743
linear_velocity: 0.0
angular_velocity: 0.0
---

$ Results after running ros2 topic info /turtle1/cmd_velel  (Checks topic info)
andrews@andrews-virtual-machine:~ros2 topic info /turtle1/cmd_velel
Type: geometry_msgs/msg/Twist
Publisher count: 1
Subscription count: 2


