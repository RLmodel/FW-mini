# FW-mini
Omnidirectional UGV FW-mini ROS package / YUHESEN robot platform

<br/>

## dependencies

<br/>

```bash
sudo apt install ros-humble-nav-msgs
sudo apt install ros-humble-rqt-robot-steering
```

<br/>

## clone && build && launch

<br/>

- source ROS2 environment

```bash
source /opt/ros/humble/setup.bash
```

<br/>

- move to {workspace}/{source_folder}

```bash
cd ~/ros2_ws/src
```

<br/>

- clone packages

```bash
git clone https://github.com/RLmodel/FW-mini.git
```

<br/>

- move to workspace

```bash
cd ~/ros2_ws
```

<br/>

- colcon build && source install folder

```bash
colcon build --packages-select --symlink-install yhs_can_interfaces
colcon build --packages-select --symlink-install yhs_can_control
source install/setup.bash
```

<br/>

- ip link up && set bitrate

```bash
sudo ip link can0 up type can bitrate 500000
```

<br/>

- launch

```bash
ros2 launch yhs_can_control yhs_can_control.launch.py
```

<br/>

- cmd_vel control test

```bash
rqt_robot_steering
```

<br/>

## Debug

- check can connection

```bash
ifconfig -a | grep can
```
<br/>

- check can message

```bash
candump can0
```

<br/>

## Platform && 3D Model

<br/>


![20241113_195631-1](https://github.com/user-attachments/assets/b06e4fee-adae-45a1-bf0e-8ca4c7b220d0)

![ImageToStl com_FW-MINI外发模型-V02 STEP](https://github.com/user-attachments/assets/d0a9e040-832c-4820-9b4f-4a357565bbc9)

![20241111_220627](https://github.com/user-attachments/assets/1e14b32e-8734-4d8f-9e7e-d1792b2d7477)
