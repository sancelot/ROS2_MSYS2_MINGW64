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
Environment development  
The following steps must have been setted up before proceding  
* Install a clean MSYS2 system.  
* Run MINGW64 MSYS2 shell  


# Workarounds to achieve the job ==  
## colcon
In order to be able to use colcon software to build package , it must be able to recognize bash shell in MSYS2 instead of powershell.  


# Annexes

