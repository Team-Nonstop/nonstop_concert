Nonstop_concert
===============

Demo software


## Groovy ##

# Download #
```
mkdir ~/nonstop
cd ~/nonstop
wstool init src https://raw.github.com/Team-Nonstop/nonstop_concert/groovy-devel/nonstop.rosinstall
```


# Prerequsition #
```
sudo apt-get install ros-groovy-robot-pose-publisher ros-groovy-navigation

```

# Compile #
```
source /opt/ros/groovy/setup.bash
export ROS_PACKAGE_PATH=$ROS_PACKAGE_PATH:~/nonstop/src/
catkin_make
cd build; sudo make install
```

# Before RUN #
```
rosrun kobuki_ftdi create_udev_rules
> source ~/nonstop/devel/setup.bash
```

# For Convinience #
```
echo "source ~/nonstop/devel/setup.bash" >> ~/.bashrc
source ~/.bashrc
```

# Run #
```
rocon_launch nonstop_concert server.launch
```



## Hydro ##

```
mkdir ~/nonstop
cd ~/nonstop
wstool init src https://raw.github.com/Team-Nonstop/nonstop_concert/hydro-devel/nonstop.rosinstall

source /opt/ros/hydro/setup.bash
source ~/turtlebot/devel/setup.bash
catkin_make
cd build; sudo make install
source ~/nonstop/devel/setup.bash
```
### For Convinience ###
```
echo "source /opt/ros/hydro/setup.bash" >> ~/.bashrc
echo "source ~/turtlebot/devel/setup.bash" >> ~/.bashrc
echo "source ~/nonstop/devel/setup.bash" >> ~/.bashrc
```
