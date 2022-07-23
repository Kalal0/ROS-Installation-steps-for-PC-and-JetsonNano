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
             
             
             

