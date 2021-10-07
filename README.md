# ROS2_MSYS2_MINGW64
ROS2 MSYS2/MINGW64 port [Windows]


This is  a Work In Progress.

The reasons :  
I have had a look at actual windows port and it does not fit what I need and maybe some of other users.  

When I want to use ROS2, I will setup a software, almost ready to use.

Since ROS has been developped mainly on unix environment, it sounds to me natural to use a similar environment to build it for windows.  

Then, when it comes to use it most of utilities need python and their dependencies .  
Most of python utilities should be packaged as executable and ready to use in windows environment.  

# Preliminary 
Environment development in win10
The following steps must have been setted up before proceding  
* Install a clean MSYS2 system.  
* Run MINGW64 MSYS2 shell  

## enabling symlinks in msys2 environment
by default symlinks are not enabled in msys2 environment
You must at first enable it 

This work is targetting ros2 rolling version

setup a ros2 source workspace  
mkdir ros2_rolling 
cd ~/ros2_rolling
mv -i ros2.repos ros2.repos.old
wget https://raw.githubusercontent.com/ros2/ros2/master/ros2.repos

# Workarounds to achieve the job 
## colcon
In order to be able to use colcon software to build package , it must be able to recognize bash shell in MSYS2 instead of powershell.  
colcon_bash and colcon_powershell packages must be patched.

# Building with colcon
Once colcon has been patched, you can build packages using next commandline:

colcon --build --cmake-args -G"MSYS Makefiles"

# references

