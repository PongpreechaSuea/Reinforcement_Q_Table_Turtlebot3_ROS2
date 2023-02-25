# ROS2-HUMBLE WITH TURTLEBOT3 Reinforcement learning Q_TABLE
 
You will need to install ROS2 on window first.
with the following steps:
1. install WSL2 :

        wsl --install
2. turn windows featuers on or off | choose :

        [x] Virtual Machine Platform
        [x] Windows Subsystem for Linux
        click OK

3. install Ubuntu 22.04 :

        wsl --install -d Ubuntu-22.04
4. open Command Prompt or terminal | Ubuntu :

        wsl
5. install ROS2 Humble : 

        sudo apt update && sudo apt install locales
        sudo locale-gen en_US en_US.UTF-8
        sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
        export LANG=en_US.UTF-8
        sudo apt install -y software-properties-common
        sudo add-apt-repository -y universe
        sudo apt -y update && sudo apt install -y curl
        sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg
        echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(. /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null
        sudo apt update -y
        sudo apt upgrade -y
        sudo apt install -y ros-humble-desktop-full
        sudo apt install -y ros-humble-turtlebot3*
        sudo apt install -y ros-dev-tools
        echo "source  /opt/ros/humble/setup.bash" >> ~/.bashrc
        echo "export  TURTLEBOT3_MODEL=burger" >> ~/.bashrc
    
##### ADD TURTLEBOT3
        export TURTLEBOT3_MODEL=burger

##### RUN MAP GAZEBO
        ros2 launch turtlebot3_gazebo turtlebot3_world.launch.py

##### CONTROL ON KEYBOARD
        ros2 run teleop_twist_keyboard teleop_twist_keyboard

##### COMAND 
    Run_ROBOT Reinforcement learning Q_TABLE
        cd %%path to you  [#example ~/edit_ros2_qtable/scrpits]
        python3 control_node.py
      
    Train_RL Reinforcement learning Q_TABLE
        cd %%path to you  [#example ~/edit_ros2_qtable/scrpits]
        python3 learning_node.py
    
    | สร้างไฟล์ README | https://dillinger.io/ |
