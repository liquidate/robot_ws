# Control
***
### Description  
The package "Control" provides Jaguar robot control both in real world and simulation.
Hereafter, the robot state is a vector of linear velocity, angular velocity, arm joints angles, front and rear flippers angles.
The exended (initial) state is when the front and rear flippers are aligned with the robot base, the arm is perpendicularly to the latter extended.

Features:
+ Control with a keyboard
+ ROS-based control
+ Real world output
+ Simulation output 
+ Flipper and arm joint rotation constraints
+ Robot sensoric output to ROS
+ Robot state publishing to ROS
+ Initialization of the simulated robot in the initial state
+ Platform state saving and reconfiguration on the start-up to the initial state
***
### Usage
`go build cmd/control_app/control_app.go && ./control_app`  
 or  
`go build cmd/control_app/control_app.go`  
`rosrun control control_app`
***
### Workflow
![The general workflow.](https://github.com/gwaxG/robot_ws/tree/main/control/assets/workflow.png)
***
### ROS  
#### Services  
  To reset the robot to its initial state  
  `/robot/reset`  

#### Topics  
Check info about topics through:  
`rosmsg info [topic name]`  

###### Publish  
    `/cmd_vel`  
    `/cmd_flipper`  
    `/robot/sensors`  
    `/robot/state`  

###### Subscribe  
    `/robot_cmd`  
***  
### Keyboard  
`z/q` - linear velocity  
`q/d` - angular velocity  
`r/f` - front flippers  
`t/g` - rear flippers  
`y/h` - first arm joint  
`u/j` - second arm joint  
`a` - reset robot state  
`p` - exit  
`b/n` - block/release motors  
