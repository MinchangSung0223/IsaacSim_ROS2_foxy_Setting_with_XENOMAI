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

정상적으로 연결된 경우
![image](https://github.com/MinchangSung0223/IsaacSim_ROS2_foxy_Setting_with_XENOMAI/assets/53217819/09c75628-8b17-49a1-98a4-e6776bf83a3d)


ROS Bridge Extension에 omni.isaac.ros2_bridge를 선택가능 실행시 예제에 ROS예제 추가됨.
![image](https://github.com/MinchangSung0223/IsaacSim_ROS2_foxy_Setting_with_XENOMAI/assets/53217819/333487e8-fd05-40a6-810d-33fe312ded69)


Ubuntu 20.04의 경우 기본 python3.8이며 Isaac sim의 ros2를 사용하기 위해서는 python3.10을 사용해야만한다.

## 6. Python 3.10 설치

python은 ROS설치 시에 충돌 가능성이 있으므로 ROS설치 후에 설치하는 것을 추천.

```
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt install python3.10 python3.10-venv python3.10-dev
```
## 7. Isaac

