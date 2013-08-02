Nonstop_concert
===============

Demo software



## Groovy ##

```
Compile
mkdir ~/nonstop
cd ~/nonstop
wstool init src https://raw.github.com/theRichu/nonstop_concert/groovy-devel/nonstop.rosinstall
```

```
source /opt/ros/groovy/setup.bash
source ~/concert/devel/setup.sh
```

```
catkin_make
cd build; sudo make install
```


### For Convinience ###
```
echo "source /opt/ros/groovy/setup.bash" >> ~/.bashrc
echo "source ~/concert/devel/setup.sh" >> ~/.bashrc

echo "export ROS_PACKAGE_PATH=$ROS_PACKAGE_PATH:~/nonstop/src/" >> ~/.bashrc
```

## Run ##
```
rocon_launch nonstop_concert server.launch
rocon_launch nonstop_concert robot.launch
```

## Hydro ##

```
mkdir ~/nonstop
cd ~/nonstop
wstool init src https://raw.github.com/theRichu/nonstop_concert/hydro-devel/nonstop.rosinstall

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
