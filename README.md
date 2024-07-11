# IsaacSim_ROS2_foxy_Setting_with_XENOMAI

## 1. Nvidia driver설치
## 2. Docker 설치
## 3. ROS2 foxy 설치
## 4. Omniverse Launcher다운 및 Isaac Sim 설치
## 5. Isaac Sim과 ROS2 라이브러리연결 ~/.bashrc 수정
``` bash
gedit ~/.bashrc
```
``` bash
export isaac_sim_package_path=$HOME/.local/share/ov/pkg/isaac-sim-2023.1.1
export ROS_DISTRO=foxy
export RMW_IMPLEMENTATION=rmw_fastrtps_cpp
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$isaac_sim_package_path/exts/omni.isaac.ros2_bridge/foxy/lib
```

```
# Run Isaac Sim command
$isaac_sim_package_path/isaac-sim.sh
```


