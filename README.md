# ROS-Installation-steps-for-PC-and-JetsonNano
This repository contains steps for installing ROS. There are plenty of other methods for installing ROS and plenty of versions to go with it. However, These steps are based on my personal experience, so I will only cover the method that worked for me. The following installation steps were done on a computer running Windows 10. <br />

# FOR PC: 

1 - Install Oracle Virtual Box -  https://www.virtualbox.org/ <br />

2 - After installation is complete and set up, create a new virtual machine and make sure the *type* is __Linux__ and the version is __Ubuntu__ (64-bit or 32-bit depends on your hardware). <br />

![image](https://user-images.githubusercontent.com/109832303/180582685-9c8404d9-095e-460b-ad46-f2ceff5b9d3a.png) <br />

3 - Follow the on-screen prompts and resize the partition and ram usage to your liking (At least 10GB of storage space is required).

4 - Download Ubuntu 20.04.4 ISO - https://releases.ubuntu.com/20.04/

5 - Now back to the Virtual Box. Right click on the Ubuntu Virtual machine you created then goto Settings -> Storage -> Controller IDE -> Empty -> then click the disk icon on the right -> Choose a disk file -> navigate to where the __Ubuntu 20.04.4 ISO__ file was downloaded and choose it.  <br />

![image](https://user-images.githubusercontent.com/109832303/180583348-52137158-3580-4d80-8d3f-7db4083b4f3f.png) 

6 - Now your virtual machine is ready, click on it to run.

7 - The virtual machine will start and Ubuntu will begin installing.

8 - After Ubuntu is finished installing and updating, it will be time to install ROS.

9 - Open the command line prompt and enter the following lines of code one after the other.

             
      1 - sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list' 
             
      2 - sudo apt install curl
       
      3 - curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
       
      4 - sudo apt update
       
      5 - sudo apt install ros-noetic-desktop-full
       
      6 - source /opt/ros/noetic/setup.bash
      
      7 - sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
      
      8 - sudo apt install python3-rosdep
      
      9 - sudo rosdep init
          rosdep update
             
             
 If you executed all these commands without any errors popping up then ROS was sucessfully installed.  
  
 For a more indepth explanations what all these commands do visit: http://wiki.ros.org/noetic/Installation/Ubuntu <br /> <br /> <br /> <br /> <br /> <br />
 
 
 
 
 
 # FOR JETSON-NANO: 
I would like to preface this by saying that I do not own a Jetson-Nano computer. This part of the guide is based off research and not actual testing. Jetson-Nano comes with Ubuntu 18.04 pre-installed. That means that Installing ROS2 off the bat is not an option since ROS2 only supports Ubuntu versions 20+. It is possible however to upgrade to version 20.04. With that being said, that's not my goal here, my goal is a quick and easy way to install ROS on the Jetson-Nano. That is why this guide will cover the installation of ROS1 on the Jetson-Nano and not ROS2. A link will be pasted at the end of this thread that will take you to an excellent guide by Q-Engineering that covers that very topic.


ROS2 for the JETSON-NANO: 
https://qengineering.eu/install-ubuntu-20.04-on-jetson-nano.html#:~:text=You%20can%20do%20this%20by,upgrade%20and%20clean%20your%20system.&text=Next%2C%20you%20need%20to%20enable,manager%2Frelease-upgrades%20file.
