# Nonstop_concert #
===============

Demo software


## Hydro Devel ##

### Download ###
```
mkdir ~/nonstop
cd ~/nonstop
wstool init src https://raw.github.com/Team-Nonstop/nonstop_concert/hydro-devel/nonstop.rosinstall
```
### Prerequisition ###
```
sudo apt-get install ros-hydro-turtlebot ros-hydro-turtlebot-apps ros-hydro-turtlebot-viz ros-hydro-turtlebot-simulator

sudo apt-get install python-rosdep python-wstool ros-hydro-ros
sudo rosdep init
rosdep update


```

### Get Turtlebot Package ###
```
> mkdir ~/nonstop/src/turtlebot
> cd ~/nonstop/src/turtlebot
> wstool init src https://raw.github.com/turtlebot/turtlebot/hydro-devel/turtlebot.rosinstall -j8
> source /opt/ros/hydro/setup.bash
> rosdep install --from-paths src -i -y
> cd ~/nonstop;catkin_make
```


### Compile ###
```
source /opt/ros/hydro/setup.bash
export ROS_PACKAGE_PATH=$ROS_PACKAGE_PATH:~/nonstop/src/
catkin_make
cd build; sudo make install
```

### Before FIRST run ###
```
rosrun kobuki_ftdi create_udev_rules
> source ~/nonstop/devel/setup.bash
```

### For Convinience ###
```
echo "source ~/nonstop/devel/setup.bash" >> ~/.bashrc
source ~/.bashrc
```

## Run ##
On server side
```
rocon_launch nonstop_concert nonstop_real.launch
```

On turtlebot side
```
roslaunch nonstop_client nonstop_
```
